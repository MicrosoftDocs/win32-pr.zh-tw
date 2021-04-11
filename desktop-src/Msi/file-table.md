---
description: File 資料表包含原始程式檔的完整清單及其各種屬性，以唯一、非當地語系化的識別碼進行排序。
ms.assetid: 31d0e727-a9eb-4cd2-a211-ea7b138d0173
title: FileTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59838001101bbc65af50bff3f2b00b540976e4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850927"
---
# <a name="file-table"></a>FileTable

File 資料表包含原始程式檔的完整清單及其各種屬性，以唯一、非當地語系化的識別碼進行排序。 檔案可以儲存在來源媒體上做為個別檔案，或壓縮在封 [*包*](c-gly.md)檔中。 如需詳細資訊，請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。

File 資料表具有下列資料行。



| Column      | 類型                               | 答案 | Nullable |
|-------------|------------------------------------|-----|----------|
| 檔案        | [識別碼](identifier.md)       | Y   | N        |
| 元件\_ | [識別碼](identifier.md)       | N   | N        |
| FileName    | [檔案名稱](filename.md)           | N   | N        |
| FileSize    | [DoubleInteger](doubleinteger.md) | N   | N        |
| 版本     | [版本](version.md)             | N   | Y        |
| 語言    | [Language](language.md)           | N   | Y        |
| 屬性  | [整數](integer.md)             | N   | Y        |
| 順序    | [整數](integer.md)             | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>檔
</dt> <dd>

可唯一識別檔案的非當地語系化標記。 此欄位不區分大小寫。 請勿將識別碼指派給不同大小寫不同的檔案。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。 此欄位會識別控制檔案的元件。

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>檔案名
</dt> <dd>

用於安裝的檔案名。 名稱可以當地語系化。

由於某些網頁伺服器可能會區分大小寫，因此檔案名應該完全符合原始程式檔的大小寫，以確保支援網際網路下載。

</dd> <dt>

<span id="FileSize"></span><span id="filesize"></span><span id="FILESIZE"></span>FileSize
</dt> <dd>

以位元組為單位的檔案大小。 此值必須是非負數。

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>版本
</dt> <dd>

此欄位是已建立版本之檔案的版本字串。 未建立版本的檔案的這個欄位是空白的。 在此欄位中輸入的檔案版本，必須與安裝套件隨附的檔案版本相同。

您也可以將 [版本] 欄位設定為包含檔案資料表中另一項記錄的主鍵。 參考的檔案接著會判斷這個檔案的版本控制邏輯。 如需詳細資訊，請參閱 [附屬](companion-files.md)檔案。 請注意，如果此檔案是其元件的金鑰路徑，則不得指定為附屬檔案。

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言
</dt> <dd>

以逗號分隔的十進位語言識別項清單。

字型檔案不能以語言識別項撰寫，因為字型沒有內嵌的語言識別項資源。 因此，字型檔案的此資料行應該保留 null。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

包含代表檔案屬性之位旗標的整數。

下表顯示位欄位的定義。



| 常數                             | 十六進位 | Decimal | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbFileAttributesReadOnly**      | 0x000001    | 1       | 唯讀                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **msidbFileAttributesHidden**        | 0x000002    | 2       | Hidden                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesSystem**        | 0x000004    | 4       | 系統                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **msidbFileAttributesVital**         | 0x000200    | 512     | 檔案對於其所屬元件的精確作業而言是很重要的。 如果安裝具有 msidbFileAttributesVital 屬性的檔案失敗，則會停止安裝並復原。 在此情況下，安裝程式會顯示沒有 [略過] 按鈕的對話方塊。 如果未設定此屬性，而且檔案安裝失敗，安裝程式會顯示具有 [略過] 按鈕的對話方塊。 在此情況下，使用者可以選擇忽略安裝檔案並繼續的失敗。 <br/> |
| **msidbFileAttributesChecksum**      | 0x000400    | 1024    | 檔案包含有效的總和 [*檢查*](c-gly.md)碼。 若要修復損毀的檔案，必須要有總和檢查碼。                                                                                                                                                                                                                                                                                                                                                                                           |
| **msidbFileAttributesPatchAdded**    | 0x001000    | 4096    | 只有在修補程式中新增檔案時，才必須加入此位。                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **msidbFileAttributesNoncompressed** | 0x002000    | 8192    | 檔案的來源類型為未壓縮。 如果設定，請忽略 [ [**字數統計摘要**](word-count-summary.md) ] 屬性。 如果未設定 **msidbFileAttributesNoncompressed** 或 **msidbFileAttributesCompressed** ，則檔案的壓縮狀態是由 [ **字數統計摘要** ] 屬性所指定。 請勿同時設定 **msidbFileAttributesNoncompressed** 和 **msidbFileAttributesCompressed**。                                                                                                                            |
| **msidbFileAttributesCompressed**    | 0x004000    | 16384   | 壓縮檔案的來源類型。 如果設定，請忽略 [ [**字數統計摘要**](word-count-summary.md) ] 屬性。 如果未設定 **msidbFileAttributesNoncompressed** 或 **msidbFileAttributesCompressed** ，則檔案的壓縮狀態是由 [ **字數統計摘要** ] 屬性所指定。 請勿同時設定 **msidbFileAttributesNoncompressed** 和 **msidbFileAttributesCompressed**。                                                                                                                              |



 

