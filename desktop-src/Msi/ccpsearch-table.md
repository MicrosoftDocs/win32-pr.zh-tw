---
description: CCPSearch 資料表包含用於合規性檢查程式 (CCP) 的檔案簽章清單。 使用者的電腦上至少必須要有一個檔案，使用者才能符合該程式。
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: CCPSearch 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d20894960dce7f346601bd2ed459140caa305323ca02d14d54416f32737216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821838"
---
# <a name="ccpsearch-table"></a>CCPSearch 資料表

CCPSearch 資料表包含用於合規性檢查程式 (CCP) 的檔案簽章清單。 使用者的電腦上至少必須要有一個檔案，使用者才能符合該程式。

CCPSearch 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 簽名\_ | [識別碼](identifier.md) | Y   | N        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_
</dt> <dd>

簽章代表唯一的檔案簽章 \_ ，而且也是簽章、 [](signature-table.md) [RegLocator](reglocator-table.md)、 [IniLocator](inilocator-table.md)、 [CompLocator](complocator-table.md)和[DrLocator](drlocator-table.md)資料表中的外部金鑰。

</dd> </dl>

## <a name="remarks"></a>備註

當執行 [CCPSearch 動作](ccpsearch-action.md) 或 [RMCCPSearch 動作](rmccpsearch-action.md) 時，就會參考此資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



