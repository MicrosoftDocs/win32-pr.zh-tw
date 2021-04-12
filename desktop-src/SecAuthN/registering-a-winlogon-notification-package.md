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
# <a name="registering-a-winlogon-notification-package"></a><span data-ttu-id="efe05-104">註冊 Winlogon 通知套件</span><span class="sxs-lookup"><span data-stu-id="efe05-104">Registering a Winlogon Notification Package</span></span>

<span data-ttu-id="efe05-105">[*Winlogon*](../secgloss/w-gly.md)通知套件的相關資訊會儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="efe05-105">Information about [*Winlogon*](../secgloss/w-gly.md) notification packages is stored in the registry.</span></span> <span data-ttu-id="efe05-106">登錄專案會指定通知套件的名稱、可執行封裝的 DLL 名稱，以及處理 Winlogon 事件的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="efe05-106">Registry entries specify the name of the notification package, the name of the DLL that implements the package, and the names of the functions that handle Winlogon events.</span></span>

<span data-ttu-id="efe05-107">當 Winlogon 開始時，它會檢查登錄並載入任何已註冊的通知套件。</span><span class="sxs-lookup"><span data-stu-id="efe05-107">When Winlogon starts, it checks the registry and loads any registered notification packages.</span></span> <span data-ttu-id="efe05-108">當事件發生時，Winlogon 會針對每個封裝呼叫指定的事件處理常式函式。</span><span class="sxs-lookup"><span data-stu-id="efe05-108">When an event occurs, Winlogon calls the designated event handler function for each package.</span></span> <span data-ttu-id="efe05-109">可以在系統上註冊多個事件通知套件。</span><span class="sxs-lookup"><span data-stu-id="efe05-109">Multiple event notification packages may be registered on a system.</span></span>

<span data-ttu-id="efe05-110">若要註冊您的通知套件，請建立名為 **Notify** 的登錄機碼作為下列登錄機碼的子機碼，並新增登錄 [專案](registry-entries.md)中詳細說明的值。</span><span class="sxs-lookup"><span data-stu-id="efe05-110">To register your notification package, create a registry key named **Notify** as a subkey of the following registry key and add the values detailed in [Registry Entries](registry-entries.md).</span></span>

<span data-ttu-id="efe05-111">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**</span><span class="sxs-lookup"><span data-stu-id="efe05-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Winlogon**</span></span>

 

 
