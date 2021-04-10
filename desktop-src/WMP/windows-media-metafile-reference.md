---
title: Windows Media 中繼檔參考
description: Windows Media 中繼檔參考
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows Media 中繼檔，參考
- 中繼檔，參考
- Windows Media 中繼檔的參考
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021412"
---
# <a name="windows-media-metafile-reference"></a>Windows Media 中繼檔參考

本參考檔是 Windows Media 中繼檔的元素和副檔名。 參考分成下列各節。



| 區段                                                                                    | 描述                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media 中繼檔元素參考](windows-media-metafile-elements-reference.md) | 記載中繼檔元素，包括定義、屬性和其值，以及與每個專案相關的特殊條件。 |
| [副檔名](file-name-extensions.md)                                           | 檔中繼檔副檔名，以及其使用規則和指導方針。                                                  |



 

Windows Media 中繼檔是提供檔案資料流程及其簡報相關資訊的文字檔。 中繼檔是以可延伸標記語言 (XML)  (XML) 語法為基礎，而且是由各種類似 XML 的元素所組成，以及它們的標記和屬性。 每個元素都會定義串流媒體的設定或動作。

有兩組元素標記可供中繼檔使用。 用戶端中繼檔有一組專案，而伺服器端中繼檔則有另一組元素。

如果專案標記沒有任何子項目 (修改或包含在另一個專案) 中的專案，就可以在開頭標記的結尾處使用單一斜線字元 (/) 來取代結束記號。 如果專案的開頭和結束記號之間沒有子項目，則它們不是該專案的子專案，而且會被忽略，或在中繼檔的語法中造成錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Windows Media 中繼檔**](about-windows-media-metafiles.md)
</dt> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Media 中繼檔**](windows-media-metafiles.md)
</dt> </dl>

 

 




