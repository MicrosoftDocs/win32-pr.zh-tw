---
description: Winlogon 通知套件的相關資訊會儲存在登錄中。 登錄專案會指定通知套件的名稱、可執行封裝的 DLL 名稱，以及處理 Winlogon 事件的函式名稱。
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: 註冊 Winlogon 通知套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192624"
---
# <a name="registering-a-winlogon-notification-package"></a>註冊 Winlogon 通知套件

[*Winlogon*](../secgloss/w-gly.md)通知套件的相關資訊會儲存在登錄中。 登錄專案會指定通知套件的名稱、可執行封裝的 DLL 名稱，以及處理 Winlogon 事件的函式名稱。

當 Winlogon 開始時，它會檢查登錄並載入任何已註冊的通知套件。 當事件發生時，Winlogon 會針對每個封裝呼叫指定的事件處理常式函式。 可以在系統上註冊多個事件通知套件。

若要註冊您的通知套件，請建立名為 **Notify** 的登錄機碼作為下列登錄機碼的子機碼，並新增登錄 [專案](registry-entries.md)中詳細說明的值。

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
