---
description: 系統參考時鐘
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: 系統參考時鐘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b3b4fa69b2ff9b74b937dd38d8be83203d5cdd43ba9a26d2cac4077c40c811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651838"
---
# <a name="system-reference-clock"></a>系統參考時鐘

系統參考時鐘物件會執行傳回系統時間的參考時鐘。 如果圖形中沒有任何篩選器提供參考時鐘，則篩選圖形管理員會使用此元件來同步處理圖形。 藉由呼叫 **CoCreateInstance** 來建立此物件。



| 標籤 | 值 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類別識別碼 | CLSID \_ SystemClock                                                                                                                                       |
| 介面       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)、 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)、 [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow物件](directshow-objects.md)
</dt> <dt>

[參考時鐘](reference-clocks.md)
</dt> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



