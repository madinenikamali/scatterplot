# scatterplot
import numpy as np
import matplotlib.pyplot as plt
np.random.seed(0)
num_points = 100
x = np.random.rand(num_points)
y = np.random.rand(num_points)
colors = np.random.rand(num_points)
sizes = 1000 * np.random.rand(num_points)
plt.scatter(x, y, c=colors, s=sizes, alpha=0.5, cmap='viridis')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Scatter Plot Example')
cbar = plt.colorbar()
cbar.set_label('Color Intensity')
legend_elements = [
    plt.Line2D([0], [0], marker='o', color='w', markerfacecolor='blue', markersize=10, label='Group A'),
    plt.Line2D([0], [0], marker='o', color='w', markerfacecolor='green', markersize=10, label='Group B'),
]
plt.legend(handles=legend_elements, loc='upper right')
plt.grid(True)
plt.xlim(0, 1)
plt.ylim(0, 1)
plt.show()
