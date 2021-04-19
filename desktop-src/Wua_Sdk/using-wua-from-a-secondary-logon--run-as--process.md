---
description: 如果 WUA 應用程式是在次要登入服務的內容中執行，則 Windows Update 代理程式 (WUA) 應用程式無法安裝需要使用者互動的更新。
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: 從次要登入使用 WUA (以) 進程的方式執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972651"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a><span data-ttu-id="ca56d-103">從次要登入使用 WUA (以) 進程的方式執行</span><span class="sxs-lookup"><span data-stu-id="ca56d-103">Using WUA from a Secondary Logon (Run As) Process</span></span>

<span data-ttu-id="ca56d-104">如果 WUA 應用程式是在次要登入服務的內容中執行，則 Windows Update 代理程式 (WUA) 應用程式無法安裝需要使用者互動的更新。</span><span class="sxs-lookup"><span data-stu-id="ca56d-104">Updates that require user interaction cannot be installed by Windows Update Agent (WUA) applications if the WUA applications are running in the context of the Secondary Logon service.</span></span>

<span data-ttu-id="ca56d-105">如果呼叫 WUA 的進程是在 RunAs 服務或次要登入服務的內容中執行，則嘗試安裝需要使用者互動的更新會失敗，並傳回 **WU \_ 電子 \_ 沒有 \_ 互動式 \_ 使用者** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca56d-105">If the process that is calling WUA is running in the context of the RunAs service or the Secondary Logon service, an attempt to install an update that requires user interaction fails and returns the **WU\_E\_NO\_INTERACTIVE\_USER** error.</span></span>

<span data-ttu-id="ca56d-106">在 Microsoft Windows 中，您可以使用與目前登入的使用者不同的使用者身分來執行程式。</span><span class="sxs-lookup"><span data-stu-id="ca56d-106">In Microsoft Windows, you can run programs as a user who differs from the user who is currently logged on.</span></span> <span data-ttu-id="ca56d-107">若要這樣做，次要登入服務必須正在執行。</span><span class="sxs-lookup"><span data-stu-id="ca56d-107">To do this the Secondary Logon service must be running.</span></span>

 

 



