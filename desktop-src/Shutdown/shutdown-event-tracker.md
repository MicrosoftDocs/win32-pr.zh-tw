---
description: 關機事件追蹤器可讓使用者或應用程式記錄關閉或重新開機系統的原因。
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: 關機事件追蹤器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4208914149bb84df34e67cca71b40cde66363211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319259"
---
# <a name="shutdown-event-tracker"></a><span data-ttu-id="857c7-103">關機事件追蹤器</span><span class="sxs-lookup"><span data-stu-id="857c7-103">Shutdown Event Tracker</span></span>

<span data-ttu-id="857c7-104">*關機事件追蹤* 器可讓使用者或應用程式記錄關閉或重新開機系統的原因。</span><span class="sxs-lookup"><span data-stu-id="857c7-104">The *Shutdown Event Tracker* enables the user or application to document the reason for shutting down or restarting the system.</span></span> <span data-ttu-id="857c7-105">當您從 [**開始**] 功能表選取 **關機**，或使用 [Shutdown.exe] 時，系統會提示使用者填寫資訊。</span><span class="sxs-lookup"><span data-stu-id="857c7-105">The user is prompted to fill in information when selecting **Shut Down** from the **Start** menu, or when using Shutdown.exe.</span></span> <span data-ttu-id="857c7-106">開發人員在呼叫 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 和 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) 函式時，可能會包含原因代碼。</span><span class="sxs-lookup"><span data-stu-id="857c7-106">Developers can include a reason code when calling the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions.</span></span> <span data-ttu-id="857c7-107">這項資訊會儲存在事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="857c7-107">The information is stored in the event log.</span></span>

<span data-ttu-id="857c7-108">**WINDOWS XP：** 從 Windows Server 2003 開始，預設會啟用這項功能，因此您必須在 Windows XP 上啟用它。</span><span class="sxs-lookup"><span data-stu-id="857c7-108">**Windows XP:** While this feature is enabled by default starting with Windows Server 2003, you must enable it on Windows XP.</span></span> <span data-ttu-id="857c7-109">如需詳細資訊，請參閱系統或 TechNet 上所含之關機事件追蹤器的檔。</span><span class="sxs-lookup"><span data-stu-id="857c7-109">For more information, see the documentation for the Shutdown Event Tracker included in the system or on TechNet.</span></span>

<span data-ttu-id="857c7-110">[**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)和 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)函式已更新，可支援 *dwReason* 參數中的關機原因代碼。</span><span class="sxs-lookup"><span data-stu-id="857c7-110">The [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions have been updated to support shutdown reason codes in the *dwReason* parameter.</span></span> <span data-ttu-id="857c7-111">使用 Reason 定義的值來建立關機原因代碼，或定義自訂的原因代碼。</span><span class="sxs-lookup"><span data-stu-id="857c7-111">Use the values defined in Reason.h to construct a shutdown reason code, or define a custom reason code.</span></span> <span data-ttu-id="857c7-112">關機原因代碼是由主要旗標、次要旗標和兩個選擇性旗標所組成。</span><span class="sxs-lookup"><span data-stu-id="857c7-112">A shutdown reason code is constructed from a major flag, a minor flag, and two optional flags.</span></span> <span data-ttu-id="857c7-113">如需詳細資訊，請參閱 [系統關機原因代碼](system-shutdown-reason-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="857c7-113">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="857c7-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="857c7-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="857c7-115">[ (TechNet) 關機事件追蹤器 ](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="857c7-115">[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span></span>
</dt> </dl>

 

 
