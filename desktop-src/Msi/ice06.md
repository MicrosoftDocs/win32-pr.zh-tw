---
description: ICE06 會檢查每個資料表，以驗證驗證資料表中所列的所有資料行 \_ 都存在於資料表中。 如果資料表不存在， \_ 則會忽略該資料表的任何驗證專案。
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: febccd205b78e90d3dac49f88d0750f803c8cd575b6b76b46cab79a684deea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142566"
---
# <a name="ice06"></a>ICE06

ICE06 會檢查每個資料表，以驗證[ \_ 驗證資料表](-validation-table.md)中所列的所有資料行都存在於資料表中。 如果資料表不存在， \_ 則會忽略該資料表的任何驗證專案。

ICE06 的目的是要偵測作者嘗試使用新的 \_ 驗證資料表的實例，該資料表會反映具有尚未更新之舊資料庫的架構變更。 ICE06 也會偵測與已改變的資料庫搭配使用之舊驗證資料表的反向案例 \_ 。

請注意， [ICE03](ice03.md) 執行的內部驗證會攔截未在資料 \_ 行目錄中列出的驗證資料表中定義的資料表資料行實例。 因此，使用 ICE03 和 ICE06，可確保資料庫中的每個資料行都經過測試。

## <a name="result"></a>結果

當驗證資料表中定義的資料表資料行 \_ 未列于 Columns 資料表中時，ICE06 會張貼錯誤 \_ 。

## <a name="example"></a>範例

下列範例 ICE06 會張貼訊息

資料行：資料表的版本： ModuleSignature 未定義于資料庫中。

[ \_ 驗證資料表](-validation-table.md) (部分) 



| 資料表           | 資料行   |
|-----------------|----------|
| ModuleSignature | ModuleID |
| ModuleSignature | 版本  |



 

[ \_ Columns 資料表](-columns-table.md) (部分) 



| 資料表           | 數字 | 名稱     |
|-----------------|--------|----------|
| ModuleSignature | 1      | ModuleID |



 

ModuleSignature 資料表的 [版本] 資料行不在資料庫中，或在 [資料行] 資料表中列出 \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



