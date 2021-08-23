---
description: 說明 Winlogon 事件的登錄專案。
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: '登錄專案 (驗證) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388cbe42d085543d5e7d4df1c9705504864b370cf94eb32f4025eaba12b89ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919444"
---
# <a name="registry-entries-authentication"></a>登錄專案 (驗證) 

為了讓您的封裝從 [*Winlogon*](../secgloss/w-gly.md)接收事件通知，您必須提供封裝的名稱、封裝中的事件處理常式函式名稱、負責執行封裝的 dll，以及 dll 是否支援非同步事件和模擬的相關資訊。

您應建立通知套件登錄機碼作為

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **通知**

金鑰的名稱通常與 DLL 的名稱相同;不過，這不是必要的。 為您的套件選擇的名稱不能與其他已安裝之通知套件的名稱衝突。

如果您的封裝中有相關的事件處理常式函式，請在 [ **通知** ] 登錄機碼中建立下列登錄值。



| 值名稱 \[ 資料類型\]                         | Description                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **非同步** \[**REG \_DWORD**\]<br/>    | 指出封裝是否可以非同步處理事件。 如果此值設定為1，則 Winlogon 會在個別的執行緒中呼叫封裝函式。 否則，則沒有。<br/>                                                                                                                                                                                                                                 |
| **DllName** \[**REG \_展開 \_ SZ**\]<br/>    | 執行通知封裝的 DLL 名稱，例如： "Notify.dll"。<br/>                                                                                                                                                                                                                                                                                                                          |
| 模擬 \[**REG \_DWORD**\]<br/>     | 指出當 Winlogon 呼叫通知套件功能時，是否應模擬已登入之使用者的安全性 [*內容*](../secgloss/c-gly.md) 。 如果此值設定為1，則 Winlogon 會使用模擬。 否則，則沒有。<br/>                                                                                                                    |
| **鎖定** \[**REG \_SZ**\]<br/>               | 處理桌面鎖定事件的函式名稱，例如： "WLEventLock"。<br/>                                                                                                                                                                                                                                                                                                                           |
| **登出** \[**REG \_SZ**\]<br/>             | 處理登出事件的函式名稱，例如： "WLEventLogoff"。<br/>                                                                                                                                                                                                                                                                                                                               |
| **登** \[ 入 **REG \_SZ**\]<br/>              | 處理登入事件的函式名稱，例如： "WLEventLogon"。<br/>                                                                                                                                                                                                                                                                                                                                 |
| **關機** \[**REG \_SZ**\]<br/>           | 處理關機事件的函式名稱，例如： "WLEventShutdown"。<br/>                                                                                                                                                                                                                                                                                                                           |
| **SmartCardLogonNotify** \[**DWORD**\]<br/> | 指出 Winlogon 是否應從智慧卡產生登入事件的通知。 如果此值設定為1，則 Winlogon 允許智慧卡通知。 否則，則沒有。<br/>                                                                                                                                                                                                                     |
| **StartScreenSaver** \[**REG \_SZ**\]<br/>   | 處理螢幕保護裝置啟動事件的函式名稱，例如： "WLEventStartScreenSaver"。<br/>                                                                                                                                                                                                                                                                                                          |
| **StartShell** \[**REG \_SZ**\]<br/>         | 處理 shell 啟動事件的函式名稱，例如： "WLEventStartShell"。<br/> Shell 啟動事件會在使用者登入之後，但在桌面出現之前發生。 這與登入事件不同之處在于，已建立使用者的安全性 [*內容*](../secgloss/c-gly.md) ，而且可以使用網路連線等資源。<br/> |
| **啟動** \[**REG \_SZ**\]<br/>            | 處理系統啟動事件的函式名稱，例如： "WLEventStartup"。<br/>                                                                                                                                                                                                                                                                                                                       |
| **StopScreenSaver** \[**REG \_SZ**\]<br/>    | 處理螢幕保護裝置停止事件的函式名稱，例如： "WLEventStopScreenSaver"。<br/>                                                                                                                                                                                                                                                                                                            |
| **解除鎖定** \[**REG \_SZ**\]<br/>             | 處理桌面解除鎖定事件的函式名稱，例如： "WLEventUnlock"。<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
