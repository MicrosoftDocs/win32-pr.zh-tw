---
title: 重要的系統服務
description: 重新開機管理員無法停止和重新開機重要的系統服務，不需要重新開機系統。 更新這些服務中的任何一個使用的檔案或資源時，都需要重新開機系統。
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022141"
---
# <a name="critical-system-services"></a><span data-ttu-id="56821-104">重要的系統服務</span><span class="sxs-lookup"><span data-stu-id="56821-104">Critical System Services</span></span>

<span data-ttu-id="56821-105">重新開機管理員無法停止和重新開機重要的系統服務，不需要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="56821-105">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="56821-106">更新這些服務中的任何一個使用的檔案或資源時，都需要重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="56821-106">Updates to any file or resource in use by one of these services requires a system restart.</span></span>

<span data-ttu-id="56821-107">**判斷進程是否為重要的系統服務。**</span><span class="sxs-lookup"><span data-stu-id="56821-107">**To determine whether a process is a critical system service.**</span></span>

1.  <span data-ttu-id="56821-108">使用 [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) 函式註冊處理常式。</span><span class="sxs-lookup"><span data-stu-id="56821-108">Register the process using the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function.</span></span>
2.  <span data-ttu-id="56821-109">呼叫 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) 函數，以取得 [**RM \_ 進程 \_ 資訊**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="56821-109">Call the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to get the [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure.</span></span>
3.  <span data-ttu-id="56821-110">傳回的 [**rm \_ 進程 \_ 資訊**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info)結構的 **ApplicationType** 成員包含 [**rm \_ 應用程式 \_ 類型**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type)的列舉值。</span><span class="sxs-lookup"><span data-stu-id="56821-110">The **ApplicationType** member of the returned [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure contains a [**RM\_APP\_TYPE**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) enumeration value.</span></span> <span data-ttu-id="56821-111">此值會設定為重要系統進程的 **RmCriticial** 。</span><span class="sxs-lookup"><span data-stu-id="56821-111">This value is set to **RmCriticial** for a critical system process.</span></span>

<span data-ttu-id="56821-112">重要的系統服務包含 smss.exe、csrss.exe、wininit.exe、logonui.exe、lsass.exe、services.exe、winlogon.exe、系統、使用 RPCSS 的 svchost.exe，以及 Dcom/PnP 的 svchost.exe。</span><span class="sxs-lookup"><span data-stu-id="56821-112">Critical system services include smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe with RPCSS, and svchost.exe with Dcom/PnP.</span></span>

 

 




