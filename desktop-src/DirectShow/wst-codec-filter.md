---
description: WST 編解碼器篩選
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: WST 編解碼器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e729e13500317711076f6cdbd39c9a6ab25bea77e8d378e12f917f2e20e4a561
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083448"
---
# <a name="wst-codec-filter"></a>WST 編解碼器篩選

> [!IMPORTANT]
> 此元件已從 Windows Vista 和更新版本的作業系統中移除。 它可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。

 

從 Windows Vista 開始，此篩選器會取代為 Microsoft 電視技術檔中記載的 VBICodec 篩選器。

全球標準 Teletext (WST) 是使用 VBI 在 PAL 類比電視信號上進行資料傳輸的歐洲標準。 這兩個字幕和資料服務都是使用這個標準提供的。 WST 編解碼器是一種核心模式篩選器，它會接收原始 VBI 範例，並選擇性地從 Capture 篩選器篩選器中的 Teletext 範例，透過端 [對端對接收器轉換器](tee-sink-to-sink-converter.md) 篩選。 此編解碼器會解碼及/或複製 [WST 解碼](wst-decoder-filter.md) 篩選器的已解碼和向前更正錯誤的 Teletext 資料。 WST 編解碼器對應于 NTSC 傳輸的 CC 編碼器篩選器。 WST 解碼器對應于 NTSC 的[第21行](line-21-decoder-filter.md)：這些篩選器會建立傳送至重迭 Mixer 或影片混合轉譯器的點陣圖。

此篩選器有兩個輸入圖釘： VBI 和 HWCC。 VBI 的 pin 會用於原始的 VBI 資料，而 HWCC 的 pin 會在使用 capture 篩選器在硬體中執行 VBI 解碼時使用。 在 HWCC 釘選上接收資料時，WST 編解碼器會在「通過」模式中運作，並將資料直接傳送至 WST 的編碼器，而不需要以任何方式進行處理。 如果捕捉篩選器公開 HWCC 的 pin，則必須直接連線到 WST 編解碼器上的對應 pin。

WST 編解碼器篩選器會出現在「WDM 串流 VBI 編解碼器」篩選類別中， (**AM \_ KSCATEGORY \_ VBICODEC**) 。

由於這是核心模式篩選器，因此應用程式無法直接使用 **CoCreateInstance** 來建立它。 相反地，請使用 [系統裝置枚舉器](system-device-enumerator.md)。 如需詳細資訊，請參閱 [建立 Kernel-Mode 篩選](creating-kernel-mode-filters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[觀賞全球標準 Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



