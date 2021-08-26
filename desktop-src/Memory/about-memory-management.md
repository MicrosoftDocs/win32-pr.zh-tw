---
description: 32位 Microsoft Windows 上的每個進程都有自己的虛擬位址空間，可讓您定址最多 4 gb 的記憶體。
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: 關於記憶體管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b2cc91b2a907fa5f9db24f42393be51bb8795200357eff0b612f8241219361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869968"
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

 

 



