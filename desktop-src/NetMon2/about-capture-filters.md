---
description: 捕捉篩選器是 NPP 應用程式的元素，會指示網路監視器驅動程式 (Nmnt.sys) 要保留的網路資料框架以及要忽略的畫面格。
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: 關於 Capture 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987518"
---
# <a name="about-capture-filters"></a>關於 Capture 篩選

捕捉篩選器是 NPP 應用程式的元素，會指示網路監視器驅動程式 (Nmnt.sys) 要保留的網路資料框架以及要忽略的畫面格。 設定捕獲篩選器的優點是提高效率。 您不需要檢查已捕獲的框架;網路監視器驅動程式會進行檢查。 這種方法可消除畫面格複製，以提供記憶體使用優勢。

## <a name="capture-filter-structure"></a>Capture 篩選結構

Capture 篩選器包含三個元素：

-   Etype/SAP 設定
-   位址
-   模式比對

這些專案一起會以邏輯方式評估在 NPP 應用程式作業期間要包含或排除的畫面格。 「捕捉」篩選器會對 NPP 應用程式提供複雜的框架元素與排除專案。

網路監視器透過 [**CAPTUREFILTER**](the-capturefilter-structure.md)傳遞至 NPP 的資料結構來執行 capture 篩選器，然後在開始時傳遞到網路監視器驅動程式。

如需 NPP 作業和 BLOB 功能的詳細資訊，請參閱 [網路封包提供者](network-packet-providers.md) 和 [網路監視器 blob](network-monitor-blobs.md)。

 

 



