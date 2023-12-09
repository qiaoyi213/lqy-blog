+++
Title: Threaded Binary Tree 引線二元樹
+++
# 動機
寫這篇的動機是這個地方上課的時候講得很不請出而且資料又比較少，想說寫這篇順便整理清楚這個二元樹在幹嘛。


# ADT of Binary tree
```cpp
struct BinaryTreeNode{
    int data;
    BinaryTreeNode* right_child, left_child;
}
```
# Why Threaded

為何引進 Thread 這個東西，是因為當建置一般的二元樹的是時候，葉節點的左右子樹的指標都將為 NULL，如果這棵樹有 n 個節點，將會留下 n+1 個 Null pointer，這將很浪費空間。能不能將這些空的指標拿來使用，利用在 Tree traversal 的時候可以更方便呢？

# Threaded Binary Tree

Thread 就是將葉節點的 right_child 指向 inorder traversal 的下一個位置。將 left_child 指向 inorder traversal 得上一個位置．

## ADT of Threaded Binary Tree

```cpp
struct threaded_pointer {
    int data;
    threaded_pointer* right_child, left_child;
    bool right_thread, left_thread;
}
```

## Successor of a node in Threaded Binary Tree


## Inorder traversal of Threaded Binary Tree



