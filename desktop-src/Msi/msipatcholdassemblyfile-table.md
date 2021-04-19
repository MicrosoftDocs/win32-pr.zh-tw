---
description: MsiPatchOldAssemblyFile 資料表會將 File 資料表中的檔案與 MsiPatchOldAssemblyName 資料表中的元件名稱產生關聯。 多個舊的元件名稱可以與單一檔案相關聯。
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: MsiPatchOldAssemblyFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992100"
---
# <a name="msipatcholdassemblyfile-table"></a>MsiPatchOldAssemblyFile 資料表

MsiPatchOldAssemblyFile 資料表會將 [file 資料表](file-table.md) 中的檔案與 [MsiPatchOldAssemblyName 資料表](msipatcholdassemblyname-table.md)中的元件名稱產生關聯。 多個舊的元件名稱可以與單一檔案相關聯。

MsiPatchOldAssemblyFile 資料表具有下列資料行。



| Column     | 類型                         | 答案 | Nullable |
|------------|------------------------------|-----|----------|
| 檔案\_     | [識別碼](identifier.md) | Y   | N        |
| 組件\_ | [識別碼](identifier.md) | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

檔案 [資料表](file-table.md) 的外鍵，可指定要修補的元件。 此資料行是主鍵的一部分。

</dd> <dt>

<span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>裝配\_
</dt> <dd>

[MsiPatchOldAssemblyName 資料表](msipatcholdassemblyname-table.md)的外鍵，可識別元件的其中一個舊元件名稱。 此資料行是主鍵的一部分。

</dd> </dl>

## <a name="remarks"></a>備註

Windows Installer 在修補安裝至全域組件快取 (GAC) 的元件時，會使用 MsiPatchOldAssemblyFile 資料表和 [MsiPatchOldAssemblyName 資料表](msipatcholdassemblyname-table.md) 。 發行元件的較新版本時，會變更元件的強式名稱。 這兩個數據表會一起識別已更新元件的舊元件名稱。 這可讓安裝程式使用舊的元件名稱來尋找 GAC 中的原始檔案，並套用二進位修補程式。 如果沒有此資訊，安裝程式可能必須存取原始安裝來源，才能修補安裝在 GAC 中的元件。

[PatchWiz](patchwiz-dll.md)不會自動產生 MsiPatchOldAssemblyFile 資料表和[MsiPatchOldAssemblyName 資料表](msipatcholdassemblyname-table.md)。 [UpgradedImages 資料表](upgradedimages-table-patchwiz-dll-.md)中指定的更新封裝必須包含這些資料表，修補程式才能擁有此資訊。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



