---
description: ICE15 會驗證 MIME 和延伸模組資料表中的內容類型和延伸模組參考是否互相反向。 MIME 資料表必須參考延伸模組資料表參考相同內容類型之延伸模組的內容類型。
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e5e54dedd2663a9f849abee43e244c73d7aa5835426be05d4e0163f599ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529308"
---
# <a name="ice15"></a>ICE15

ICE15 會驗證 [MIME](mime-table.md) 和 [延伸](extension-table.md) 模組資料表中的內容類型和延伸模組參考是否互相反向。 MIME 資料表必須參考延伸模組資料表參考相同內容類型之延伸模組的內容類型。

只要 MIME 型別參考回其中一個擴充功能，多個擴充功能就可以參考相同的 MIME 型別。 多個 MIME 類型可以參考相同的副檔名，只要副檔名參考回其中一個 MIME 類型即可。

請注意，每當 MIME 參考副檔名時，延伸模組資料表中的 MIME 資料行都不能 \_ 設為 Null。

## <a name="result"></a>結果

如果內容類型和延伸模組參考不是交互，ICE15 會張貼錯誤。

## <a name="example"></a>範例

ICE15 會針對所顯示的範例張貼兩則錯誤訊息：

-   MIME 資料表中的內容類型 test/x 翼參考了延伸模組 tst，但延伸模組表中的副檔名 tst 參考了翼翼/x 翼。 這不是交互。
-   內容類型的翼/x 翼參考延伸模組 flp，但延伸模組資料表的 MIME 資料行中有 Null 專案 \_ 。

[MIME 表格](mime-table.md) (部分) 



| ContentType   | 延伸模組\_ |
|---------------|-------------|
| 測試/x 測試   | Tst         |
| 翼翼/x 翼 | flp         |



 

[延伸模組資料表](extension-table.md) (部分) 



| 延伸模組 | MIME\_        |
|-----------|---------------|
| Tst       | 翼翼/x 翼 |
| flp       | Null          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



