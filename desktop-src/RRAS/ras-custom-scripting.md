---
title: RAS 自訂腳本
description: 開發人員可以建立位於 RAS 用戶端電腦上的自訂腳本 DLL。 此 DLL 可在建立連接的過程中與伺服器進行通訊。
ms.assetid: c27b8b02-6018-4441-a355-1fb890b9001c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c625f020d9dafcb352c5f1b382014f9dba189330
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933347"
---
# <a name="ras-custom-scripting"></a><span data-ttu-id="807e1-104">RAS 自訂腳本</span><span class="sxs-lookup"><span data-stu-id="807e1-104">RAS Custom Scripting</span></span>

<span data-ttu-id="807e1-105">開發人員可以建立位於 RAS 用戶端電腦上的自訂腳本 DLL。</span><span class="sxs-lookup"><span data-stu-id="807e1-105">Developers can create a custom-scripting DLL that resides on a RAS client computer.</span></span> <span data-ttu-id="807e1-106">此 DLL 可在建立連接的過程中與伺服器進行通訊。</span><span class="sxs-lookup"><span data-stu-id="807e1-106">This DLL can communicate with the server during the process of establishing a connection.</span></span>

<span data-ttu-id="807e1-107">**Windows NT：** 無法使用自訂腳本。</span><span class="sxs-lookup"><span data-stu-id="807e1-107">**Windows NT:** Custom scripting is not available.</span></span>

## <a name="setting-up-the-dll"></a><span data-ttu-id="807e1-108">設定 DLL</span><span class="sxs-lookup"><span data-stu-id="807e1-108">Setting up the DLL</span></span>

