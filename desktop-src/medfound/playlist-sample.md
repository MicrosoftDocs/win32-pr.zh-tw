---
description: 播放清單範例
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: 播放清單範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987427"
---
# <a name="playlist-sample"></a>播放清單範例

顯示如何使用 Microsoft 媒體基礎播放播放清單中的音訊檔案序列。 此範例會使用 [Sequencer 來源](sequencer-source.md) 來建立和管理播放清單。

> [!Note]  
> SDK 中已不再包含此範例。

 

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列媒體基礎介面：

-   [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>使用方式

播放清單範例會建立 Windows 應用程式。

-   若要建立新的播放清單，請 **選取 [檔案**] 功能表中的 [**加入至播放清單**]。 在 [ **開啟** 檔案] 對話方塊中，選取一或多個音訊檔案。 檔案會新增至播放清單。
-   若要播放順序，請按一下 [ **播放**]。
-   若要暫停目前的區段，請按一下 [ **暫停**]。
-   若要停止目前的區段，請按一下 [ **停止**]。
-   若要略過檔案，請按兩下播放清單中的專案。
-   若要從播放清單中刪除檔案，請選取播放清單中的專案。 然後選取 [檔案] 功能表中 **的 [** **從播放清單移除**]。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

下列位置提供此範例。



| Location                                                     | 路徑/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [Windows SDK](https://www.microsoft.com/download/details.aspx?id=8279) | *SDK 根目錄* \\範例 \\ 多媒體 \\ mediafoundation \\ 播放清單 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[BasicPlayback 範例](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[Sequencer 來源](sequencer-source.md)
</dt> </dl>

 

 
