---
description: 列出必須執行才能建立認證管理員的 DLL 匯出。
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: 執行認證管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bbd42f4ade57b754c6f7a067519d7df2711cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851747"
---
# <a name="implementing-a-credential-manager"></a><span data-ttu-id="155a0-103">執行認證管理員</span><span class="sxs-lookup"><span data-stu-id="155a0-103">Implementing a Credential Manager</span></span>

<span data-ttu-id="155a0-104">若要建立認證管理員，您必須建立可匯出下列函式的 DLL：</span><span class="sxs-lookup"><span data-stu-id="155a0-104">To create a credential manager, you must create a DLL that exports the following functions:</span></span>

-   [<span data-ttu-id="155a0-105">**NPLogonNotify**</span><span class="sxs-lookup"><span data-stu-id="155a0-105">**NPLogonNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [<span data-ttu-id="155a0-106">**NPPasswordChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="155a0-106">**NPPasswordChangeNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

<span data-ttu-id="155a0-107">若要將通知還原至智慧卡登入的 [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) 和 [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) 功能，請建立名為 **SmartCardLogonNotify** 的登錄專案做為 **DWORD**，然後將它設定為1：</span><span class="sxs-lookup"><span data-stu-id="155a0-107">To restore notifications to the [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) functions for smart card logon, create a registry entry called **SmartCardLogonNotify** as a **DWORD**, and set it to 1:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

<span data-ttu-id="155a0-108">**Windows Server 2003 和 WINDOWS XP：** 不需要 **SmartCardLogonNotify** 登錄專案。</span><span class="sxs-lookup"><span data-stu-id="155a0-108">**Windows Server 2003 and Windows XP:** The **SmartCardLogonNotify** registry entry is not required.</span></span>

<span data-ttu-id="155a0-109">此外，認證管理員也應該支援 WNNC 開始 (的 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) 函式， \_) 的認證管理員不需要支援其他索引。</span><span class="sxs-lookup"><span data-stu-id="155a0-109">In addition, credential managers should also support the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function for WNNC\_START (supporting other indexes is not required for credential managers).</span></span> <span data-ttu-id="155a0-110">這會告訴 MPR 何時將啟動認證管理員。</span><span class="sxs-lookup"><span data-stu-id="155a0-110">This tells MPR when a credential manager will start.</span></span> <span data-ttu-id="155a0-111">藉由呼叫 **NPGetCaps** ，並將 *nIndex* 參數設定為 WNNC \_ START，MPR 會取得呼叫提供者的認證管理進入點函式之前所等待的時間。</span><span class="sxs-lookup"><span data-stu-id="155a0-111">By calling **NPGetCaps** with the *nIndex* parameter set to WNNC\_START, the MPR gets the time to wait before calling the provider's credential management entry point functions.</span></span> <span data-ttu-id="155a0-112">如果 MPR 有此資訊，它可以將它轉寄到認證管理員，設定超時時間。</span><span class="sxs-lookup"><span data-stu-id="155a0-112">And if the MPR has this information, it can forward it to the credential manager, setting the time out.</span></span>

 

 



