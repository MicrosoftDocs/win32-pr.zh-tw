---
description: 為什麼解碼器不接受我設定的輸入格式？
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: 為什麼解碼器不接受我設定的輸入格式？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7299045e41c7ec6e4c4796ed77e22c4b59af1f2c63dfc8817de8a551021f29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887038"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>為什麼解碼器不接受我設定的輸入格式？

有許多原因會導致解碼器拒絕格式。 最常見的是遺失或不正確的延伸格式資料。 擴充格式資料是附加至描述媒體類型結構的編解碼器特定資訊。

當您使用編碼器物件來列舉輸出類型時， [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構的 **pbFormat** 成員會指向 **WAVEFORMATEX** 結構。 此結構會附加延伸格式資料，而該資料的大小會儲存在 **WAVEFORMATEX. cbSize** 成員中。 無論使用哪一個容器來儲存壓縮的資料，您都必須保存 **WAVEFORMATEX** 結構，並將它用於此解碼器的輸入類型。 如果沒有延伸格式資料，則解碼器無法解壓縮內容。

針對影片格式，您必須手動抓取延伸格式的資料，並將其附加至 **VIDEOINFOHEADER** 結構。 如需詳細資訊，請參閱 [使用影片編解碼器私用資料](usingvideocodecprivatedata.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常見問題集](frequentlyaskedquestions.md)
</dt> </dl>

 

 
