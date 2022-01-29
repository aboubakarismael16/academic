title: Welcome to my demo post
subtitle: map

summary: ""

# Link this post with a project
projects: []

# Date published
date: "2022-02-29T00:00:00Z"


# Date updated
lastmod: "2022-01-29T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false


# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- golang


categories:
- Demo
---

## 1. map struct

Golang's map uses hash table as the underling implemention. There can be multiple hash table nodes in a hash table, that is buckets, and each bucket is saved one or a set of key value pairs in hte map.

map struct is set on `runtime/map/map.go/hmap`

```go
type hmap struct{
    count     int// 当前保存的元素个数
    ...
    B         uint8  // 指示bucket数组的大小
    ...
    buckets    unsafe.Pointer// bucket数组指针，数组的大小为2^B
    ...
}
```




