---
description: ASF 索引子
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: ASF 索引子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adde38583d70bdbc23382e6d57316cc92b5fbd3963560a10960acbe29ea97624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881139"
---
# <a name="asf-indexer"></a>ASF 索引子

ASF *索引子* 是 WMContainer 層元件，可用來以 Advanced 系統格式讀取或寫入索引物件 (ASF) 檔。 如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。

應用程式可以使用索引子，根據展示時間來執行搜尋，或為 ASF 檔案產生新的索引項目。 ASF 索引子會實 [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) 介面。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>索引類型</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>以時間為基礎的簡報索引</td>
<td>針對索引區塊中的音訊和影片資料流程提供以時間為基礎的簡報索引編制，讓索引更具空間效率。 每個索引區塊都會參考包含位元組位移的索引項目。 <br/> 相較于 ASF 資料物件的開頭，位移是要 seeked 之資料封包的位置。<br/> GUID_Null 必須當做索引識別碼的 GUID 類型使用。 如需詳細資訊，請參閱 <a href="using-the-indexer-to-write-a-new-index.md">使用索引子來寫入新的索引</a>。<br/></td>
</tr>
<tr class="even">
<td>時間碼索引</td>
<td>協助在包含時間碼中繼資料的資料流程中依時間碼進行搜尋。 時間碼符合 SMPTE 格式 (<em>小時：分鐘：秒：畫面</em> 格) 。 每個索引區塊都會參考包含位元組位移的索引項目。 <br/> 相較于 ASF 資料物件的開頭，位移是要 seeked 之資料封包的位置。<br/>
<blockquote>
[!Note]<br />
目前不支援時間碼索引物件。
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>以框架為基礎的索引</td>
<td>提供影片資料流程的框架型索引。 以畫面格為基礎之索引的索引是以畫面格數目為基礎，而 ASF 檔案中資料流程的第一個框架對應到以框架為基礎的索引物件中的專案0。 每個索引區塊都會參考包含位元組位移的索引項目。<br/>
<blockquote>
[!Note]<br />
目前不支援以框架為基礎的索引物件。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

此章節包含下列主題。



| 主題                                                                                | 描述                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [建立和設定索引子](indexer-creation-and-configuration.md)         | 如何建立索引子物件，並將它設定為讀取現有的索引，或為檔案撰寫新的 ASF 索引物件。 |
| [使用索引子在檔案中搜尋](using-the-indexer-to-seek.md)                 | 如何使用索引子在 ASF 檔案內搜尋。                                                                               |
| [使用索引子來寫入新的索引](using-the-indexer-to-write-a-new-index.md) | 如何使用索引子來產生索引項目，以及為 ASF 檔案撰寫新的索引物件。                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMContainer ASF 元件](wmcontainer-asf-components.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




