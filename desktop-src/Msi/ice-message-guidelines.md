---
description: ICE 自訂動作會藉由呼叫 MsiProcessMessage 和張貼 INSTALLMESSAGE \_ 使用者類型訊息來進行通訊。
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: ICE 訊息指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d603175dbecc12b0b9524db1a02d9ca677f61c87
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887445"
---
# <a name="ice-message-guidelines"></a>ICE 訊息指導方針

ICE 自訂動作會藉由呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 和張貼 INSTALLMESSAGE \_ 使用者類型訊息來進行通訊。

撰寫 ICE 自訂動作的訊息字串時，請將字串格式化，如下所示。

*ICE* &lt; 的名稱索引標籤訊息類型索引標籤描述索引標籤 &gt;  &lt; &gt; *說明* &lt; &gt; *URL 或位置* 索引標籤的 &lt; &gt; *資料表名稱* &lt; &gt;  &lt; &gt;  &lt; &gt;  &lt; &gt; 索引標籤主鍵索引標籤主要索引標籤主要索引鍵 . .  (視需要針對多個主要金鑰重複執行) 

每個訊息中都需要字串的前三個欄位。

[訊息類型] 欄位會指定 ICE 是否報告失敗、錯誤、警告或告知性訊息。



| 值 | 訊息類型                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 報告 ICE 自訂動作失敗的失敗訊息。                                                                                                       |
| 1     | 導致不正確行為的錯誤訊息報告資料庫撰寫。                                                                                             |
| 2     | 在某些情況下導致不正確行為的警告訊息報告資料庫撰寫。 警告也可以報告資料庫撰寫的非預期副作用。 |
| 3     | 參考資訊。                                                                                                                                                |



 

如果無法使用 [說明]，[說明 URL] 欄位可能是空字串。

錯誤和警告訊息應該提供資料表名稱、資料行名稱和主要索引鍵欄位。 如果省略這些欄位中的任何欄位，則在第一個空白欄位之後的所有欄位都必須留出訊息。 例如，提供的資料表名稱沒有資料行名稱和主鍵或資料表名稱，而且沒有主鍵的資料行名稱。 不過，資料行名稱和主鍵不能在沒有資料表名稱的情況下使用。 在該資料表中的所有主鍵都已指定值之前，可能會列出多個主要索引鍵。

## <a name="examples"></a>範例

[C + + 中範例 ICE](sample-ice-in-c-.md)所說明的第一則訊息：

"ICE01 \\ t3 \\ t 已建立 04/29/1998 by <在此處插入作者名稱>。

範例 ICE 所公佈的第二個訊息：

「ICE01 \\ t3 \\ tLast 修改了05/06/1999，<在此處插入作者的名稱>。」

範例 ICE 所公佈的第三個訊息。

「ICE01 \\ t3 \\ tSimple 冰以說明霜淇淋概念」。

 

 



