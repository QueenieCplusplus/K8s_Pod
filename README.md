# K8s_Pod
碗豆莢裡面有多容器，而節點內有多碗豆莢。

* 邏輯伺服器 (容器與碗豆莢的關係)

Pod 俗稱碗豆莢子是 K8s 最基本的運作單位，內含有多個碗豆（此處即容器），一個 Pod 碗豆殼子可以算是容器的 Logical Host 邏輯伺服器，一個邏輯伺服器內含有多個 containers，而 containers 彼此是緊密耦合的。

此處的耦合，是指容器共用邏輯伺服器內的資源，如共用儲存區。

* 豌豆莢子與豌豆莢子之間

彼此獨立，所以 Pod 算是個沙盒。

* 豌豆莢子的土盆栽 (邏輯伺服器與實際虛擬伺服器的關係)

Node 可能是實體伺服器，也可能是虛擬伺服器。
