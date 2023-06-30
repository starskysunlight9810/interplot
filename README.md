# interplot

interplot is a R package designed specifically for the calculation and visualization of intersection results derived from multiple BED format files.

Main code by Xinkai Zhou.

## Requirements

1. `corrplot`
2. `ggplot2`
3. `ggpolypath`
4. `ggthemes`
5. `paletteer`
6. `plotrix`
7. `UpSetR`
8. `valr`
9. `venn`

## How to use interplot

### Venn/Upset plot for multiple intersections

```
# Get beds using get_beds
beds <- get_beds(c('path1', 'path2', ... ))

# Use get_combine_result() to get intersection result
# The processing time may vary depending on the number of sets involved
inputs <- get_combine_result(beds)

# Venn plot
draw_venn(inputs, beds)

# Upset plot
draw_upset(inputs, beds)
```

### Corrplot for pairwise intersections

```
# Get beds using get_beds
beds <- get_beds(c('path1', 'path2', ... ))

plot <- cal_pairwise(beds)
```

### Flower plot

```
draw_flower(c('path1','path2', ...))
```
