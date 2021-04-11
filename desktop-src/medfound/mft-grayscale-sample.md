---
description: 說明如何將影片效果實作為媒體基礎轉換 (MFT) 。
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: MFT_Grayscale 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114393"
---
# <a name="mft_grayscale-sample"></a>MFT \_ 灰階範例

說明如何將影片效果實作為媒體基礎轉換 (MFT) 。 灰階 MFT 可將影片中的色度值設定為中性，以將 YUV 影片轉換成灰階。 MFT 以 UYVY、YUY2 或 NV12 格式接受未壓縮的影片。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列 Microsoft 媒體基礎介面：

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>使用方式

MFT \_ 灰階範例會建立一個 DLL，它是 MFT 的 COM 伺服器。 使用 MFT 之前，您必須先註冊 DLL。

若要查看使用中的灰階 MFT，請執行 [PlaybackFX 範例](/previous-versions//bb970336(v=vs.85))。 您也可以使用 TopoEdit 工具來建立包含灰階 MFT 的拓撲。 如需 TopoEdit 的詳細資訊，請參閱 [TopoEdit](topoedit.md)。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 YUV 影片](about-yuv-video.md)
</dt> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> <dt>

[MFT \_ AudioDelay 範例](mft-audiodelay-sample.md)
</dt> <dt>

[撰寫自訂的 MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 
