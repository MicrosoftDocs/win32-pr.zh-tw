---
title: SYSMON 傳回值
description: 以下是在 Smonmsg 中定義的系統監視器傳回值的清單。
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ce526a64132cef51338a83b387aa8e9bfd58ce0ef0b99a1fb7db0dce4c15ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956444"
---
# <a name="sysmon-return-values"></a>SYSMON 傳回值

以下是在 Smonmsg 中定義的系統監視器傳回值的清單。



| 傳回值                                       | 描述                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SMON \_ 狀態 \_ DUPL \_ 計數器 \_ 路徑 (0xC0001388)      | 計數器集合已包含指定的計數器。                                                                                                                                                                               |
| SMON \_ STATUS \_ NO \_ SYSMON \_ OBJECT (0xC0001389)       | 這些設定不包含任何完整的系統監視器 HTML 物件。                                                                                                                                                                        |
| SMON \_ 狀態 \_ 太 \_ 少 \_ 樣本 (0xC000138A)        | 指定的記錄檔包含的資料樣本少於兩個。                                                                                                                                                                                 |
| SMON \_ 狀態 \_ 記錄 \_ 檔 \_ 大小 \_ 限制 (0xC000138B)   | 指定的記錄檔超過系統監視器控制項的大小限制。 如果目前已選取記錄檔，請選取 [目前的活動] 作為資料來源，以便卸載目前的記錄檔，然後重新選取指定的記錄檔。 |
| SMON \_ 狀態 \_ 記錄 \_ 檔 \_ 資料 \_ 源 (0xC000138C)  | 若要在資料來源中加入新的記錄檔，必須將資料來源類型變更為 sysmonLogFiles 以外的類型。                                                                                                                          |
| SMON \_ 狀態 \_ DUPL \_ 記錄 \_ 檔 \_ 路徑 (0xC000138D)    | 記錄檔集合已包含指定的記錄檔。                                                                                                                                                                             |



 

如需系統監視器所傳回之其他傳回值的描述，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 和 [效能資料](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values)協助程式錯誤碼。

 

 