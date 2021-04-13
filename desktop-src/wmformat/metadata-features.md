---
title: 中繼資料功能
description: 中繼資料會在 ASF 檔案中用來描述檔案內容和屬性。
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows Media Format SDK，中繼資料功能
- Windows Media Format SDK，功能
- Advanced Systems Format (ASF) ，中繼資料功能
- ASF (Advanced Systems Format) ，中繼資料功能
- Advanced Systems Format (ASF) ，功能
- ASF (Advanced Systems Format) ，功能
- 中繼資料，功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374801"
---
# <a name="metadata-features"></a>中繼資料功能

中繼資料會在 ASF 檔案中用來描述檔案內容和屬性。 您建立的所有 ASF 檔案都應該包含適當的中繼資料。  (如需總覽，請參閱 [中繼資料](metadata.md)。 ) Windows MEDIA 格式 SDK 支援透過寫入器物件、中繼資料編輯器物件，以及讀取器和同步讀取器物件來編輯中繼資料。 包含各種中繼資料屬性的原生支援。 如需預先定義的屬性清單，請參閱 [屬性](attributes.md) 。

Windows Media Format SDK 的各種物件所提供的中繼資料支援有彈性且功能強大。 下列清單摘要說明主要的中繼資料功能：

-   彈性的屬性大小。 中繼資料屬性的大小不限。
-   資料流程層級屬性。 ASF 檔案中的中繼資料可以指派給整個檔案，或指派給特定的資料流程。
-   重複的屬性。 您可以在相同的檔案中多次使用命名屬性。 這項功能在指派內容描述性屬性時特別使用。 例如，某首歌可能會有多位作者，而每位作者在檔案中都需要個別的 **Author** 屬性。
-   多種語言。 每個屬性都有相關聯的語言。 您可以設定支援的語言，然後將它指派給您所撰寫的每個屬性。 由於您可以複製屬性，因此您可以使用數種語言提供最重要的屬性來觸及較大的物件。 如果您未指定語言，則會使用從執行應用程式之電腦的作業系統取得的預設語言 () 。
-   複雜屬性。 某些預先定義的屬性支援結構化資料。 針對這些屬性，資料類型為 binary，但值為此 SDK 中定義的結構。

下列主題將討論其他支援的中繼資料功能。



| 主題                                  | 描述                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [ID3 支援](id3.md)                 | 討論如何使用 Windows Media Format SDK 的物件來支援 ID3 框架。 |
| [自訂中繼資料](custom-metadata.md) | 討論使用自訂中繼資料的含意。                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**功能**](features.md)
</dt> <dt>

[**IWMHeaderInfo 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMHeaderInfo2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[**IWMHeaderInfo3 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[**中繼資料**](metadata.md)
</dt> </dl>

 

 




