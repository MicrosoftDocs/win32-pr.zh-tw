---
title: WFP Version-Independent 名稱，並以特定的 Windows 版本為目標
description: 在許多情況下， (WFP) API 的 Windows 篩選平台會提供一個以上版本的函式或結構。
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969028"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a><span data-ttu-id="a5c0a-103">WFP Version-Independent 名稱，並以特定的 Windows 版本為目標</span><span class="sxs-lookup"><span data-stu-id="a5c0a-103">WFP Version-Independent Names and Targeting Specific Versions of Windows</span></span>

<span data-ttu-id="a5c0a-104">在許多情況下， (WFP) API 的 Windows 篩選平台會提供一個以上版本的函式或結構。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-104">In many cases, the Windows Filtering Platform (WFP) API provides more than one version of a function or structure.</span></span>

<span data-ttu-id="a5c0a-105">WFP API 中大部分的資料和函式名稱都是以版本號碼結尾，例如 "0" 或 "1"，即使只有一個版本也是一樣。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-105">Most data and function names in the WFP API end with a version number, such as "0" or "1", even if there is only one version.</span></span>

## <a name="version-mapping-in-fwpvih"></a><span data-ttu-id="a5c0a-106">Fwpvi 中的版本對應</span><span class="sxs-lookup"><span data-stu-id="a5c0a-106">Version Mapping in fwpvi.h</span></span>

<span data-ttu-id="a5c0a-107">從 Windows 7 SDK 和 WDK 開始包含 fwpvi .h 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-107">The fwpvi.h header file is included starting with the Windows 7 SDK and WDK.</span></span> <span data-ttu-id="a5c0a-108">此標頭檔會將無版本 API 名稱對應至適用于指定作業系統的版本。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-108">This header file maps the versionless API name to the version that is appropriate for use with a given operating system.</span></span>

<span data-ttu-id="a5c0a-109">例如，以下是 Windows 8 SDK 中包含的 fwpvi 版本的簡短摘要。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-109">For example, here is a brief excerpt from the version of fwpvi.h included in the Windows 8 SDK.</span></span>


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



<span data-ttu-id="a5c0a-110">如上所示，只有一個版本的 **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) –因此任何對 **FwpmNetEventCreateEnumHandle** 的呼叫一律會呼叫 **FwpmNetEventCreateEnumHandle0**，不論目標作業系統為何。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-110">As shown above, there is only one version of **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – so any call to **FwpmNetEventCreateEnumHandle** will always call **FwpmNetEventCreateEnumHandle0**, regardless of the operating system targeted.</span></span>

<span data-ttu-id="a5c0a-111">不過，有三種版本的 **FwpmNetEventEnum**： [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)、 [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)和 [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-111">However, there are three versions of of **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1), and [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span></span> <span data-ttu-id="a5c0a-112">Fwpvi .h 標頭檔可確保對 **FwpmNetEventEnum** 的呼叫將會呼叫最適合目標作業系統的版本：</span><span class="sxs-lookup"><span data-stu-id="a5c0a-112">The fwpvi.h header file ensures that a call to **FwpmNetEventEnum** will call the version most appropriate to the targeted operating system:</span></span>

-   <span data-ttu-id="a5c0a-113">Windows 8 (或更新版本的 [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)) </span><span class="sxs-lookup"><span data-stu-id="a5c0a-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) for Windows 8 (or later)</span></span>
-   <span data-ttu-id="a5c0a-114">適用于 Windows 7 的 [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)為目標</span><span class="sxs-lookup"><span data-stu-id="a5c0a-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) for Windows 7 is targeted</span></span>
-   <span data-ttu-id="a5c0a-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) 舊版作業系統 (例如 windows Vista 或 Windows Vista Service Pack 1 (SP1) ) </span><span class="sxs-lookup"><span data-stu-id="a5c0a-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) for earlier operating systems (such as Windows Vista or Windows Vista with Service Pack 1 (SP1))</span></span>

## <a name="calling-version-independent-functions-and-structures"></a><span data-ttu-id="a5c0a-116">呼叫 Version-Independent 函式和結構</span><span class="sxs-lookup"><span data-stu-id="a5c0a-116">Calling Version-Independent Functions and Structures</span></span>

<span data-ttu-id="a5c0a-117">建議以特定作業系統或 WDK 版本為目標的 WFP 開發人員一律針對與版本無關的宏進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-117">WFP developers targeting a particular operating system or WDK version are encouraged to always program against the version-independent macros.</span></span> <span data-ttu-id="a5c0a-118">這會自動選取您的目標作業系統所支援的最新版本。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-118">This will automatically select the latest version supported in the operating system you are targeting.</span></span> <span data-ttu-id="a5c0a-119">建議使用最新的標頭檔，即使是以較早的作業系統為目標。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-119">Use of the most recent header files is recommended, even when targeting an earlier operating system.</span></span> <span data-ttu-id="a5c0a-120">以一致的方式進行，可確保使用最新的支援版本，也可以讓您更輕鬆地維護和更新程式碼。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-120">Doing this consistently will ensure the latest supported version is used, and can also make it easier to maintain and update your code.</span></span>

<span data-ttu-id="a5c0a-121">[WFP api 參考檔](fwp-reference.md)說明編號 API 的每個版本。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-121">The [WFP API reference documentation](fwp-reference.md) describes each version of a numbered API.</span></span> <span data-ttu-id="a5c0a-122">如果有一個以上的版本，則會注明目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-122">If more than one version exists, the targeted operating system is noted.</span></span> <span data-ttu-id="a5c0a-123">不過，開發人員通常會想要呼叫與版本無關的 (numberless) Api，並指出目標作業系統 (例如 **NTDDI \_ WIN6** for Windows Vista 或 **NTDDI \_ WIN8** for Windows 8) 。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-123">However, developers will generally want to call the version-independent (numberless) APIs, and indicate the targeted operating system (such as **NTDDI\_WIN6** for Windows Vista or **NTDDI\_WIN8** for Windows 8).</span></span>

<span data-ttu-id="a5c0a-124">為了確保正確處理在不同版本中採用不同參數的函式，您可以包含條件式區塊（例如） `#if (NTDDI_VERSION >= NTDDI_WIN7)` 。</span><span class="sxs-lookup"><span data-stu-id="a5c0a-124">To ensure proper handling of functions that take different parameters in different versions, you can include conditional blocks such as `#if (NTDDI_VERSION >= NTDDI_WIN7)`.</span></span>

 

 




