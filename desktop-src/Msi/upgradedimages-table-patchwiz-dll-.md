---
description: UpgradedImages 資料表包含產品升級後影像的相關資訊。
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: 'UpgradedImages 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320559"
---
# <a name="upgradedimages-table-patchwizdll"></a>UpgradedImages 資料表 (Patchwiz.dll) 

UpgradedImages 資料表包含產品升級後影像的相關資訊。 升級的映射應該是產品最新版本的完全未壓縮安裝映射，例如，系統管理映射或 CD-ROM 的未壓縮安裝映射。 Windows Installer 修補程式套件會將目標映射更新為升級的映射。 UpgradedImages 資料表在 patch 建立資料庫中是必要的， (. pcp 檔案) 並由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)使用。

在每個修補程式建立資料庫中都必須包含至少一筆記錄的 UpgradedImages 資料表， ( pcp 檔案) 。 此資料表是由 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)所使用。

UpgradedImages 資料表具有下列資料行。



| Column       | 類型 | 答案 | Nullable |
|--------------|------|-----|----------|
| 已升級     | text | Y   | N        |
| MsiPath      | text |     | N        |
| PatchMsiPath | text |     | Y        |
| SymbolPaths  | text |     | Y        |
| 系列       | text |     | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>升級
</dt> <dd>

升級的欄位是任意的識別碼，可將目標映射連接到產品的升級映射。

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

此欄位會指定檔案的完整路徑（包括檔案名）至已升級之映射的 .msi 檔案位置。 這是已升級映射之來源檔案的位置。

</dd> <dt>

<span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath
</dt> <dd>

選擇性的 patchMsiPath 會指向已升級安裝資料庫的已修改複本，其中包含修補程式安裝程式的其他專屬撰寫。 例如，在 [**PATCH**](patch.md) 屬性上有條件的其他對話或自訂動作。

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

以分號分隔的資料夾清單，這些資料夾是要搜尋的符號檔，可用於優化二進位修補程式的產生。 請注意，不會搜尋此欄位中指定的資料夾子目錄。 優化的二進位修補程式可能較小。 Visual C++ 必須安裝在產生修補程式的電腦上，並用來建立符號檔。 這個欄位是選擇性欄位，即使未指定符號檔或符號檔無法 Patchwiz.dll，安裝程式還是會建立二進位修補程式。

</dd> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>家庭
</dt> <dd>

[ImageFamilies 資料表](imagefamilies-table-patchwiz-dll-.md)中的外鍵。 每個升級的映射都只能屬於一個系列。

</dd> </dl>

## <a name="remarks"></a>備註

雖然每個升級的映射都可以分組為不同的映射系列，但是將共用檔案的已升級影像群組在一起，可能會使 .msp 變得較小。

此資料表接受環境變數作為從4.0 版 Patchwiz.dll 開始的路徑。

 

 



