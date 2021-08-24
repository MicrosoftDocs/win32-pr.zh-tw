---
description: 自訂動作可以呼叫以 VBScript 或 JScript 撰寫的函式。
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: 指令碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af49e1863d43956e8ec799e467d8391873458d1879f78455abda9ee06fb739aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041368"
---
# <a name="scripts"></a>指令碼

自訂動作可以呼叫以 VBScript 或 JScript 撰寫的函式。 Windows安裝程式未提供腳本引擎。 因此，想要在安裝期間利用指令碼語言的作者，必須確保適當的腳本引擎可以使用。

安裝程式不支援 JScript 1.0 版。

以腳本為基礎的64位自訂動作必須明確標記為64位自訂動作，方法是在 [CustomAction](customaction-table.md)資料表的類型資料行中，將 **msidbCustomActionType64BitScript** 位新增至自訂動作數數值型別。 如需詳細資訊，請參閱 [64 位自訂動作](64-bit-custom-actions.md)。

下列基本自訂動作類型會呼叫以腳本撰寫的函式。



| 自訂動作類型                                 | 描述                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [自訂動作類型5](custom-action-type-5.md)   | JScript 儲存在二進位資料表資料流程中的檔案。                                                  |
| [自訂動作類型21](custom-action-type-21.md) | 隨產品安裝的 JScript 檔案。                                                 |
| [自訂動作類型53](custom-action-type-53.md) | JScript 屬性值所指定的文字。                                                    |
| [自訂動作類型37](custom-action-type-37.md) | JScript 儲存在[CustomAction](customaction-table.md)資料表的目標資料行中的文字。  |
| [自訂動作類型6](custom-action-type-6.md)   | 儲存在 [二進位](binary-table.md) 資料表資料流程中的 VBScript 檔案。                             |
| [自訂動作類型22](custom-action-type-22.md) | 隨產品安裝的 VBScript 檔案。                                                |
| [自訂動作類型54](custom-action-type-54.md) | 由屬性值指定的 VBScript 文字。                                                   |
| [自訂動作類型38](custom-action-type-38.md) | [CustomAction](customaction-table.md)資料表的目標資料行中所儲存的 VBScript 文字。 |



 

> [!Note]  
> 安裝程式會直接執行腳本自訂動作，而不會使用 Windows 腳本主機。 **wscript.echo** 物件不能用在腳本自訂動作內，因為此物件是由 Windows 腳本主機提供。 只有在電腦上安裝了 Windows 腳本主機時，才可以在自訂動作中使用 Windows 腳本主機物件模型中的物件，方法是使用 CreateObject 的呼叫來建立物件的新實例，並提供物件的 ProgId (例如 "wscript.echo. Shell" ) 。 根據腳本的自訂動作類型而定，基於安全性考慮，可能會拒絕存取 Windows 腳本主機物件模型的某些物件和方法。

 

如需詳細資訊，請參閱所有自訂動作 [類型的摘要清單](summary-list-of-all-custom-action-types.md) ，以取得所有自訂動作類型的摘要，以及它們如何編碼至 [CustomAction](customaction-table.md) 資料表。

 

 



