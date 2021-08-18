---
description: 延伸模組資料表包含必須在產品公告中產生的副檔名伺服器的相關資訊。 每個資料列都會產生一組登錄機碼和值。
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: 延伸模組資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d664df812b723d7ab6c9b966b09fac8c57a35b655e123f720fdb87bdf431146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821738"
---
# <a name="extension-table"></a>延伸模組資料表

延伸模組資料表包含必須在產品公告中產生的副檔名伺服器的相關資訊。 每個資料列都會產生一組登錄機碼和值。

延伸模組資料表包含下表所示的資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 延伸模組   | [Text](text.md)             | Y   | N        |
| 元件\_ | [識別碼](identifier.md) | Y   | N        |
| ProgId\_    | [Text](text.md)             | N   | Y        |
| MIME\_      | [Text](text.md)             | N   | Y        |
| 特徵\_   | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>擴展
</dt> <dd>

與資料表資料列相關聯的延伸模組。 延伸模組的長度最多可達255個字元。 在此欄位中輸入延伸模組，但不含前置句點。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

[元件](component-table.md)資料表第一個資料行的外部索引鍵。 此資料行參考控制延伸模組安裝的元件。

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_
</dt> <dd>

與此延伸模組相關聯的程式識別碼。 這是 [ProgId](progid-table.md) 資料表中的外鍵。

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>MIME\_
</dt> <dd>

要為延伸模組資料行撰寫的內容類型。

[MIME](mime-table.md)資料表第一個資料行的外部索引鍵。

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_
</dt> <dd>

在 [功能](feature-table.md) 資料表的第一個資料行中，指定提供延伸模組伺服器之功能的外部索引鍵。

</dd> </dl>

## <a name="remarks"></a>備註

執行 [RegisterExtensionInfo](registerextensioninfo-action.md) 動作或 [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) 動作時，會參考延伸模組資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE69](ice69.md)  
</dl>

 

 