如果已設定 [屬性] 欄中的 **msidbFileAttributesVital** 位，而且已選取要安裝檔案所屬的元件，則安裝程式必須能夠安裝此檔案，才能順利完成安裝。 如果安裝程式因某些原因而無法安裝檔案 (例如，如果來源檔案無法在來源映射) 內，則會出現 [錯誤] 對話方塊，其中包含選項 [重試] 或 [取消]。 針對未設定 **msidbFileAttributesVital** 的檔案，在安裝錯誤時的選項將會是 [中止]、[重試] 和 [忽略] (也就是說，使用者可以選擇順利完成安裝，而不需要安裝該檔案) 。

您應該針對安裝中的每個可執行檔設定 **msidbFileAttributesChecksum** 位，其中具有儲存在可攜性可執行檔 (PE) 檔案標頭中的有效總和 [*檢查*](c-gly.md) 碼。 只有已設定此位的檔案會在重新安裝期間驗證是否有有效的總和檢查碼。 如需詳細資訊，請參閱 [**REINSTALLMODE**](reinstallmode.md)。

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列
</dt> <dd>

此檔案在媒體影像上的順序位置。 如果檔案已壓縮，此順序必須對應至封包中的檔案順序。 此欄位中的整數必須等於或大於1。

[順序] 資料行中的序號用來指定檔案的安裝順序，以及檔案所在的來源媒體 (與 [媒體資料表](media-table.md)) 搭配使用的順序。 例如，假設檔案的序號為92。 若要判斷此檔案所在的來源磁片，請查看媒體資料表中最小的最後一個序列值大於92的專案。

雖然壓縮檔案是在封包內指派內部序號，但是這些絕對數位不需要符合檔案資料表內的序號。 但是，檔案資料表中的檔案順序與封包內的檔案順序相同，是很重要的。

針對未壓縮的檔案，序號不需要是唯一的。 比方說，如果您的所有檔案都未壓縮，而且全部都位於一個磁片上，您可以為所有檔案提供相同的序號。

最大限制為32767個檔案。 若要建立具有更多檔案的 Windows Installer 封裝，請參閱 [撰寫大型封裝](authoring-a-large-package.md)。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [InstallFiles](installfiles-action.md)和 [RemoveFiles](removefiles-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

資料表一開始是從檔案清單產生的，但如果使用封包壓縮，則會從壓縮引擎的輸出重新產生資料表。 如需詳細資訊，請參閱封 [包](cabinet-files.md)檔。

若要在安裝期間移動使用者電腦上的現有檔案，請使用 [MoveFiles 動作](movefiles-action.md) 和 [MoveFile 資料表](movefile-table.md)。 若要將檔案安裝到多個位置，請使用 [DuplicateFiles 動作](duplicatefiles-action.md) 和 [DuplicateFile 資料表](duplicatefile-table.md)。

下表摘要說明 [版本] 資料行和 [語言] 資料行中的可能值組合。 如需詳細資訊，請參閱檔案 [版本控制規則](file-versioning-rules.md)。



| 版本 | Language | 描述                                                                     |
|---------|----------|---------------------------------------------------------------------------------|
| 1.2.3.4 | 1033     | 版本和語言。                                                       |
| 1.2.3.4 |  (Null)    | 版本，但不是語言。                                                    |
| 1.2.3.4 | 0        | 版本和語言是中立的。                                           |
| Testdb  |  (Null)    | 沒有相關聯語言的隨附檔案。                         |
| Testdb  | 1033     | 隨附的檔案和語言。                                                |
|  (Null)   | 1033     | 沒有任何版本，但有與其相關聯的語言 (也就是 typelib、功能説明) 。 |



 

如需詳細資訊，請參閱 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md) 和 [LockPermissions 資料表](lockpermissions-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE35](ice35.md)  
[ICE39](ice39.md)  
[ICE42](ice42.md)  
[ICE45](ice45.md)  
[ICE50](ice50.md)  
[ICE51](ice51.md)  
[ICE54](ice54.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE60](ice60.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE76](ice76.md)  
[ICE91](ice91.md)  
</dl>

 

 




