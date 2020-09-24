# K8s_Pod
碗豆莢裡面有多容器，而節點內有多碗豆莢。

![pod](https://raw.githubusercontent.com/QueenieCplusplus/K8s_Pod/master/pod.png)

# Role & Relationship 角色與關係

* 邏輯伺服器 (容器與碗豆莢的關係)

    Pod 俗稱碗豆莢子是 K8s 最基本的運作單位，內含有多個碗豆（此處即容器），一個 Pod 碗豆殼子可以算是容器的 Logical Host 邏輯伺服器，一個邏輯伺服器內含有多個 containers，而 containers 彼此是緊密耦合的。

    此處的耦合，是指容器共用邏輯伺服器內的資源，如共用儲存區。

* 豌豆莢子與豌豆莢子之間

    彼此獨立，所以 Pod 算是個沙盒。
    
* 豌豆莢子的種植農夫

   RC 全名為 Replication Controller，豌豆莢子的生命週期由 RC 管理。

* 豌豆莢子的土盆栽 (邏輯伺服器與實際虛擬伺服器的關係)

    Node 可能是實體伺服器，也可能是虛擬伺服器。

# Life Cycle 生命週期

* Pend

  定義完 Pod 後，第一階段先行傳送至 Master，讓 Master 對 Pod 進行調度協作。
  倘若到第二階段的映像檔案執行下載也屬於此階段。

* Run 

  豌豆莢子被種植入土壤中，即 Pod 被分配到某 Node 上，而相應的 container 的內涵也變成實質的映像檔 image 。

* Success

  運行成功，且不會重啟，最終狀態。

* Fail

  運行失敗，因為時間結束前，有一容器以失敗狀態結束，此為最終狀態。


# 實作範例

  https://godleon.github.io/blog/Kubernetes/k8s-Pod-Overview/
