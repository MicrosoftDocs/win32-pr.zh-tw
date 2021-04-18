---
description: 32位 Microsoft Windows 上的每個進程都有自己的虛擬位址空間，可讓您定址最多 4 gb 的記憶體。
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: 關於記憶體管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971406"
---
# <a name="about-memory-management"></a>關於記憶體管理

32位 Microsoft Windows 上的每個進程都有自己的虛擬位址空間，可讓您定址最多 4 gb 的記憶體。 64位 Windows 上的每個進程都有 8 tb 的虛擬位址空間。 進程的所有線程都可以存取其虛擬位址空間。 但是，執行緒無法存取屬於另一個進程的記憶體，以防止其他進程損毀進程。

如需虛擬位址空間和記憶體管理函數的詳細資訊，請參閱下列主題。

-   [虛擬位址空間](virtual-address-space.md)
-   [記憶體集區](memory-pools.md)
-   [記憶體效能資訊](memory-performance-information.md)
-   [虛擬記憶體函數](virtual-memory-functions.md)
-   [堆積函數](heap-functions.md)
-   [檔案對應](file-mapping.md)
-   [海量儲存體支援](large-memory-support.md)
-   [全域和區域函數](global-and-local-functions.md)
-   [標準 C 程式庫函式](standard-c-library-functions.md)
-   [比較記憶體配置方法](comparing-memory-allocation-methods.md)

 

 



