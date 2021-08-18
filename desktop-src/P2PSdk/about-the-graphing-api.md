---
description: 對等圖形 API 可讓應用程式有效率且可靠地在對等之間傳遞資料。 對等圖形技術的核心概念是對等圖形的節點，以及事件通知。
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: 關於圖形 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735bf7993744aa8d1e76b8c5d98e8d6856bb4e1757224cd0c98f2e7b1b6f710b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011786"
---
# <a name="about-the-graphing-api"></a>關於圖形 API

對等圖形 API 可讓應用程式有效率且可靠地在對等之間傳遞資料。 對等圖形技術的核心概念是對等圖形的 **節點** ，以及事件通知。

## <a name="nodes"></a>節點

節點代表網路上對等的特定實例。 對等圖形 API 基礎結構可確保每個節點在圖形中都具有一致的資料檢視。 節點有下列功能：

-   可以連接到不同的節點，並形成稱為對等圖形的相互關聯網路。
-   可以與圖形中的其他節點以 [記錄](records.md)形式共用資料。
-   可以建立與使用對等 [群組 API](about-the-grouping-api.md)所建立之對等圖形分開的直接連接。
    > [!Note]  
    > 直接連接可讓節點將私用資料傳送給彼此。

     

## <a name="event-notices"></a>事件通知

對等圖形 API 有一個事件基礎結構，可讓應用程式在對等圖形 API 基礎結構內註冊及接收對等事件的通知。 當對等圖形中的某個專案發生變更時，應用程式會傳送事件通知，以識別已發生變更。

 

 



