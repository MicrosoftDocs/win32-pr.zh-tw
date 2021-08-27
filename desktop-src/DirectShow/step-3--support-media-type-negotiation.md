---
description: 在撰寫轉換篩選時，實作為媒體類型協商的支援。 媒體類型描述資料的格式。
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: 步驟 3： 支援媒體類型的協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1558d5b1a7fd9db41fef7e5a9818d93c306f4f15f42099d4cb88f66b34725660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051468"
---
# <a name="step-3-support-media-type-negotiation"></a>步驟 3： 支援媒體類型的協商

這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟3。

當兩個 pin 連線時，他們必須同意連接的媒體類型。 媒體類型描述資料的格式。 如果沒有媒體類型，篩選器可能會提供一種資料，只是讓另一個篩選器將它視為其他的篩選準則。

協商媒體類型的基本機制是 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法。 輸出圖釘會以建議的媒體類型，在輸入 pin 上呼叫這個方法。 輸入 pin 接受連接或拒絕連接。 如果拒絕連線，輸出 pin 可以嘗試其他媒體類型。 如果找不到適合的類型，連接就會失敗。 輸入 pin 可以選擇性地透過 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法，通告其慣用的類型清單。 當輸出 pin 提議媒體類型時，就可以使用這份清單，雖然不需要這麼做。

**CTransformFilter** 類別會為此程式實作為一般架構，如下所示：

-   輸入 pin 沒有慣用的媒體類型。 它完全依賴上游篩選器來提議媒體類型。 對於影片資料而言很有意義，因為媒體類型包含影像大小和畫面播放速率。 一般而言，該資訊必須由上游來源篩選器或剖析器篩選器提供。 在音訊資料的情況下，可能會有一組較小的格式，因此輸入 pin 可能會提供一些慣用的類型。 在此情況下，請覆寫輸入釘選上的 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 。
-   當上游篩選提議媒體類型時，輸入 pin 會呼叫 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法，以接受或拒絕該類型。
-   除非先連接輸入 pin，否則輸出 pin 將不會連接。 這是轉換篩選準則的一般行為。 在大部分的情況下，篩選準則必須先判斷輸入類型，才能設定輸出類型。
-   當輸出連接連接時，它會有一份向下游篩選器提出的媒體類型清單。 它會呼叫 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法來產生這份清單。 輸出釘選也會嘗試下游篩選準則所建議的任何媒體類型。
-   若要檢查特定的輸出類型是否與輸入類型相容，輸出圖釘會呼叫 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法。

先前所列的三個 **CTransformFilter** 方法是純虛擬方法，因此您的衍生類別必須執行這些方法。 這些方法都不屬於 COM 介面;它們只是基類所提供之實作為的一部分。

下列各節會更詳細地說明每個方法：

-   [步驟3A。執行 CheckInputType 方法](step-3a--implement-the-checkinputtype-method.md)
-   [步驟3B。執行 GetMediaType 方法](step-3b--implement-the-getmediatype-method.md)
-   [步驟3C。執行 CheckTransform 方法](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選準則的連線](how-filters-connect.md)
</dt> <dt>

[撰寫 DirectShow 篩選](writing-directshow-filters.md)
</dt> </dl>

 

 



