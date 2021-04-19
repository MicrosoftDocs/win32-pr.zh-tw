---
description: ModuleComponents 資料表包含在合併模組中找到的元件清單。
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: ModuleComponents 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981199"
---
# <a name="modulecomponents-table"></a>ModuleComponents 資料表

ModuleComponents 資料表包含在合併模組中找到的元件清單。

ModuleComponents 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 元件 | [識別碼](identifier.md) | Y   | N        |
| ModuleID  | [識別碼](identifier.md) | Y   | N        |
| 語言  | [整數](integer.md)       | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>元件
</dt> <dd>

參考合併模組中元件的識別碼。 元件資料行是 [元件資料表](component-table.md)的外鍵。 元件資料行中的專案必須遵循命名慣例，以 [命名合併模組資料庫中的主鍵](naming-primary-keys-in-merge-module-databases.md)。

</dd> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

合併模組的識別碼。 這是 [ModuleSignature 資料表](modulesignature-table.md)的外鍵。

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言
</dt> <dd>

語言識別項描述合併模組的預設語言。 語言識別項採用十進位格式，例如，美國英文為1033。 [ModuleSignature 資料表](modulesignature-table.md)的外鍵。

</dd> </dl>

## <a name="remarks"></a>備註

如果合併模組支援多種語言，則語言轉換必須能夠更新此資料表。

 

 



