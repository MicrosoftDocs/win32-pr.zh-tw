---
description: RemoveRegistry 資料表包含應用程式需要從系統登錄刪除的登錄資訊。
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: RemoveRegistry 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170dc727eef47ac214f7a7f42af7f487f53ad0b9a0658182420b28eb5224e38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314878"
---
# <a name="removeregistry-table"></a>RemoveRegistry 資料表

RemoveRegistry 資料表包含應用程式需要從系統登錄刪除的登錄資訊。

RemoveRegistry 資料表具有下列資料行。



| Column         | 類型                         | 答案 | Nullable |
|----------------|------------------------------|-----|----------|
| RemoveRegistry | [識別碼](identifier.md) | Y   | N        |
| Root           | [整數](integer.md)       | N   | N        |
| 答案            | [RegPath](regpath.md)       | N   | N        |
| Name           | [格式 化](formatted.md)   | N   | Y        |
| 元件\_    | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry
</dt> <dd>

此資料表的索引鍵。

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>根
</dt> <dd>

登錄值的預先定義根金鑰。



| 常數                          | 十六進位 | Decimal | 根金鑰                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (無)                            | \- 0x001    | -1      | **HKEY \_目前的 \_ 使用者** 安裝程式會在執行每個使用者安裝時設定此機碼。<br/>                                                                                                                    |
| (無)                            | -0x001      | -1      | **HKEY \_本機 \_ 電腦** 安裝程式會在執行所有使用者安裝時設定此機碼，並將 [**ALLUSERS**](allusers.md) 設定為1。<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_類別 \_ 根目錄** 安裝程式會在每位使用者和每部電腦的 [安裝內容](installation-context.md)中，從 **HKCU \\ Software \\** class hive 移除值。<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ 目前的 \_ 使用者**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ 本機 \_ 電腦**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **HKEY \_ 使用者**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵
</dt> <dd>

登錄值的可當地語系化金鑰。

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

可當地語系化的登錄值名稱。

[名稱] 資料行中的下列字串具有特殊意義。



| String | 意義                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | 安裝元件時，將會刪除金鑰（如果有的話）及其所有值和子機碼。 |



 

請注意，移除元件時，應該使用登錄 [資料表](registry-table.md) 來建立或移除登錄機碼。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md) 的第一個資料行中，外部索引鍵參考控制登錄值刪除的元件。

</dd> </dl>

## <a name="remarks"></a>備註

當已選取要在本機安裝或從來源執行的對應元件時，系統會從系統登錄刪除登錄資訊。

當 [RemoveRegistryValues 動作](removeregistryvalues-action.md) 執行時，就會參考此資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




