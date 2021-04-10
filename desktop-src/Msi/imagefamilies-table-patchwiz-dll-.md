---
description: 映射家族是已更新為最新版本之產品的一或多個已升級映射的群組。
ms.assetid: 06a77b35-b593-47e6-9083-46a6b65b7481
title: 'ImageFamilies 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ece99e3c42626eb2155f16f2198703dc31b682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943717"
---
# <a name="imagefamilies-table-patchwizdll"></a>ImageFamilies 資料表 (Patchwiz.dll) 

映射家族是已更新為最新版本之產品的一或多個已升級映射的群組。 每個升級的映射只能屬於一個系列。 屬於映射系列的已升級映射會共用一或多個檔案。 每個映射系列在 .msp 檔中都有自己的封包檔，其中包含更新目標和升級檔案之間差異所需的二進位修補程式和新檔案。 封包檔不會複寫共用檔案所使用的二進位修補程式和新檔案。

在每個修補程式建立資料庫中都必須包含至少一筆記錄的 ImageFamilies 資料表， ( pcp 檔案) 。 此資料表是由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數所使用。

ImageFamilies 資料表包含要新增至 [媒體資料表](media-table.md)的修補資訊。 修補程式會將一個專案新增至媒體資料表。 ImageFamilies 資料表中的每一筆記錄都會參考一組已更新為最新產品版本的相關產品影像。

ImageFamilies 資料表具有下列資料行。 如果 MediaSrcPropName、MediaDiskId 和 FileSequenceStart 資料行套用修補程式與 Windows Installer 和 Patchwiz.dll 2.0 版，則可以在、和資料行中使用 null 值。



| Column            | 類型    | 答案 | Nullable |
|-------------------|---------|-----|----------|
| 系列            | text    | Y   | N        |
| MediaSrcPropName  | text    |     | Y        |
| MediaDiskId       | 整數 |     | Y        |
| FileSequenceStart | 整數 |     | Y        |
| DiskPrompt        | text    |     | Y        |
| VolumeLabel       | text    |     | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>家庭
</dt> <dd>

在此欄位中輸入的值是已更新為產品最新版本之相關產品影像群組的識別碼。 限制為總共8個英數位元或底線。 安裝程式會在 Windows Installer 修補檔中，為數據表中的每個系列內嵌一個封包資料流程 ( .msp 檔) 。 此封包包含二進位修補程式，以及將目標映射更新為產品的升級映射時所需的新檔案。 安裝程式會在 PCW CAB 的系列名稱前加上前置詞， \_ \_ 以產生封包在新 [媒體資料表](media-table.md) 專案的 [封包] 欄位中輸入的資料流程名稱。

</dd> <dt>

<span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>MediaSrcPropName
</dt> <dd>

在已升級影像的新 [媒體資料表](media-table.md) 專案的 [來源] 欄位中輸入的值。 只有當您使用2.0 版的 Patchwiz.dll，以及屬性工作表中的 MinimumRequiredMsiVersion [ (Patchwiz.dll) ](properties-table-patchwiz-dll-.md) 設定為200時，此欄位才可以是 null。

</dd> <dt>

<span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>MediaDiskId
</dt> <dd>

安裝程式會在新的 [媒體資料表](media-table.md) 記錄的 DiskId 欄位中輸入此值。 DiskID 值必須大於目標套件中的任何目前 DiskID。 MediaDiskId 的限制為32767。 只有當您使用2.0 版的 Patchwiz.dll，以及屬性工作表中的 MinimumRequiredMsiVersion [ (Patchwiz.dll) ](properties-table-patchwiz-dll-.md) 設定為200時，此欄位才可以是 null。

</dd> <dt>

<span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>FileSequenceStart
</dt> <dd>

此欄位是起始檔案的序號。 相同產品的兩個修補程式中不能有相同的檔案序號。 為確保這一點，此欄位中的值必須大於先前修補或原始安裝套件中使用的所有序號。 您可以藉由將修補程式封包檔中的專案總數新增至該修補程式的 FileSequenceStart 號碼，來判斷修補程式中的最大序號。 判斷這一點的其中一種方式，是查看在建立修補程式期間 [Patchwiz.dll](patchwiz-dll.md) 所產生的 ddf 檔案。 FileSequenceStart 的限制為32767。 只有當您使用2.0 版的 Patchwiz.dll，以及屬性工作表中的 MinimumRequiredMsiVersion [ (Patchwiz.dll) ](properties-table-patchwiz-dll-.md) 設定為200時，此欄位才可以是 null。

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

安裝程式會在新的 [媒體資料表](media-table.md) 記錄的 DiskPrompt 欄位中輸入此值。

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

安裝程式會在新媒體記錄的 VolumeLabel 欄位中輸入此值。

</dd> </dl>

## <a name="remarks"></a>備註

修補程式會將 .msp 檔中的封包名稱新增至新增至 [媒體資料表](media-table.md)的新記錄的 [封包] 欄位中。 因為它是內嵌的封包，所以名稱前面會加上 ' \# ' 字元。 修補程式會將屬性新增至媒體資料表中新記錄的來源欄位。 沒有兩個修補程式可能具有相同的來源屬性。

在映射系列內共用的檔案，在每個升級的系列映射中都必須具有相同的檔案資料表索引鍵。 在升級的映射之間共用的任何檔案資料表索引鍵都必須代表相同的檔案，而且在所有升級的映射中都必須相同。 File 資料表索引鍵是在 [file 資料表](file-table.md)的 file 資料行中輸入的值。

MediaDiskId 和 FileSequenceStart 的限制為32767。 若要增加此限制，請使用 [Msidb.exe](msidb-exe.md) 將 ImageFamilies 資料表匯出至 idt 檔案，並將資料行類型從 i2 變更為 i4，或從 i2 變更為 i4，然後將 idt 檔案匯回 pcp 資料庫。 無法在具有不同資料行類型的兩個封裝之間建立轉換和修補程式。

 

 



