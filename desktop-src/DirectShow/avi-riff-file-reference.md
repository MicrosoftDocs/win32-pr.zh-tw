---
description: AVI RIFF 檔案參考
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: AVI RIFF 檔案參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467898"
---
# <a name="avi-riff-file-reference"></a>AVI RIFF 檔案參考

Microsoft AVI 檔案格式是一種 RIFF 檔規格，與可捕獲、編輯及播放音訊影片順序的應用程式搭配使用。 一般情況下，AVI 檔案包含多個不同資料類型的資料流程。 大部分的 AVI 序列都會使用音訊和影片串流。 AVI 序列的簡單變化會使用影片資料，而且不需要音訊串流。

本節不說明 OpenDML AVI 檔案格式延伸模組。 如需這些擴充功能的進一步資訊，請參閱 *OPENDML Avi 檔案格式延伸* 模組，由 OpenDML avi M-JPEG 檔案格式 Subcommittee 發行。

## <a name="fourccs"></a>FOURCCs

FOURCC (四個字元的程式碼) 是串連四個 ASCII 字元所建立的32位不帶正負號的整數。 例如，FOURCC ' abcd ' 在 Little-Endian 系統上表示為0x64636261。 FOURCCs 可包含空白字元，因此 ' abc ' 是有效的 FOURCC。 AVI 檔案格式會使用 FOURCC 碼來識別資料流程類型、資料區塊、索引項目目和其他資訊。

## <a name="riff-file-format"></a>RIFF 檔案格式

AVI 檔案格式是以 RIFF (資源交換檔案格式) 檔案格式為基礎。 RIFF 檔案包含 RIFF 標頭，後面接著零或多個 *清單* 和 *區塊*。

-   RIFF 標頭的格式如下：

    `'RIFF' fileSize fileType (data)`

    其中 ' RIFF ' 是常值 FOURCC 代碼 ' RIFF '， `fileSize` 是4位元組值，提供檔案中的資料大小，而 `fileType` 是識別特定檔案類型的 FOURCC。 的值 `fileSize` 包括 FOURCC 的大小 `fileType` 加上下列資料的大小，但不包含 ' RIFF ' FOURCC 的大小或的大小 `fileSize` 。 檔案資料是以任何順序由區塊和清單所組成。

-   區塊的格式如下：

    `ckID ckSize ckData`

    其中 `ckID` 是識別區塊中所含資料的 FOURCC， `ckSize` 是4位元組值，提供中資料的大小 `ckData` ，而 `ckData` 是零或多個位元組的資料。 資料一律會填補到最接近的 **單字** 界限。 `ckSize` 提供區塊中有效資料的大小;它不包含填補、大小 `ckID` 或的大小 `ckSize` 。

-   清單的格式如下：

    `'LIST' listSize listType listData`

    其中 ' LIST ' 是常值 FOURCC 代碼 ' LIST '， `listSize` 是一個4位元組值，提供清單的大小、 `listType` 是 FOURCC 程式碼，並 `listData` 以任何順序包含區塊或清單。 的值包含的大小 `listSize` `listType` 加上大小，不 `listData` 包含 ' LIST ' FOURCC 或的大小 `listSize` 。

本節的其餘部分會使用下列標記法來描述 RIFF 區塊：

`ckID ( ckData )`

區塊大小是隱含的。 使用此標記法時，清單可以表示為：

`'LIST' ( listType ( listData ) )`

選擇性元素會放在括弧中： `[ optional element ]`

## <a name="avi-riff-form"></a>AVI RIFF 表單

AVI 檔案是由 RIFF 標頭中的 FOURCC ' AVI ' 所識別。 所有 AVI 檔案都包含兩個強制清單區塊，分別定義資料流程和資料流程資料的格式。 AVI 檔案也可能包含索引區塊，以提供檔案內資料區塊的位置。 具有這些元件的 AVI 檔案具有下列格式：


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



' Hdrl ' 清單會定義資料的格式，而且是第一個必要的清單區塊。 ' Movi ' 清單包含 AVI 序列的資料，而是第二個必要的清單區塊。 ' Idx1 ' 清單包含索引。 AVI 檔案必須以正確的順序保留這三個元件。

> [!Note]  
> OpenDML 延伸模組會定義另一個索引類型，由 FOURCC ' indx ' 識別。

 

' Hdrl ' 和 ' movi ' 清單會將 subchunks 用於其資料。 下列範例顯示以完成這些清單所需的區塊擴充的 AVI RIFF 表單：


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a>AVI 主要標頭

' Hdrl ' 清單是以包含在 ' avih ' 區塊中的主要 AVI 標頭為開頭。 主要標頭包含整個 AVI 檔案的全域資訊，例如檔案內的資料流程數目，以及 AVI 序列的寬度和高度。 主要標頭區塊是由 [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) 結構所組成。

