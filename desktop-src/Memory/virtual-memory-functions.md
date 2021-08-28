---
description: 虛擬記憶體函數可讓進程操作或判斷頁面在其虛擬位址空間中的狀態。
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: 虛擬記憶體函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee6839a00c573a3724cd22b3d304fef4276db29507c89802b42602120180bd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105708"
---
# <a name="virtual-memory-functions"></a>虛擬記憶體函數

虛擬記憶體函數可讓進程操作或判斷頁面在其虛擬位址空間中的狀態。 他們可以執行下列作業：

-   保留進程的虛擬位址空間範圍。 保留位址空間不會配置任何實體儲存體，但會防止其他配置作業使用指定的範圍。 它不會影響其他進程的虛擬位址空間。 保留頁面可避免不必要的實體儲存空間耗用量，同時讓進程能夠保留動態資料結構可以成長的範圍。 此程式可以視需要配置此空間的實體儲存體。
-   在進程的虛擬位址空間中認可一系列的保留頁面，讓實體儲存體 (在 RAM 或磁片) 只能供配置的進程存取。
-   針對某個範圍的認可頁面指定讀取/寫入、唯讀或無存取權。 這不同于一律以讀取/寫入存取權配置頁面的標準配置函數。
-   釋放一系列的保留頁面，讓呼叫進程可使用虛擬位址的範圍來進行後續的配置作業。
-   取消認可一系列已認可的頁面，釋出其實體儲存體，並讓它可供任何程式進行後續的配置。
-   將一或多個認可的記憶體頁面鎖定 (RAM) 的實體記憶體，讓系統無法將頁面交換到分頁檔案。
-   取得呼叫進程之虛擬位址空間中的頁面範圍或指定進程的相關資訊。
-   在呼叫進程的虛擬位址空間或指定進程的虛擬位址空間中，為指定的認可頁面範圍變更存取保護。

如需詳細資訊，請參閱下列主題。

-   [配置虛擬記憶體](allocating-virtual-memory.md)
-   [比較記憶體配置方法](comparing-memory-allocation-methods.md)
-   [釋放虛擬記憶體](freeing-virtual-memory.md)
-   [使用頁面](working-with-pages.md)
-   [記憶體管理函數](memory-management-functions.md)

 

 



