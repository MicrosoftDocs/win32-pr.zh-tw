---
description: 佈告欄資料表列出完整使用者介面中顯示的佈告欄控制項。
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: 佈告欄資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944000"
---
# <a name="billboard-table"></a>佈告欄資料表

佈告欄資料表列出完整使用者介面中顯示的 [佈告欄控制項](billboard-control.md) 。

佈告欄資料表有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 廣告 牌 | [識別碼](identifier.md) | Y   | N        |
| 功能\_ | [識別碼](identifier.md) | N   | N        |
| 動作    | [識別碼](identifier.md) | N   | Y        |
| 排序  | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>廣告 牌
</dt> <dd>

[佈告欄控制項](billboard-control.md)的名稱。

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_
</dt> <dd>

[功能資料表](feature-table.md)第一個資料行的外部索引鍵。 只有在安裝這項功能時，才會顯示此佈告欄。

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

動作的名稱。 這個佈告欄會在從此動作收到的進度訊息期間顯示。

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>訂購
</dt> <dd>

如果有一個以上的佈告欄對應到某個動作，則會依此資料行所定義的順序來顯示。 此數位必須為非負數。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



