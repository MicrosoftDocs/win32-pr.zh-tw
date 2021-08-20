---
description: 本主題會識別您可用來控制自訂動作執行緒的選項旗標。
ms.assetid: a09b3a0e-564e-41aa-af0d-2e46776f291b
title: 自訂動作傳回處理選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2dd719271e6291decbd2123d5cf1525121769704b3fc4177c8b301662697689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947976"
---
# <a name="custom-action-return-processing-options"></a>自訂動作傳回處理選項

本主題會識別您可用來控制自訂動作執行緒的選項旗標。 旗標是用來指定主要和自訂動作執行緒會以同步方式執行 (Windows Installer 等待自訂動作執行緒完成，再繼續執行主要安裝執行緒) ，或以非同步方式 (Windows Installer 在主要安裝繼續) 時，同時執行自訂動作。

若要啟用選項旗標，請將下表所識別的值加入至 [CustomAction 資料表](customaction-table.md)之 [類型] 欄位中的值。



| 常數                                                           | 十六進位             | Decimal | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|-------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (無)                                                             | 0x00000000              | +0      | 如果結束代碼不是 0 (零) ，則同步執行會失敗。 <br/> 如果未設定旗標 msidbCustomActionTypeContinue，自訂動作必須傳回 [自訂動作傳回值](custom-action-return-values.md)中所描述的其中一個傳回值。<br/>                                                                                                                                                                                                                             |
| **msidbCustomActionTypeContinue**                                  | 0x00000040              | + 64     | 會忽略結束代碼並繼續的同步執行。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **msidbCustomActionTypeAsync**                                     | 0x00000080              | + 128    | 在序列結尾等候結束代碼的非同步執行。<br/> 此選項不能與 [並行安裝](concurrent-installations.md)搭配使用、 [復原自訂動作](rollback-custom-actions.md)或 [編寫自訂動作的腳本](scripts.md)。<br/>                                                                                                                                                                                                                                |
| **msidbCustomActionTypeAsync**  + **msidbCustomActionTypeContinue** | 0x00000040 + 0x00000080 | +192    | 未等候完成的非同步執行。<br/> Windows Installer 終止之後，就會繼續執行。<br/> 這個選項只可搭配使用的 EXE 類型自訂動作（ [可執行檔](executable-files.md)）使用。 <br/> 所有其他類型的自訂動作在安裝會話中只能是非同步，而且必須結束安裝才能終止。<br/> 此選項不能與 [並行安裝](concurrent-installations.md)一起使用。<br/> |



 

 

 