<span data-ttu-id="807e1-109">若要設定 DLL，請在下列登錄機碼底下建立名稱 **CustomScriptDllPath** 的值：</span><span class="sxs-lookup"><span data-stu-id="807e1-109">To set up the DLL, create a value with the name **CustomScriptDllPath** under the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
```

<span data-ttu-id="807e1-110">此值的類型應為 **REG \_ EXPAND \_ SZ**。</span><span class="sxs-lookup"><span data-stu-id="807e1-110">This value should be of type **REG\_EXPAND\_SZ**.</span></span> <span data-ttu-id="807e1-111">此值應該包含自訂腳本 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="807e1-111">The value should contain the path to the custom-scripting DLL.</span></span> <span data-ttu-id="807e1-112">每部 RAS 用戶端電腦都只支援一個自訂腳本 DLL。</span><span class="sxs-lookup"><span data-stu-id="807e1-112">Only one custom-scripting DLL is supported for each RAS client computer.</span></span>

## <a name="interaction-between-the-server-ras-and-the-custom-scripting-dll"></a><span data-ttu-id="807e1-113">伺服器、RAS 和 Custom-Scripting DLL 之間的互動</span><span class="sxs-lookup"><span data-stu-id="807e1-113">Interaction Between the Server, RAS, and the Custom-Scripting DLL</span></span>

<span data-ttu-id="807e1-114">自訂腳本 DLL 應匯出單一進入點： [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)。</span><span class="sxs-lookup"><span data-stu-id="807e1-114">The custom scripting DLL should export a single entry point: [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn).</span></span> <span data-ttu-id="807e1-115">RAS 會在連接程式的 RASCS 互動狀態期間呼叫此函式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="807e1-115">RAS calls this function during the RASCS\_Interactive state of the connection process.</span></span> <span data-ttu-id="807e1-116">RASCS \_ 互動狀態為暫停狀態，可讓使用者與自訂腳本 DLL 所顯示的使用者介面互動。</span><span class="sxs-lookup"><span data-stu-id="807e1-116">The RASCS\_Interactive state is a paused state, which allows the user to interact with a user interface presented by the custom-scripting DLL.</span></span> <span data-ttu-id="807e1-117">如需連接狀態的詳細資訊，請參閱 [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="807e1-117">See [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) for more information about connection states.</span></span>

<span data-ttu-id="807e1-118">RAS 會以參數形式傳遞至 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) 函式：</span><span class="sxs-lookup"><span data-stu-id="807e1-118">RAS will pass as parameters to the [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) function:</span></span>

-   <span data-ttu-id="807e1-119">用戶端電腦上用於連接之埠的控制碼。</span><span class="sxs-lookup"><span data-stu-id="807e1-119">A handle to the port on the client computer that is being used for the connection.</span></span>
-   <span data-ttu-id="807e1-120">識別連接之電話簿和專案的字串。</span><span class="sxs-lookup"><span data-stu-id="807e1-120">Strings that identify the phone book and entry for the connection.</span></span>
-   <span data-ttu-id="807e1-121">RAS 也會將控制碼傳遞至視窗，讓 DLL 能呈現使用者介面。</span><span class="sxs-lookup"><span data-stu-id="807e1-121">RAS also passes in a handle to a window to enable the DLL to present a user interface.</span></span>
-   <span data-ttu-id="807e1-122">DLL 可以用來與伺服器通訊的一組函式指標。</span><span class="sxs-lookup"><span data-stu-id="807e1-122">A set of function pointers that the DLL can use to communicate with the server.</span></span>

<span data-ttu-id="807e1-123">如需這些參數的詳細資訊，請參閱 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) 。</span><span class="sxs-lookup"><span data-stu-id="807e1-123">See [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) for more information about these parameters.</span></span>

<span data-ttu-id="807e1-124">RAS 會將 [**RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) 結構的指標傳遞至 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)的最後一個參數。</span><span class="sxs-lookup"><span data-stu-id="807e1-124">RAS passes a pointer to a [**RASCUSTOMSCRIPTEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa376738(v=vs.85)) structure as the last parameter to [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn).</span></span> <span data-ttu-id="807e1-125">此結構包含 [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings)型別函式的指標。</span><span class="sxs-lookup"><span data-stu-id="807e1-125">This structure contains a pointer to a function of type [**PFNRASSETCOMMSETTINGS**](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings).</span></span> <span data-ttu-id="807e1-126">自訂腳本 DLL 會呼叫這個函式，以修改連接所使用之通訊埠上的通訊設定。</span><span class="sxs-lookup"><span data-stu-id="807e1-126">The custom-scripting DLL calls this function to modify the communication settings on the port being used by the connection.</span></span>

<span data-ttu-id="807e1-127">RAS 會協調伺服器與自訂腳本 DLL 之間的互動。</span><span class="sxs-lookup"><span data-stu-id="807e1-127">RAS mediates the interaction between the server and the custom-scripting DLL.</span></span> <span data-ttu-id="807e1-128">一般來說，伺服器會起始對話。</span><span class="sxs-lookup"><span data-stu-id="807e1-128">Typically, the server initiates the dialog.</span></span> <span data-ttu-id="807e1-129">例如，伺服器可能會要求使用者的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="807e1-129">For example, the server may request the user name and password of the user.</span></span>

<span data-ttu-id="807e1-130">使用自訂腳本建立連接時，伺服器不需要執行 Windows NT 4.0 或 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="807e1-130">When using custom-scripting to establish a connection, the server need not be running Windows NT 4.0 or Windows 2000.</span></span>

## <a name="custom-scripting-user-interface-must-support-idcancel"></a><span data-ttu-id="807e1-131">自訂腳本消費者介面必須支援 IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="807e1-131">Custom Scripting User Interface Must Support IDCANCEL</span></span>

<span data-ttu-id="807e1-132">如果自訂撥號程式顯示使用者介面，則使用者介面必須支援 \_ LOWORD (*WParam*) 等於 IDCANCEL 的 WM 命令訊息。</span><span class="sxs-lookup"><span data-stu-id="807e1-132">If the custom dialer displays a user interface, the user interface must support WM\_COMMAND messages where LOWORD(*wParam*) equals IDCANCEL.</span></span>

## <a name="configuring-the-connection"></a><span data-ttu-id="807e1-133">設定連接</span><span class="sxs-lookup"><span data-stu-id="807e1-133">Configuring the Connection</span></span>

<span data-ttu-id="807e1-134">[**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn)進入點可以從 [**RASDIALDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)或 Windows XP 上的 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)叫用。</span><span class="sxs-lookup"><span data-stu-id="807e1-134">The [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) entry point can be invoked from [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) or, on Windows XP, from [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="807e1-135">若要從 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)叫用 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) ，請 \_ 在連接的電話簿專案中，設定 RASEO CustomScript 選項。</span><span class="sxs-lookup"><span data-stu-id="807e1-135">To invoke [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) from [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga), set the RASEO\_CustomScript option in the phone-book entry for the connection.</span></span> <span data-ttu-id="807e1-136">如需電話簿輸入選項的說明，請參閱 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))的 **dwfOptions** 成員。</span><span class="sxs-lookup"><span data-stu-id="807e1-136">See the **dwfOptions** member of [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) for a description of phone-book entry options.</span></span> <span data-ttu-id="807e1-137">使用 [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) 和 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) 函式，以程式設計方式設定此選項。</span><span class="sxs-lookup"><span data-stu-id="807e1-137">Use the [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) and [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) functions to set this option programmatically.</span></span>

<span data-ttu-id="807e1-138">**WINDOWS XP：** 若要從 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)叫用 [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) ，則對 **RasDial** 的呼叫必須指定 [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85))結構，而且此結構必須指定 RDEOPT \_ UseCustomScripting 旗標。</span><span class="sxs-lookup"><span data-stu-id="807e1-138">**Windows XP:** To invoke [**RasCustomScriptExecute**](/windows/desktop/api/Ras/nc-ras-rascustomscriptexecutefn) from [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala), the call to **RasDial** must specify a [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) structure, and this structure must specify the RDEOPT\_UseCustomScripting flag.</span></span> <span data-ttu-id="807e1-139">此外，連接的電話簿專案必須指定 RASEO \_ CustomScript 選項，如前面段落中所述。</span><span class="sxs-lookup"><span data-stu-id="807e1-139">In addition, the phone-book entry for the connection must specify the RASEO\_CustomScript option as described in the preceding paragraph.</span></span>

## <a name="invoking-the-custom-scripting-dll"></a><span data-ttu-id="807e1-140">叫用自訂腳本 DLL</span><span class="sxs-lookup"><span data-stu-id="807e1-140">Invoking the Custom Scripting DLL</span></span>

<span data-ttu-id="807e1-141">如果使用者針對已設定 RASEO CustomScript 的電話簿專案啟用連線，RAS 會叫用 \_ 自訂腳本 DLL。</span><span class="sxs-lookup"><span data-stu-id="807e1-141">If the user activates a connection for a phone-book entry that has RASEO\_CustomScript set, RAS invokes the custom-scripting DLL.</span></span> <span data-ttu-id="807e1-142">在此案例中，RAS 會從 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)叫用自訂腳本 DLL。</span><span class="sxs-lookup"><span data-stu-id="807e1-142">In this scenario, RAS invokes the custom-scripting DLL from [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga).</span></span>

<span data-ttu-id="807e1-143">若要以程式設計方式叫用自訂腳本 DLL，請使用 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) 函數建立連接。</span><span class="sxs-lookup"><span data-stu-id="807e1-143">To invoke the custom-scripting DLL programmatically, establish the connection using the [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) function.</span></span> <span data-ttu-id="807e1-144">在 Windows XP 上， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式也會叫用自訂腳本 DLL。</span><span class="sxs-lookup"><span data-stu-id="807e1-144">On Windows XP, the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function also invokes the custom-scripting DLL.</span></span>

 

 