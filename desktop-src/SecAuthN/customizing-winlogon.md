---
description: 藉由執行認證提供者來自訂 Winlogon 行為。
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: 自訂 Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996602"
---
# <a name="customizing-winlogon"></a><span data-ttu-id="55c1e-103">自訂 Winlogon</span><span class="sxs-lookup"><span data-stu-id="55c1e-103">Customizing Winlogon</span></span>

<span data-ttu-id="55c1e-104">藉由執行認證提供者來自訂 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 行為。</span><span class="sxs-lookup"><span data-stu-id="55c1e-104">Customize [*Winlogon*](/windows/desktop/SecGloss/w-gly) behavior by implementing a Credential Provider.</span></span> <span data-ttu-id="55c1e-105">如需認證提供者的詳細資訊，請參閱 [**ICredentialProvider 介面**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider)。</span><span class="sxs-lookup"><span data-stu-id="55c1e-105">For information about Credential Providers, see [**ICredentialProvider Interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span></span>

<span data-ttu-id="55c1e-106">**Windows Server 2003 和 WINDOWS XP：** 不支援認證提供者。</span><span class="sxs-lookup"><span data-stu-id="55c1e-106">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span>

<span data-ttu-id="55c1e-107">下列各節說明在 windows Vista 之前的 Windows 版本中自訂 Winlogon 的方式。</span><span class="sxs-lookup"><span data-stu-id="55c1e-107">The following sections describe ways to customize Winlogon in Windows versions prior to Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="55c1e-108">Windows Vista 中會忽略 GINA Dll 和 Winlogon 通知套件。</span><span class="sxs-lookup"><span data-stu-id="55c1e-108">GINA DLLs and Winlogon notification packages are ignored in Windows Vista.</span></span>

 

-   [<span data-ttu-id="55c1e-109">Winlogon 通知套件</span><span class="sxs-lookup"><span data-stu-id="55c1e-109">Winlogon Notification Packages</span></span>](#winlogon-notification-packages)
-   [<span data-ttu-id="55c1e-110">GINA 存根</span><span class="sxs-lookup"><span data-stu-id="55c1e-110">GINA Stubs</span></span>](#gina-stubs)
-   [<span data-ttu-id="55c1e-111">GINA 鉤</span><span class="sxs-lookup"><span data-stu-id="55c1e-111">GINA Hooks</span></span>](#gina-hooks)

## <a name="winlogon-notification-packages"></a><span data-ttu-id="55c1e-112">Winlogon 通知套件</span><span class="sxs-lookup"><span data-stu-id="55c1e-112">Winlogon Notification Packages</span></span>

<span data-ttu-id="55c1e-113">Winlogon 通知套件是一個 DLL，可匯出處理 Winlogon 事件的函式。</span><span class="sxs-lookup"><span data-stu-id="55c1e-113">A Winlogon notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="55c1e-114">例如，當使用者登入系統時，Winlogon 會呼叫每個通知套件來提供事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="55c1e-114">For example, when a user logs onto the system, Winlogon calls each notification package to provide information about the event.</span></span> <span data-ttu-id="55c1e-115">如需詳細資訊，請參閱 [Winlogon 通知套件](winlogon-notification-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="55c1e-115">For more information, see [Winlogon Notification Packages](winlogon-notification-packages.md).</span></span>

## <a name="gina-stubs"></a><span data-ttu-id="55c1e-116">GINA 存根</span><span class="sxs-lookup"><span data-stu-id="55c1e-116">GINA Stubs</span></span>

<span data-ttu-id="55c1e-117">[*GINA*](/windows/desktop/SecGloss/g-gly)存根是自訂的 GINA DLL，它使用先前安裝的 GINA DLL 的匯出函式， (通常 MsGina.dll) 。</span><span class="sxs-lookup"><span data-stu-id="55c1e-117">A [*GINA*](/windows/desktop/SecGloss/g-gly) stub is a custom GINA DLL that uses the export function implementations of a previously installed GINA DLL (typically MsGina.dll).</span></span> <span data-ttu-id="55c1e-118">GINA 存根會取得先前安裝的 GINA DLL 所匯出之每個函式的指標。</span><span class="sxs-lookup"><span data-stu-id="55c1e-118">A GINA stub gets pointers to each function exported by the previously installed GINA DLL.</span></span> <span data-ttu-id="55c1e-119">每個 GINA 存根函式接著會使用適當的函式指標，在先前安裝的 GINA DLL 中呼叫對應的函式。</span><span class="sxs-lookup"><span data-stu-id="55c1e-119">Each GINA stub function then uses the appropriate function pointer to call the corresponding function in the previously installed GINA DLL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55c1e-120">每個 GINA 存根函數都必須在先前安裝的 GINA 中呼叫對應的函式。</span><span class="sxs-lookup"><span data-stu-id="55c1e-120">Each GINA stub function must call the corresponding function in the previously installed GINA.</span></span>

 

<span data-ttu-id="55c1e-121">GINA 存根函式可在其一或多個匯出函式中執行額外的功能。</span><span class="sxs-lookup"><span data-stu-id="55c1e-121">A GINA stub function can implement additional functionality in one or more of its export functions.</span></span> <span data-ttu-id="55c1e-122">例如，GINA stub 的 [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) 函式可能會在呼叫 MsGina.dll 的 **WlxLoggedOutSAS** 函式之前，先檢查目前的時間。</span><span class="sxs-lookup"><span data-stu-id="55c1e-122">For example, the [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) function of a GINA stub might check the current time before calling the **WlxLoggedOutSAS** function of the MsGina.dll.</span></span> <span data-ttu-id="55c1e-123">如果目前時間是在特定範圍內，存根函式可能會顯示一則訊息，指出在該期間內不允許登入，並將 **WLX \_ SAS \_ 動作 \_ 無** 傳回給 Winlogon。</span><span class="sxs-lookup"><span data-stu-id="55c1e-123">If the current time was within a specific range, the stub function could display a message that indicates logon is disallowed during that time period and return **WLX\_SAS\_ACTION\_NONE** to Winlogon.</span></span> <span data-ttu-id="55c1e-124">MsGina.dll 的 **WlxLoggedOutSAS** 函式只會在允許的時間週期內呼叫。</span><span class="sxs-lookup"><span data-stu-id="55c1e-124">The **WlxLoggedOutSAS** function of the MsGina.dll would then be called only during the allowed time period.</span></span>

<span data-ttu-id="55c1e-125">GINA 存根應用程式會透過 [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize)函式的 *pWinlogonFunctions* 參數，取得 Winlogon 支援函數的分派資料表。</span><span class="sxs-lookup"><span data-stu-id="55c1e-125">The GINA stub application gets a dispatch table to Winlogon support functions through the *pWinlogonFunctions* parameter of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function.</span></span> <span data-ttu-id="55c1e-126">GINA 存根應用程式可以使用此分派資料表來呼叫 Winlogon 支援函式。</span><span class="sxs-lookup"><span data-stu-id="55c1e-126">The GINA stub application can use this dispatch table to call Winlogon support functions.</span></span> <span data-ttu-id="55c1e-127">例如，GINA 存根應用程式可以呼叫 [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify)函式，以在 [*智慧卡*](/windows/desktop/SecGloss/s-gly)插入 [*讀取器*](/windows/desktop/SecGloss/r-gly)時， (SAS) 事件時產生 [*安全的注意順序*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="55c1e-127">For example, A GINA stub application can call the [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) function to cause a [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) event when a [*smart card*](/windows/desktop/SecGloss/s-gly) is inserted into a [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="55c1e-128">如需有關建立 GINA 存根的詳細資訊，請參閱 \\ \\ 平臺軟體發展工具組的範例安全性 GINA GinaStub 目錄中的 GINA 存根範例 \\ \\) 安裝 (SDK。</span><span class="sxs-lookup"><span data-stu-id="55c1e-128">For more information about creating a GINA stub, see the Gina Stubs sample in the \\Samples\\Security\\Gina\\GinaStub directory of a Platform Software Development Kit (SDK) installation.</span></span>

> [!Note]  
> <span data-ttu-id="55c1e-129">GINA 和 Winlogon 之間的所有呼叫都必須在單一線程內。</span><span class="sxs-lookup"><span data-stu-id="55c1e-129">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

## <a name="gina-hooks"></a><span data-ttu-id="55c1e-130">GINA 鉤</span><span class="sxs-lookup"><span data-stu-id="55c1e-130">GINA Hooks</span></span>

<span data-ttu-id="55c1e-131">GINA 攔截是 GINA 存根，在其 WlxInitialize 函式的 [](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize)中，會以其本身的 **WlxDialogBoxParam** 函數實作為指標，取代分派資料表中 [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support 函數的指標。</span><span class="sxs-lookup"><span data-stu-id="55c1e-131">A GINA hook is a GINA stub that, in its implementation of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function, replaces the pointer to the [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support function in the dispatch table with a pointer to its own implementation of the **WlxDialogBoxParam** function.</span></span> <span data-ttu-id="55c1e-132">如此一來，每次先前安裝的 GINA (通常 MsGina.dll) 呼叫 **WlxDialogBoxParam** 函式時，就會呼叫 GINA 勾點所執行的函式。</span><span class="sxs-lookup"><span data-stu-id="55c1e-132">As a result, each time the previously installed GINA (typically MsGina.dll) calls the **WlxDialogBoxParam** function, the function implemented by the GINA hook is called.</span></span>

<span data-ttu-id="55c1e-133">GINA 攔截所執行的 [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) 函數可以取代回應特定對話方塊事件的 [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) 回呼程式。</span><span class="sxs-lookup"><span data-stu-id="55c1e-133">The [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) function implemented by the GINA hook can replace the [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) callback procedure that responds to a specific dialog box event.</span></span>

<span data-ttu-id="55c1e-134">這可讓 GINA 攔截程式完全控制 MsGina.dll 所建立之所有對話方塊的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="55c1e-134">This gives the GINA hook full control over the appearance and behavior of all of the dialog boxes that MsGina.dll creates.</span></span>

<span data-ttu-id="55c1e-135">如需有關建立 GINA 攔截的詳細資訊，請參閱 \\ \\ Platform SDK 安裝的範例 Security \\ GINA \\ GinaHook 目錄中的 GINA 攔截範例。</span><span class="sxs-lookup"><span data-stu-id="55c1e-135">For more information about creating a GINA hook, see the Gina Hooks sample in the \\Samples\\Security\\Gina\\GinaHook directory of a Platform SDK installation.</span></span>

> [!Note]  
> <span data-ttu-id="55c1e-136">GINA 和 Winlogon 之間的所有呼叫都必須在單一線程內。</span><span class="sxs-lookup"><span data-stu-id="55c1e-136">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

 

 
