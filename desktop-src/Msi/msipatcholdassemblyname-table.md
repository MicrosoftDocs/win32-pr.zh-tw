---
description: MsiPatchOldAssemblyName 資料表會指定元件的舊名稱。
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: MsiPatchOldAssemblyName 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319915"
---
# <a name="msipatcholdassemblyname-table"></a>MsiPatchOldAssemblyName 資料表

MsiPatchOldAssemblyName 資料表會指定元件的舊名稱。

MsiPatchOldAssemblyName 資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| 組件 | [識別碼](identifier.md) | Y   | N        |
| Name     | [Text](text.md)             | Y   | N        |
| 值    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>裝配
</dt> <dd>

舊元件名稱的唯一識別碼。 此索引鍵是用來做為此與 [MsiPatchOldAssemblyFile 資料表](msipatcholdassemblyfile-table.md)之間的對應。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

與 [值] 資料行中指定的值相關聯之屬性的名稱。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

與 [名稱] 資料行中指定之名稱相關聯的值。

</dd> </dl>

## <a name="remarks"></a>備註

Windows Installer 在修補安裝至全域組件快取 (GAC) 的元件時，會使用 [MsiPatchOldAssemblyFile 資料表](msipatcholdassemblyfile-table.md) 和 MsiPatchOldAssemblyName 資料表。 發行元件的較新版本時，會變更元件的強式名稱。 這兩個數據表會一起識別已更新元件的舊元件名稱。 這可讓安裝程式使用舊的元件名稱來尋找 GAC 中的原始檔案，並套用二進位修補程式。 如果沒有此資訊，安裝程式可能必須存取原始安裝來源，才能修補安裝在 GAC 中的元件。

[PatchWiz](patchwiz-dll.md)不會自動產生[MsiPatchOldAssemblyFile 資料表](msipatcholdassemblyfile-table.md)和 MsiPatchOldAssemblyName 資料表。 [UpgradedImages 資料表](upgradedimages-table-patchwiz-dll-.md)中指定的更新封裝必須包含這些資料表，修補程式才能擁有此資訊。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



