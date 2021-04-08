---
title: ID3 標記支援
description: ID3 標記支援
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性、ID3 標記
- ID3 標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3dd91119aedf2983e654b4925231b8fd9e4b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021869"
---
# <a name="id3-tag-support"></a>ID3 標記支援

下表列出對應至 ID3 標記的所有屬性。 如果您想要使用 ID3 標記做為屬性，而不是使用標準的屬性名稱，請將前置詞 "ID3/" 新增至標記名稱。 例如，"ID3/TPE2" 相當於 **Author**。



| 屬性                      | ID3v1. x | ID3v 2。2 | ID3v 2.3/2.4 版 |
|--------------------------------|---------|---------|--------------|
| **Author** (作者)                     | 演出者  | TP1     | TPE1         |
| **Copyright** (著作權)                  |         | Tcr     | TCOP         |
| **CopyrightURL**               |         | WCP     | WCOP         |
| **說明**                | 註解 | COM     | COMM         |
| **有效期間**                   |         | TLE     | TLEN         |
| **FileSize**                   |         |         | TSIZ         |
| **標題**                      | 標題   | TT2     | TIT2         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/AlbumTitle**              | 專輯   | 塔爾     | TALB         |
| **WM/ArtistSortOrder**         |         |         | TSOP         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/二進位**                  |         | 地理     | GEOB         |
| **WM/評論**                |         | COM     | COMM         |
| **WM/編輯器**                |         | TCM     | TCOM         |
| **WM/導體**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | TIT1         |
| **WM/EncodedBy**               |         | 十     | TENC         |
| **WM/EncodingSettings**        |         | Tss     | TSSE         |
| **WM/EncodingTime**            |         |         | TDEN         |
| **WM/GenreID**                 | GenreID | TCO     | TCON         |
| **WM/InitialKey**              |         |         | TKEY         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/語言**                |         | TLA     | TLAN         |
| **WM/歌詞 \_ 內容**    |         | SLT     | SYLT         |
| **WM/MCDI**                    |         |         | MCDI         |
| **WM/ModifiedBy**              |         |         | TPE4         |
| **WM/情緒**                    |         |         | TMOO         |
| **WM/OriginalAlbumTitle**      |         | Tot     | 總數         |
| **WM/OriginalArtist**          |         | 守護 神     | 頂端         |
| **WM/OriginalFilename**        |         | Tof     | TOFN         |
| **WM/OriginalLyricist**        |         | TOL     | TOLY         |
| **WM/OriginalReleaseYear**     |         | Tor     | 保守黨         |
| **WM/PartOfSet**               |         | Tpa     | TPOS         |
| **WM/圖片**                 |         | PIC     | APIC         |
| **WM/PlaylistDelay**           |         |         | TDLY         |
| **WM/發行者**               |         | 城 規 會     | TPUB         |
| **WM/RadioStationName**        |         | TRN     | TRSN         |
| **WM/RadioStationOwner**       |         | TRO     | TRSO         |
| **WM/SetSubTitle**             |         |         | TSST         |
| **WM/子標題**                |         | TT3     | TIT3         |
| **WM/Text**                    |         | TXX     | TXXX         |
| **WM/TitleSortOrder**          |         |         | TSOT         |
| **WM/TrackNumber**             | Track   | TRK     | TRCK         |
| **WM/UniqueFileIdentifier**    |         | UFI     | UFID         |
| **WM/UserWebURL**              |         | WXX     | WXXX         |
| **WM/Writer**                  |         | TXT     | TEXT         |
| **WM/年**                    | Year    | 泰     | TYER         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**屬性**](attributes.md)
</dt> </dl>

 

 




