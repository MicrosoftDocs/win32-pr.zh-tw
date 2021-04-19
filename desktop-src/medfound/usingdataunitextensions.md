---
description: 描述如何在使用 Windows Media 編碼器時新增資料單位延伸模組。
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: '使用資料單位延伸模組 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c16053ee078f5adcd48767f53d9e6e1c0eeb02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981456"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>使用資料單位延伸模組 (Microsoft 媒體基礎) 

Windows Media 音訊和影片編解碼器是設計來搭配 Advanced Systems Format (ASF) 容器使用。 ASF 是用來 Windows Media 音訊 (WMA) 檔案和 Windows Media 視訊 (WMV) 檔的結構化格式。 它是針對串流資料而設計的可擴充格式。 ASF 結構的其中一個不尋常特性是能夠將中繼資料附加至個別範例，並將該資料與位資料流程中的範例一起內嵌。 以這種方式儲存的中繼資料專案稱為資料 *單位延伸* 模組或 *範例延伸* 模組。

資料單位延伸可以包含編碼器、解碼器或播放程式應用程式所需的資訊。 Windows Media 9 系列編解碼器中所執行的大部分資料單位延伸模組類型，都包含用於解碼和轉譯媒體的應用程式所適用的資料。 例如，您可以藉由將它新增為數據單位延伸，來維護來源資料的 SMPTE 時間代碼。 但是，下列編解碼器功能需要資料單位延伸：

-   [強制插入主要畫面格](forcedkeyframeinsertion.md)
-   [交錯式影片編碼](interlacedvideoencoding.md)
-   直接存取編解碼器時使用資料單位延伸的困難之處，就是物件接收延伸資料的機制。 這是由 Windows Media Format SDK 的物件使用設計來支援此功能的緩衝區物件來達成。 建議您使用 Windows Media Format SDK 來啟用需要資料單位延伸的編解碼器功能，但您可以將這些功能與獨立的編解碼器物件搭配使用。

## <a name="passing-extended-samples-to-the-codec-objects"></a>將延伸範例傳遞給編解碼器物件

Windows Media 格式 SDK 會使用公開 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) 介面的緩衝區物件。 最新的介面為 [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4)。 若要使用資料單位延伸將範例傳遞給編解碼器物件，您必須使用可實 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) 或 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面和 **INSSBuffer** 介面的緩衝區物件。 您可以使用 Windows Media Format SDK 或 Microsoft 媒體基礎所建立的緩衝區物件來完成這項工作，或者您可以自行建立符合需求的緩衝區類別。 若要建立您自己的緩衝區類別，您必須符合 **INSSBuffer** 介面的方法原型。 這些介面定義可以在隨 Windows Media Format SDK 安裝的 wmsbuffer .h 標頭檔中找到。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Media 轉碼器](windows-media-codecs.md)
</dt> </dl>

 

 
