---
description: 解碼器的需求
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: 解碼器的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84d02926b4ce36cea9e4221589d52690edb8e256b2f0f4863fa19fff5dc033
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697028"
---
# <a name="requirements-for-decoders"></a>解碼器的需求

傳遞範例給 VMR 的解碼器必須遵守下列規則：

-   每個影片畫面應該會有一個子圖片的框架傳遞至 VMR。 這兩個畫面格的時間戳記應該相同。
-   如果子圖片未變更，請使用 \_ \_ [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法中的 AM GBF NOTASYNCPOINT 旗標，強制配置器傳回緩衝區，其中包含傳遞至 VMR 的最後一個畫面格。 只要將新的時間戳記放在範例上，然後再將它傳遞至 VMR。 如果子圖片成名是空白的，您仍然應該提供它。 VMR 將會偵測到空白框架，而不會將它與影片混合。 這項測試是由 VGA 晶片執行，並不會影響播放效能。
-   除了即時資料流以外的所有範例都必須附加有效的開始和停止時間戳記。  (DVD 不是即時串流。 ) 
-   媒體取樣時間戳記必須是連續的
-   此解碼器必須將本身識別為可供圖形產生器使用的 VMR。
-   子圖片資料流程現在應該包含內嵌的每圖元 Alpha 值。 ARGB4444 介面類別型很適合用於 subpictures。
-   請勿假設子圖片的 stride 與表面寬度相同。 這不一定是 VMR 的情況。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DirectX Video 加速](about-directx-video-acceleration.md)
</dt> </dl>

 

 



