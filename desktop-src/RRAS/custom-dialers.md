---
title: 自訂撥號
description: Windows 2000 和更新版本的作業系統可讓開發人員提供自己的自訂撥號程式，以與遠端存取服務 (RAS) 搭配使用。
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- 自訂撥號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186048"
---
# <a name="custom-dialers"></a><span data-ttu-id="95e57-104">自訂撥號</span><span class="sxs-lookup"><span data-stu-id="95e57-104">Custom Dialers</span></span>

<span data-ttu-id="95e57-105">Windows 2000 和更新版本的作業系統可讓開發人員提供自己的自訂撥號程式，以與遠端存取服務 (RAS) 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="95e57-105">Windows 2000 and later operating systems enable developers to provide their own custom dialers that work with the Remote Access Service (RAS).</span></span> <span data-ttu-id="95e57-106">自訂的撥號程式會實作為單一動態連結程式庫 (DLL) ，以匯出下列進入點：</span><span class="sxs-lookup"><span data-stu-id="95e57-106">The custom dialer is implemented as a single dynamic-link library (DLL) that exports the following entry points:</span></span>

-   [<span data-ttu-id="95e57-107">**RasCustomDial**</span><span class="sxs-lookup"><span data-stu-id="95e57-107">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [<span data-ttu-id="95e57-108">**RasCustomDialDlg**</span><span class="sxs-lookup"><span data-stu-id="95e57-108">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [<span data-ttu-id="95e57-109">**RasCustomHangup**</span><span class="sxs-lookup"><span data-stu-id="95e57-109">**RasCustomHangup**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [<span data-ttu-id="95e57-110">**RasCustomEntryDlg**</span><span class="sxs-lookup"><span data-stu-id="95e57-110">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [<span data-ttu-id="95e57-111">**RasCustomDeleteEntryNotify**</span><span class="sxs-lookup"><span data-stu-id="95e57-111">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

<span data-ttu-id="95e57-112">自訂撥號 DLL 必須匯出所有的進入點，而且必須將進入點實作為 Unicode 函數。</span><span class="sxs-lookup"><span data-stu-id="95e57-112">The custom-dial DLL must export all of these entry points, and it must implement the entry points as Unicode functions.</span></span> <span data-ttu-id="95e57-113">如需這些函式的詳細資訊，請參閱 Windows SDK 遠端存取服務參考中各項功能的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="95e57-113">For more information about these functions, see the reference page for each function in the Windows SDK Remote Access Service Reference.</span></span>

<span data-ttu-id="95e57-114">為了讓 RAS 連線使用自訂撥號程式，連接的電話簿專案必須包含自訂撥號 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="95e57-114">In order for a RAS connection to use the custom dialer, the phone-book entry for the connection must contain the path to the custom-dial DLL.</span></span> <span data-ttu-id="95e57-115">使用 [RAS API 函式 [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa)和 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) ]，在 [電話簿] 專案的 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))結構的 **szCustomDialDll** 成員中設定此路徑。</span><span class="sxs-lookup"><span data-stu-id="95e57-115">Use the RAS API functions [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) and [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) to set this path in the **szCustomDialDll** member of the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure for the phone-book entry.</span></span>

## <a name="updating-the-registry-for-custom-dialers"></a><span data-ttu-id="95e57-116">更新自訂撥號的登錄</span><span class="sxs-lookup"><span data-stu-id="95e57-116">Updating the Registry for Custom Dialers</span></span>

<span data-ttu-id="95e57-117">為了讓系統能夠撥號使用自訂撥號程式的連線，自訂撥號 DLL 的路徑必須存在於下列登錄值中。</span><span class="sxs-lookup"><span data-stu-id="95e57-117">In order for the system to dial a connection that uses a custom dialer, the path to the custom-dial DLL must exist in the following registry value.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

<span data-ttu-id="95e57-118">由於 **CustomDLL** 的類型為 **REG \_ multiple \_ SZ**，因此可以保留多個自訂撥號 dll 的路徑。</span><span class="sxs-lookup"><span data-stu-id="95e57-118">Because **CustomDLL** is of type **REG\_MULTI\_SZ**, it can hold paths to multiple custom-dial DLLs.</span></span> <span data-ttu-id="95e57-119">除了連線的電話簿專案以外，您還需要設定此登錄值中自訂撥號 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="95e57-119">You need to set the path to the custom-dial DLL in this registry value, in addition to the phone-book entry for the connection.</span></span>

<span data-ttu-id="95e57-120">根據預設，此登錄值只能由具有系統管理員或系統許可權的使用者寫入。</span><span class="sxs-lookup"><span data-stu-id="95e57-120">By default, this registry value is writeable only by a user with Administrator or System privileges.</span></span> <span data-ttu-id="95e57-121">基於安全考慮，請勿變更此登錄機碼的許可權。</span><span class="sxs-lookup"><span data-stu-id="95e57-121">For security reasons, do not change the permissions on this registry key.</span></span>

## <a name="using-custom-dialers-at-system-logon"></a><span data-ttu-id="95e57-122">在系統登入時使用自訂的撥號</span><span class="sxs-lookup"><span data-stu-id="95e57-122">Using Custom Dialers at System Logon</span></span>

<span data-ttu-id="95e57-123">Windows 2000 和更新版本的作業系統可讓使用者在登入時建立 RAS 連接。</span><span class="sxs-lookup"><span data-stu-id="95e57-123">Windows 2000 and later operating systems allow a user to establish a RAS connection at the time of logon.</span></span> <span data-ttu-id="95e57-124">若要這樣做，使用者會使用 [**登入資訊**] 對話方塊中的 [**撥號網路**] 來檢查登入。</span><span class="sxs-lookup"><span data-stu-id="95e57-124">To do so, the user checks **Logon using Dial-up Networking** in the **Logon Information** dialog box.</span></span> <span data-ttu-id="95e57-125">當使用者按一下 [確定] 按鈕之後，系統會顯示可用的連接。</span><span class="sxs-lookup"><span data-stu-id="95e57-125">After the user clicks the Okay button, the system displays the available connections.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="95e57-126">安全性考量</span><span class="sxs-lookup"><span data-stu-id="95e57-126">Security Considerations</span></span>

<span data-ttu-id="95e57-127">在大多數情況下，自訂撥號程式會使用叫用它之使用者的安全性許可權來操作。</span><span class="sxs-lookup"><span data-stu-id="95e57-127">In most cases, a custom dialer operates with the security privileges of the user that invokes it.</span></span> <span data-ttu-id="95e57-128">但是，如果在登入時叫用自訂撥號程式，它就會以系統許可權運作。</span><span class="sxs-lookup"><span data-stu-id="95e57-128">However, if the custom dialer is invoked at logon, it operates with system privileges.</span></span> <span data-ttu-id="95e57-129">因此，請設計自訂的撥號程式，使其無法用來違反系統安全性。</span><span class="sxs-lookup"><span data-stu-id="95e57-129">Therefore, design the custom dialer so that it cannot be used to violate system security.</span></span> <span data-ttu-id="95e57-130">例如，撥號程式不應顯示使用者介面，以允許使用者對電腦檔案系統的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="95e57-130">For example, the dialer should not present a user interface that allows the user write access to the computer's file system.</span></span> <span data-ttu-id="95e57-131">提供這類存取的使用者介面包括 [ **尋找** 檔案] 對話方塊、[檔案 **開啟** ] 對話方塊和 **[Windows 說明**]。</span><span class="sxs-lookup"><span data-stu-id="95e57-131">User interfaces that provide such access include the **Find-File** dialog, the **File-Open** common dialog, and Windows **Help**.</span></span>

## <a name="custom-dialer-user-interface-must-support-idcancel"></a><span data-ttu-id="95e57-132">自訂的撥號程式消費者介面必須支援 IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="95e57-132">Custom Dialer User Interface Must Support IDCANCEL</span></span>

<span data-ttu-id="95e57-133">如果自訂撥號程式顯示使用者介面，則使用者介面必須支援 \_ LOWORD (*WParam*) 等於 IDCANCEL 的 WM 命令訊息。</span><span class="sxs-lookup"><span data-stu-id="95e57-133">If the custom dialer displays a user interface, the user interface must support WM\_COMMAND messages where LOWORD(*wParam*) equals IDCANCEL.</span></span>

 

 