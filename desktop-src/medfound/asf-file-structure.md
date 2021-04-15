---
description: 本主題將說明 Advanced 系統格式的結構 (ASF) 檔。
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: ASF 檔案結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510829"
---
# <a name="asf-file-structure"></a>ASF 檔案結構

本主題將說明 Advanced 系統格式的結構 (ASF) 檔。

如需 ASF 檔案的詳細資訊，請下載 [Asf 規格](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)。 您也可以使用 [Windows MEDIA ASF Viewer 9 系列](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) 工具來查看現有 ASF 檔案的結構。

ASF 檔案的組織基礎單位稱為 *物件*。 ASF 檔案物件包含下列資料。



| 資料                                                        | 大小     |
|-------------------------------------------------------------|----------|
| 識別物件的 GUID。                          | 128 位元 |
| 物件大小。                                     | 64-位。 |
| 物件資料。 物件資料可以包含其他 ASF 物件。 | 變動。  |



 

> [!Note]  
> ASF 檔案物件只是一個資料區塊。 它不是電腦程式設計中的物件。

 

ASF 檔案包含三種類型的最上層檔案物件。



| ASF 檔案物件                                                                                                                      | Description                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header 物件<br/>         | 包含 ASF 檔案的相關資訊。<br/>  |
| <span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data 物件<br/>                     | 包含媒體資料的封包。<br/>           |
| <span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> 索引物件 (s) <br/> | 包含一或多個索引。 (選擇性。)<br/> |



 

下圖顯示 ASF 檔案結構。

![顯示 asf 檔案結構的圖表，包括標頭、資料和索引內的專案](images/asf-components04.png)

此圖表不會繪製以進行調整;通常，資料物件會包含大部分的檔案。

### <a name="header-object"></a>Header 物件

標頭物件是必要的，而且會出現在每個 ASF 檔案的開頭。 它包含通用檔案屬性，以及有關 ASF 檔案中資料流程的資訊。 這項資訊是用來解讀和播放檔案中的資料。

標頭物件包含數個強制子物件：

-   檔案屬性物件會描述檔案的全域屬性，例如檔案大小、播放持續時間、資料封包數、最小和最大封包大小，以及最大位元速率。
-   標頭擴充物件可將其他功能新增至 ASF 檔案，同時維持回溯相容性。
-   資料流程屬性物件會描述檔案中的一個資料流程。 ASF 檔案必須包含至少一個資料流程，因此至少必須包含一個資料流程屬性物件。

標頭物件可以包含其他選用的資訊，包括與檔案相關的中繼資料 (例如標題和作者) 、用來編碼檔案的編解碼器清單，以及內容保護資訊。

### <a name="data-object"></a>資料物件

ASF 資料物件包含 ASF 檔案的所有媒體資料。 此物件是必要的，而且必須遵循 ASF 標頭物件。

資料物件會分割成資料封 *包*。 每個封包都包含檔案中一個或多個資料流程的資料。 資料封包包含可提供封包剖析資訊的資料封包標頭，後面接著承載資料的實際數位媒體資料。 所有的資料封包都有相關聯的呈現時間，並依照收到的順序排列。

資料物件內容的相關資訊（例如封包大小和封包計數）會儲存在標頭物件中。

### <a name="index-object"></a>Index 物件

索引物件是選擇性的，且是 ASF 檔案中的最後一個物件。 ASF 檔案可以包含一個以上的索引物件。 Index 物件提供以時間為基礎的隨機存取 ASF 資料物件。

簡單的索引物件是另一種索引類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