## <a name="avi-stream-headers"></a>AVI 資料流程標頭

一或多個 ' strl ' 清單在主要標頭之後。 每個資料流程都需要 ' strl ' 清單。 每個 ' strl ' 清單都包含檔案中某個資料流程的相關資訊，而且必須包含資料流程標頭區塊 ( ' strh ' ) 和 ( ' strf ' ) 的資料流程格式區塊。 此外，' strl ' 清單可能包含資料流程標頭資料區塊 ( ' strd ' ) 和 ( ' strn ' ) 的資料流程名稱區塊。

資料流程標頭區塊 ( ' strh ' ) 由 [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) 結構組成。

資料流程格式區塊 ( ' strf ' ) 必須遵照資料流程標頭區塊。 資料流程格式區塊描述資料流程中資料的格式。 此區塊中包含的資料取決於資料流程類型。 針對影片串流，此資訊是 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構，其中包含適用的調色板資訊。 針對音訊串流，此資訊是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構。

如果資料流程標頭資料 ( ' strd ' ) 區塊存在，則會遵循資料流程格式區塊。 此區塊的格式和內容是由編解碼器驅動程式所定義。 通常，驅動程式會使用此資訊進行設定。 讀取和寫入 AVI 檔案的應用程式不需要解讀此資訊;它們可輕鬆地將它傳輸到驅動程式，做為記憶體區塊。

選擇性的 ' strn ' 區塊包含描述資料流程的以 null 結束的文字字串。

' Hdrl ' 清單中的資料流程標頭會根據 ' strl ' 區塊的順序，與 ' movi ' 清單中的資料流程資料相關聯。 第一個 ' strl ' 區塊適用于 stream 0，第二個區塊適用于 stream 1 等等。

## <a name="stream-data-movi-list"></a>串流資料 ( ' movi ' 清單) 

標頭資訊之後的「movi」清單會包含資料流程中的實際資料，也就是影片畫面和音訊範例。 資料區塊可以直接位於 ' movi ' 清單中，或可能會在 ' rec ' 清單中分組。 「Rec」群組意指應一次從磁片讀取群組的區塊，並將其用於交錯從 CD-ROM 播放的檔案。

識別每個資料區塊的 FOURCC 包含兩位數的資料流程數位，後面接著兩個字元的程式碼，以定義區塊中的資訊類型。



| 雙字元碼 | Description              |
|--------------------|--------------------------|
| db                 | 未壓縮的影片畫面 |
| dc                 | 壓縮的影片畫面   |
| pc                 | 元件變更           |
| 工 務 局                 | 音訊資料               |



 

例如，如果 stream 0 包含音訊，則該資料流程的資料區塊會有 FOURCC ' 00wb '。 如果 stream 1 包含影片，則該資料流程的資料區塊會有 FOURCC ' 01db ' 或 ' 01dc '。 影片資料區塊也可以定義新的調色板專案，在 AVI 序列期間更新調色板。 每個調色板-變更區塊 ( ' xxpc ' ) 包含 [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) 結構。 如果資料流程包含元件元件變更，請在該資料流程的 [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader)結構的 **dwFlags** 成員中設定 **AVISF \_ VIDEO \_ PALCHANGES** 旗標。

文字資料流程可以使用任意兩個字元的代碼。

## <a name="avi-index-entries"></a>AVI 索引項目

<dl> <dt>

<span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 索引
</dt> <dd>

 ( ' idx1 ' ) 區塊的選擇性索引可以跟隨在 ' movi ' 清單後面。 索引包含資料區塊的清單，以及其在檔案中的位置。 它包含 [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) 結構，其中包含每個資料區塊的專案，包括 ' rec ' 區塊。 如果檔案包含索引，請在 [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader)結構的 **dwFlags** 成員中設定 **AVIF \_ HASINDEX** 旗標。

</dd> <dt>

<span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 索引
</dt> <dd>

AVI 2.0 索引可以顯示為單一區塊。 或者，索引區段可以交錯在 ' movi ' 區塊內。 如果索引區段放在 ' movi ' 區塊中，則超級索引會包含索引區段的索引。 [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex)結構是索引區段和超級索引的基底結構。 如需詳細資訊，請參閱 OpenDML AVI M-JPEG 檔案格式 Subcommittee 所發佈的 *OPENDML Avi 檔案格式延伸*。  (此資源可能無法在某些語言及國家/地區使用。 ) 

</dd> </dl>

## <a name="other-data-chunks"></a>其他資料區塊

您可以視需要插入「垃圾」區塊，以將資料對齊 AVI 檔案。 應用程式應該忽略「垃圾」區塊的內容。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AVI 檔案格式](avi-file-format.md)
</dt> </dl>

 

 
