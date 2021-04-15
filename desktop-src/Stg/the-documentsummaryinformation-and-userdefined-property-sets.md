---
title: DocumentSummaryInformation 和使用者設定的屬性集
description: DocumentSummaryInformation 和使用者設定的屬性集是摘要資訊屬性集的延伸。 這兩個屬性集可以同時存在。
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- 使用者設定的屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507204"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>DocumentSummaryInformation 和使用者設定的屬性集

**DocumentSummaryInformation** 和 **使用者** 設定的屬性集是 [摘要資訊屬性集](the-summary-information-property-set.md)的延伸。 這兩個屬性集可以同時存在。

包含 **DocumentSummaryInformation** 屬性集之資料流程的名稱為 **" \\ 005DocumentSummaryInformation"**。 **DocumentSummaryInformation** 屬性集的格式識別碼 (FMTID) 為 **D5CDD502-2E9C-101B-9397-08002B2CF9AE**。

提供的標頭檔中提供此值的宣告作為 **FMTID \_ DocSummaryInformation**。 如需詳細資訊，請參閱 [IStorage](names-in-istorage.md)中 [的名稱、摘要資訊屬性集](the-summary-information-property-set.md)、 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 和 [Format 識別碼](format-identifiers.md)。

針對自訂使用者定義的屬性，此資料流程也有個別的區段，如同在 **DocumentSummaryInformation** 和 **使用者** 定義的屬性集中。 此區段會以個別屬性集的形式出現在 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面中，並以 **FMTID \_ UserDefinedProperties**) ： **D5CDD505-2E9C-101B-9397-08002B2CF9AE** 的形式 (提供下列 FMTID。

這兩個屬性集是單一資料流程可以包含多個屬性集的唯一一個屬性集。 這兩個屬性集在單一資料流程中的事實，會影響 **IPropertySetStorage** 介面的行為。 如需詳細資訊，請參閱 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)。

下表列出新增的屬性至 **DocumentSummaryInformation** 和 **使用者** 設定的屬性集。 如同 **SummaryInformation** 屬性集，名稱通常不會儲存在屬性集中，而是從屬性識別碼推斷而來。



| 屬性名稱      | 屬性識別碼     | 屬性識別碼值 | VARIANT 類型                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| 類別           | **PIDDSI \_ 類別**    | 0x00000002                | **VT \_ LPSTR**                     |
| PresentationTarget | **PIDDSI \_ PRESFORMAT**  | 0x00000003                | **VT \_ LPSTR**                     |
| 位元組              | **PIDDSI \_ BYTECOUNT**   | 0x00000004                | **VT \_ I4**                        |
| 線條              | **PIDDSI \_ LINECOUNT**   | 0x00000005                | **VT \_ I4**                        |
| 段落         | **PIDDSI \_ PARCOUNT**    | 0x00000006                | **VT \_ I4**                        |
| 投影片             | **PIDDSI \_ SLIDECOUNT**  | 0x00000007                | **VT \_ I4**                        |
| 備註              | **PIDDSI \_ NOTECOUNT**   | 0x00000008                | **VT \_ I4**                        |
| HiddenSlides       | **PIDDSI \_ HIDDENCOUNT** | 0x00000009                | **VT \_ I4**                        |
| MMClips            | **PIDDSI \_ MMCLIPCOUNT** | 0x0000000A                | **VT \_ I4**                        |
| ScaleCrop          | **PIDDSI \_ SCALE**       | 0x0000000B                | **VT \_ BOOL**                      |
| HeadingPairs       | **PIDDSI \_ HEADINGPAIR** | 0x0000000C                | **VT \_VARIANT** \| **VT \_ 向量** |
| TitlesofParts      | **PIDDSI \_ DOCPARTS**    | 0x0000000D                | **VT \_向量** \| **VT \_ LPSTR**   |
| Manager            | **PIDDSI \_ 管理員**     | 0x0000000E                | **VT \_ LPSTR**                     |
| 公司            | **PIDDSI \_ 公司**     | 0x0000000F                | **VT \_ LPSTR**                     |
| LinksUpToDate      | **PIDDSI \_ LINKSDIRTY**  | 0x00000010                | **VT \_ BOOL**                      |



 

這些屬性具有下列用途：

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>類別
</dt> <dd>

使用者輸入的文字字串，指出檔案所屬的類別 (備忘錄、提案等) 。 它很適合用來尋找相同類型的檔案。

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget
</dt> <dd>

簡報 (35mm、印表機、影片等) 的目標格式。

</dd> <dt>

<span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>位元組
</dt> <dd>

位元組數。

</dd> <dt>

<span id="Lines"></span><span id="lines"></span><span id="LINES"></span>線
</dt> <dd>

行數。

</dd> <dt>

<span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>段落
</dt> <dd>

段落數目。

</dd> <dt>

<span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>幻燈片
</dt> <dd>

幻燈片數目。

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>筆記
</dt> <dd>

包含附注的頁面數目。

</dd> <dt>

<span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides
</dt> <dd>

隱藏的幻燈片數。

</dd> <dt>

<span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips
</dt> <dd>

音效或影片剪輯的數目。

</dd> <dt>

<span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop
</dt> <dd>

當需要調整縮圖時，設定為 True (-1) 。 如果未設定，則需要裁剪。

</dd> <dt>

<span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs
</dt> <dd>

內部使用的屬性，指出不同檔部分的群組以及每個群組中的專案數。 檔部分的標題會儲存在 **TitlesofParts** 屬性中。 **HeadingPairs** 屬性會以一組重複的 **vt \_ LPSTR** (或 **vt \_ LPWSTR**) 和 **vt \_ I4** 值，儲存為 variant 的向量。 **Vt \_ LPSTR** 值代表標題名稱，而 **vt \_ I4** 值則表示該標題底下的檔部分計數。

</dd> <dt>

<span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts
</dt> <dd>

檔元件的名稱。

</dd> <dt>

<span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>經理
</dt> <dd>

專案的管理員。

</dd> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>公司
</dt> <dd>

公司名稱。

</dd> <dt>

<span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate
</dt> <dd>

布林值，指出針對所有應用程式，自訂連結是否受到過度雜訊的阻礙。

> [!Note]  
> 如12.3 中所述。 OLE 2.0 設計規格之屬性集的序列化格式， **HeadingPairs** 和 **TitlesofParts** 屬性中的 vector 元素應該在屬性集內的32位界限上對齊。 不過，在 **DocumentSummaryInformation** 和 **使用者** 配置的屬性集中，當屬性集的字碼頁不是 Unicode 時，必須封裝這些元素。

 

</dd> </dl>

您可以使用可設定的屬性集來保存 **任何屬性。** 通常，它是用來儲存使用者所建立的命名屬性。

 

 




