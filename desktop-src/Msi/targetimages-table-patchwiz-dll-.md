---
description: TargetImages 資料表包含產品目標影像的相關資訊。 Windows Installer 修補程式套件會將目標映射更新為升級的映射。
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: 'TargetImages 資料表 (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec35a9090f89e93e807cda9429ae48d8cc28d175acc4c83e97150e3a98ce5fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893588"
---
# <a name="targetimages-table-patchwizdll"></a>TargetImages 資料表 (Patchwiz.dll) 

TargetImages 資料表包含產品目標影像的相關資訊。 Windows Installer 修補程式套件會將目標映射更新為升級的映射。

在每個修補程式建立資料庫中都必須包含至少一筆記錄的 TargetImages 資料表， ( pcp 檔案) 。 此資料表是由 [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 函數所使用。

TargetImages 資料表具有下列資料行。



| Column                | 類型    | 答案 | Nullable |
|-----------------------|---------|-----|----------|
| 目標                | text    | Y   | N        |
| MsiPath               | text    |     | N        |
| SymbolPaths           | text    |     | Y        |
| 已升級              | text    |     | N        |
| 單                 | 整數 |     | N        |
| ProductValidateFlags  | text    |     | Y        |
| IgnoreMissingSrcFiles | 整數 |     | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標
</dt> <dd>

目標映射的識別碼。 修補程式套件會將此資料行中指定的目標映射更新為升級的資料行中所指定的升級映射。 每個升級的映射都有一個或多個目標映射。 目標映射必須是產品的完全未壓縮安裝映射，例如 CD-ROM 上的系統管理映射或未壓縮的安裝映射。 請注意， [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) 函數不會為封包中的檔案產生二進位修補程式。 此欄位中的值會與 [已升級] 欄位中的值搭配使用，以產生安裝程式新增至 patch 封裝的轉換名稱。

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

此欄位會指定目標映射的 .msi 檔案位置的完整路徑（包括檔案名）。 這是目標映射的來源檔案位置。

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

以分號分隔的資料夾清單，這些資料夾是要搜尋的符號檔，可用於優化二進位修補程式的產生。 請注意，不會搜尋此欄位中指定的資料夾子目錄。 優化的二進位修補程式可能較小。 Microsoft Visual C++ 必須安裝在產生修補程式的電腦上，並用來建立符號檔。 這個欄位是選擇性欄位，即使未指定符號檔或符號檔無法 Patchwiz.dll，安裝程式還是會建立二進位修補程式。

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>升級
</dt> <dd>

[UpgradedImages 資料表](upgradedimages-table-patchwiz-dll-.md)的升級資料行外鍵。 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)函式會忽略至少一個 TargetImages 資料表記錄未參考的已升級影像。

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>以
</dt> <dd>

目標影像的相對順序。 因為多個目標可以修補為升級的映射，所以 [順序] 欄位提供在 [修補程式轉換] 清單中排序轉換的方法。 通常，順序是從最舊到最新的影像。

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags
</dt> <dd>

ProductValidateFlags 欄位是用來指定產品檢查，以避免套用不相關的轉換。 在此欄位中輸入的值必須是8位數的十六進位整數，以及 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)函數之 *iValidation* 參數的其中一個有效值。 預設值為0x00000922，等於 **MSITRANSFORM \_ validate \_ UPDATEVERSION**  +  **MSITRANSFORM \_ validate \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ validate \_ UPGRADECODE**  +  **MSITRANSFORM \_ validate \_ PRODUCT**。

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles
</dt> <dd>

如果此欄位設定為非零值，則安裝程式會忽略目標映射中遺失的檔案，並在修補期間保持不變。 這可讓您在不需要整個映射的情況下進行修補;只有已變更的產品和 .msi 檔案的檔案是必要的。 這可能會減少產生修補程式所需的時間。

> [!Note]  
> 請勿在 [Properties 資料表](properties-table-patchwiz-dll-.md)中使用 IgnoreMissingSrcFiles 值，並將 TrustMsi 設定為1。

 

</dd> </dl>

## <a name="remarks"></a>備註

此資料表接受環境變數作為從4.0 版 Patchwiz.dll 開始的路徑。

 

 



