---
description: 顯示如何在 Microsoft 媒體基礎中播放受保護的媒體內容。
ms.assetid: e4a47e1c-16aa-45c1-8aa8-8929d6e1e653
title: ProtectedPlayback 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd4290a92ba18695d1780fc0401334c4bce252754353d8757b3e904a2aa979fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034976"
---
# <a name="protectedplayback-sample"></a>ProtectedPlayback 範例

顯示如何在 Microsoft 媒體基礎中播放受保護的媒體內容。

## <a name="usage"></a>使用方式

ProtectedPlayback 範例會建立 Windows 應用程式。

若要播放本機媒體檔案，請 **選取 [檔案**] 功能表中的 [**開啟** 檔案]。 若要依 URL 指定檔案，請 **選取 [檔案**] 功能表中的 [**開啟 URL** ]。 當您選取檔案之後，播放會自動開始。 若要暫停播放，請按下空格鍵。 若要繼續播放，請再次按下空格鍵。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列媒體基礎介面：

-   [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
-   [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在[Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何播放受保護的媒體檔案](how-to-play-protected-media-files.md)
</dt> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[MFPlayer 範例](/previous-versions//bb970516(v=vs.85))
</dt> </dl>

 

 
