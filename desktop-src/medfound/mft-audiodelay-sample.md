---
description: MFT \_ AudioDelay 範例
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: MFT_AudioDelay 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996633"
---
# <a name="mft_audiodelay-sample"></a>MFT \_ AudioDelay 範例

說明如何將音訊效果實作為媒體基礎轉換 (MFT) 。 音訊延遲 MFT 接受 PCM 音訊做為輸入、套用延遲 (回應) 效果，以及輸出修改過的音訊資料。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列 Microsoft 媒體基礎介面：

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>使用方式

MFT \_ AudioDelay 範例會建立一個 DLL，它是 MFT 的 COM 伺服器。 使用 MFT 之前，您必須先註冊 DLL。 您可以使用 TopoEdit 工具來建立包含音訊延遲 MFT 的拓撲。 如需 TopoEdit 的詳細資訊，請參閱 [TopoEdit](topoedit.md)。 您也可以修改 [PlaybackFX 範例](/previous-versions//bb970336(v=vs.85)) 以使用 MFT。 您將需要修改 AddBranchToPartialTopology 函式。 從下列程式程式碼變更：

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

變更為：

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

值 CLSID \_ DelayMFT 是在 MFT \_ AudioDelay 範例資料夾的標頭檔 AudioDelayUuids 中宣告的。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> <dt>

[MFT \_ 灰階範例](mft-grayscale-sample.md)
</dt> <dt>

[撰寫自訂的 MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 
