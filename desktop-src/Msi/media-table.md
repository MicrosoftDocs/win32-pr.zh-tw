---
description: 媒體資料表描述組成安裝來源媒體的磁片集。
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: 媒體資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29939553e64fb6558aa6480fb69b7beab208a4ccb3e2c9ce55c4d8fcbfc18cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805093"
---
# <a name="media-table"></a>媒體資料表

媒體資料表描述組成安裝來源媒體的磁片集。

媒體資料表包含下表所示的資料行。



| Column       | 類型                     | 答案 | Nullable |
|--------------|--------------------------|-----|----------|
| DiskId       | [整數](integer.md)   | Y   | N        |
| LastSequence | [整數](integer.md)   | N   | N        |
| DiskPrompt   | [Text](text.md)         | N   | Y        |
| 內閣      | [內閣](cabinet.md)   | N   | Y        |
| VolumeLabel  | [Text](text.md)         | N   | Y        |
| 來源       | [屬性](property.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId
</dt> <dd>

決定資料表的排序次序。 此數位必須等於或大於1。

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

此媒體之最後一個檔案的檔案序號。 LastSequence 資料行中的數位會指定 [檔案資料表中的哪些](file-table.md) 檔案是在特定的來源磁片上找到。 每個來源磁片都包含序號 (的所有檔案，如 [檔案] 資料表的 [順序] 資料行中所示) 小於或等於 [LastSequence] 資料行中的值，以及大於前一個磁片 (或大於0的 LastSequence 值（針對媒體資料表) 中的第一個專案）。 此數位必須為非負數;最大限制為32767個檔案。 如需有關使用更多檔案建立 Windows Installer 套件的詳細資訊，請參閱[撰寫大型封裝](authoring-a-large-package.md)。

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

磁片名稱，通常是列印在磁片上的可見文字。 這個可當地語系化的文字是用來在需要插入磁片時提示使用者。

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>內閣
</dt> <dd>

如果儲存在媒體上的部分或所有檔案壓縮成封包檔，則為封包的名稱。 如果未使用任何封包，則此資料行必須為空白。 封包的名稱必須使用封 [包](cabinet.md) 資料類型的語法。 Windows安裝程式一律需要有效的來源，才能修復內嵌封包檔中包含的檔案。 當 Windows Installer 安裝包含內嵌封包檔的封裝時，系統會儲存封包檔的複本。 此複本無法用來修復封包檔。 若要節省磁碟空間，請使用外部封包檔，而不是內嵌的封包檔。

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

屬於磁片區的標籤。 這是 [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) 函式所傳回的磁片區標籤。 如果 [**SourceDir**](sourcedir.md) 內容參考可移動 (磁片或 cd-rom) 磁片區，則會使用此磁片區標籤來確認磁片磁碟機中是否有適當的磁片，然後再嘗試安裝檔案。 此資料行中的專案必須符合實體媒體的磁片區標籤。

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>源
</dt> <dd>

此欄位僅供修補使用，否則會保留空白。 修補程式轉換可以在這裡輸入內容，這是包含修補檔案的封包檔的位置，或修補程式所加入的任何新檔案。 您必須為這些檔案指定不同的來源，因為修補套件的來源可以與產品的來源分開儲存。 如果 [封包] 欄位是空的，安裝程式會忽略此資料行中的值。 如果這個欄位是空的，安裝程式會使用 [**SourceDir**](sourcedir.md) 屬性的值做為封包的來源。

</dd> </dl>

## <a name="remarks"></a>備註

如果封包名稱前面加上數位記號 (\#) ，則參考此媒體資料表記錄的檔案會封裝在以個別資料流程形式儲存在資料庫中的封包檔中。

如需如何將封包新增至檔案資料表和媒體資料表的詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。

Windows安裝程式要求 .msi 檔案必須位於卸載式媒體的第一個磁片上， (CD、DVD 或磁片) 用於產品的安裝。

**判斷 SourceMode**

[ [**字數統計摘要**](word-count-summary.md) ] 屬性會決定目前安裝的來源模式。 如果這個屬性設定為2或3，則會假設為封包安裝。 在此模式中，會假設封包檔存在於 [**SourceDir**](sourcedir.md) 屬性所指示的目錄中。 如果來源類型值為0或1，則會假設所有原始程式檔都存在於樹狀結構中，其根目錄會以 **SourceDir** 屬性工作表示。

請注意，這只適用于檔案資料表中，未在 [屬性] 資料行中設定壓縮或未壓縮位的檔案。 判斷特定檔案是否已壓縮或未壓縮時，這些位會覆寫 [ [**字數統計摘要**](word-count-summary.md) ] 屬性的值。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE35](ice35.md)  
[ICE58](ice58.md)  
[ICE71](ice71.md)  
[ICE81](ice81.md)  
</dl>

 

 
