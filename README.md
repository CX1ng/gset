GSet
---
一个简单的Golang集合包

目前支持的操作：
+ 获取集合元素数
+ 增加元素
+ 删除元素
+ 增加多个元素
+ 删除多个元素
+ 添加数组或切片
+ 删除数组或切片
+ 获取集合中全部元素

安装
-----
    go get github.com/CX1ng/GSet

初始化
-----
    str := "apple"
    set, err := gset.NewGSet(str)
NewGSet()传入的第一个参数，其类型指定了集合存储的元素类型

方法
----
目前支持方法：
* func NewGSet(gsetType interface{}) (*GSet, error) 
* func (st GSet) Add(data interface{}) (int, error)
* func (st GSet) Remove(data interface{}) (int, error)
* func (st GSet) MultiAdd(data ...interface{}) int
* func (st GSet) MultiRemove(data ...interface{}) int
* func (st GSet) Size() int
* func (st GSet) Type() string
* func (st GSet) Clear()
* func (st GSet) Union(other GSet) (*GSet, error)
* func (st GSet) Intersect(other GSet) (*GSet, error)
* func (st GSet) Except(other GSet) (*GSet, error)
* func (st GSet) Exists(data interface{})(bool, error)
* func (st GSet) BulkAdd(data interface{}) (int, error)
* func (st GSet) BulkRemove(data interface{}) (int, error)
* func (st GSet) Keys() (int, []string)