---
description: 動詞資料表包含與副檔名相關的命令動詞資訊，必須在產品公告中產生。 每個資料列都會產生一組登錄機碼和值。
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: 動詞資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976606"
---
# <a name="verb-table"></a>動詞資料表

動詞資料表包含與副檔名相關的命令動詞資訊，必須在產品公告中產生。 每個資料列都會產生一組登錄機碼和值。

動詞資料表具有下列資料行。



| Column      | 類型                       | 答案 | Nullable |
|-------------|----------------------------|-----|----------|
| 分機\_ | [Text](text.md)           | Y   | N        |
| 動詞命令        | [Text](text.md)           | Y   | N        |
| 順序    | [整數](integer.md)     | N   | Y        |
| Command     | [格式 化](formatted.md) | N   | Y        |
| 引數    | [格式 化](formatted.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>擴展\_
</dt> <dd>

與資料表資料列相關聯的延伸模組。 此資料行是 [延伸模組資料表](extension-table.md)第一個資料行的外部索引鍵。

</dd> <dt>

<span id="Verb"></span><span id="verb"></span><span id="VERB"></span>動詞
</dt> <dd>

命令的動詞。

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列
</dt> <dd>

命令的順序。 只有順序資料行為非 Null 的動詞，才能用來準備 shell 索引鍵的預設值的排序清單。 此資料行中具有最低值的動詞會成為預設動詞。

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>命令
</dt> <dd>

顯示在內容功能表上的可當地語系化文字。

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>參數
</dt> <dd>

命令引數的值。

請注意，[引數] 欄位中的屬性解析有限。 \[  \] 只有在已安裝擁有動詞的元件時，如果屬性已經有預期的值，就可以解析此欄位中格式化為屬性的屬性。 例如，若要將引數 " \[ \#MyDoc.doc\] " 解析為正確的值，則相同的進程必須安裝 MyDoc.doc 以及擁有該動詞命令的元件。

</dd> </dl>

## <a name="remarks"></a>備註

當執行 [RegisterExtensionInfo 動作](registerextensioninfo-action.md) 或 [UnregisterExtensionInfo 動作](unregisterextensioninfo-action.md) 時，就會參考此資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



