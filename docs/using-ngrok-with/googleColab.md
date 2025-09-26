import matplotlib.pyplot as plt
import matplotlib.patches as patches
from matplotlib.font_manager import FontProperties
from matplotlib import rcParams

# 设置中文字体（请确保系统有该字体，如SimHei）
rcParams['font.sans-serif'] = ['SimHei', 'DejaVu Sans']
plt.figure(figsize=(8.27, 11.69), dpi=300)  # A4尺寸，高DPI确保清晰
ax = plt.gca()
ax.set_facecolor('#f5e8c8')

# 绘制古典边框
border = patches.Rectangle((0.5, 0.5), 0.94, 0.94, linewidth=3, edgecolor='#8b4513', facecolor='none', transform=ax.transAxes)
ax.add_patch(border)

# 标题文字
plt.text(0.5, 0.7, '至圣先师', fontsize=32, ha='center', color='#8b4513', fontproperties=FontProperties(size=32))
plt.text(0.5, 0.6, '孔子', fontsize=48, ha='center', color='#8b4513', fontproperties=FontProperties(size=48, weight='bold'))
plt.text(0.5, 0.3, '翻翻书', fontsize=18, ha='center', color='#666666')

plt.axis('off')
plt.savefig('孔子翻翻书_封面.png', bbox_inches='tight', dpi=300)
plt.show()
