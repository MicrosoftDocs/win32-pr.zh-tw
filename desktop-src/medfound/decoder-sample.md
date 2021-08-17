---
description: 示範如何撰寫 Microsoft 媒體基礎的解碼器。
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: 解碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290f8b2db32b12d535feaeef65f37b77e1a29115cd8844a8d8aad29fb7ce699a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449381"
---
# <a name="decoder-sample"></a>解碼範例

示範如何撰寫 Microsoft 媒體基礎的解碼器。

此範例會執行模擬的 MPEG-2 視頻解碼器，以顯示每個影片畫面的時間代碼。 它並不會實際解碼 MPEG 1 位流。 下圖顯示來自解碼器的影片輸出。

![來自解碼器之影片畫面格的螢幕擷取畫面](images/decodersample.png)

> [!Note]  
> 在 Windows 7 的 Windows SDK 之前，此範例包含在[MPEG1Source 範例](mpeg1source-sample.md)中。

 

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列媒體基礎介面：

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在[Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> <dt>

[撰寫自訂的 MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



