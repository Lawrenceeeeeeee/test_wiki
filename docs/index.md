---
comments: true
---
# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

!!! warning

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

## Python code example

```python
# merge sort
def merge_sort(arr):
    """
    使用归并排序算法对数组进行排序
    
    参数:
        arr: 需要排序的列表
    返回:
        排序后的列表
    """
    # 基本情况：如果数组长度小于等于1，则已排序
    if len(arr) <= 1:
        return arr
    
    # 将数组分成两半
    mid = len(arr) // 2
    left_half = arr[:mid]
    right_half = arr[mid:]
    
    # 递归地排序两半
    left_half = merge_sort(left_half)
    right_half = merge_sort(right_half)
    
    # 合并两个已排序的半数组
    return merge(left_half, right_half)

def merge(left, right):
    """
    合并两个已排序的数组
    
    参数:
        left: 左半部分已排序数组
        right: 右半部分已排序数组
    返回:
        合并后的已排序数组
    """
    result = []
    i = j = 0
    
    # 比较两个数组的元素并按顺序合并
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    
    # 添加剩余元素（如果有）
    result.extend(left[i:])
    result.extend(right[j:])
    
    return result

# 使用示例
if __name__ == "__main__":
    # 测试数组
    arr = [38, 27, 43, 3, 9, 82, 10]
    print("原始数组:", arr)
    sorted_arr = merge_sort(arr)
    print("排序后数组:", sorted_arr)
```

$$
\cos x=\sum_{k=0}^{\infty}\frac{(-1)^k}{(2k)!}x^{2k}
$$