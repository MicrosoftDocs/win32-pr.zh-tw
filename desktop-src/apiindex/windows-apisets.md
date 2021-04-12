---
description: API 集合是核心 OS 中 Win32 Api 的功能群組。 它們提供與指定的 WIN32 API 定義所在的主機 DLL 以及 API 所屬的功能群組之間的架構分隔。
title: Windows API 集合
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 15c8e6ad8124abf06e6ab3c2a8ca2bcd83772855
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104463980"
---
# <a name="windows-api-sets"></a><span data-ttu-id="2714e-104">Windows API 集合</span><span class="sxs-lookup"><span data-stu-id="2714e-104">Windows API sets</span></span>

<span data-ttu-id="2714e-105">所有版本的 Windows 10 都會共用作業系統元件的通用基底，稱為 *核心 os* (在某些內容中，這個通用基底也稱為 *OneCore*) 。</span><span class="sxs-lookup"><span data-stu-id="2714e-105">All versions of Windows 10 share a common base of OS components that is called the *core OS* (in some contexts this common base is also called *OneCore*).</span></span> <span data-ttu-id="2714e-106">在核心 OS 元件中，Win32 Api 會組織成稱為 *API 集合* 的功能群組。</span><span class="sxs-lookup"><span data-stu-id="2714e-106">In core OS components, Win32 APIs are organized into functional groups called *API sets*.</span></span>

<span data-ttu-id="2714e-107">API 集的目的是要提供與主機 DLL （在其中執行指定的 WIN32 API）和 API 所屬的功能合約之間的架構分隔。</span><span class="sxs-lookup"><span data-stu-id="2714e-107">The purpose of an API set is to provide an architectural separation from the host DLL in which a given Win32 API is implemented and the functional contract to which the API belongs.</span></span> <span data-ttu-id="2714e-108">將 API 集合提供給開發人員與合約之間的分離，可為開發人員提供許多工程優勢。</span><span class="sxs-lookup"><span data-stu-id="2714e-108">The decoupling that API sets provide between implementation and contracts offers many engineering advantages for developers.</span></span> <span data-ttu-id="2714e-109">尤其是在您的程式碼中使用 API 集合，可以改善與所有 Windows 10 裝置的相容性。</span><span class="sxs-lookup"><span data-stu-id="2714e-109">In particular, using API sets in your code can improve compatibility with all Windows 10 devices.</span></span>

<span data-ttu-id="2714e-110">API 集合專門解決下列案例：</span><span class="sxs-lookup"><span data-stu-id="2714e-110">API sets specifically address the following scenarios:</span></span>

- <span data-ttu-id="2714e-111">雖然電腦上支援完整的 WIN32 API 範圍，但其他 Windows 10 裝置（例如 HoloLens、Xbox 和其他執行 Windows 10 的裝置）都只能使用 WIN32 API 的子集。</span><span class="sxs-lookup"><span data-stu-id="2714e-111">Although the full breadth of the Win32 API is supported on PCs, only a subset of the Win32 API is available on other Windows 10 devices such as HoloLens, Xbox, and other devices running Windows 10x.</span></span> <span data-ttu-id="2714e-112">API 集合名稱提供查詢機制，可完全偵測是否有任何特定裝置上的 API。</span><span class="sxs-lookup"><span data-stu-id="2714e-112">The API set name provides a query mechanism to cleanly detect whether an API is available on any given device.</span></span>

- <span data-ttu-id="2714e-113">某些 WIN32 API 的執行會存在於不同 Windows 10 裝置上具有不同名稱的 Dll 中。</span><span class="sxs-lookup"><span data-stu-id="2714e-113">Some Win32 API implementations exist in DLLs with different names across different Windows 10 devices.</span></span> <span data-ttu-id="2714e-114">偵測 API 可用性和延遲載入 Api 時，在偵測 api 可用性和延遲載入 Api 時使用 API 集合名稱（而不是 DLL 名稱）會提供正確的執行路由，不論 API 實際上的執行位置</span><span class="sxs-lookup"><span data-stu-id="2714e-114">Using API set names instead of DLL names when detecting API availability and delay loading APIs provide a correct route to the implementation no matter where the API is actually implemented.</span></span>

<span data-ttu-id="2714e-115">如需詳細資訊，請參閱 [api 集載入](api-set-loader-operation.md) 器作業和偵測 [api 設定的可用性](detect-api-set-availability.md)。</span><span class="sxs-lookup"><span data-stu-id="2714e-115">For more details, see [API set loader operation](api-set-loader-operation.md) and [Detect API set availability](detect-api-set-availability.md).</span></span>

## <a name="linking-to-umbrella-libraries"></a><span data-ttu-id="2714e-116">連結至傘程式庫</span><span class="sxs-lookup"><span data-stu-id="2714e-116">Linking to umbrella libraries</span></span>

<span data-ttu-id="2714e-117">為了讓您更輕鬆地將程式碼限制為核心 OS 所支援的 Win32 Api，我們提供一系列的一系列 *傘程式庫*。</span><span class="sxs-lookup"><span data-stu-id="2714e-117">To make it easier to restrict your code to Win32 APIs that are supported in the core OS, we provide a series of *umbrella libraries*.</span></span> <span data-ttu-id="2714e-118">例如，名為 OneCore 的傘程式庫會針對所有 Windows 10 裝置通用的 Win32 Api 子集提供匯出。</span><span class="sxs-lookup"><span data-stu-id="2714e-118">For example, an umbrella library named OneCore.lib provides the exports for the subset of Win32 APIs that are common to all Windows 10 devices.</span></span>

<span data-ttu-id="2714e-119">傘程式庫中的 Api 可以跨各種模組來實行。</span><span class="sxs-lookup"><span data-stu-id="2714e-119">The APIs in an umbrella library may be implemented across a range of modules.</span></span> <span data-ttu-id="2714e-120">傘程式庫會將這些詳細資料抽象化，讓您的程式碼更能在 Windows 10 版本和裝置之間移植。</span><span class="sxs-lookup"><span data-stu-id="2714e-120">The umbrella library abstracts those details away from you, making your code more portable across Windows 10 versions and devices.</span></span> <span data-ttu-id="2714e-121">與其連結至程式庫（例如 kernel32.dll .lib 和 advapi32.dll），只需將您的桌面應用程式或驅動程式連結至包含您感興趣之核心作業系統 Api 集合的傘程式庫。</span><span class="sxs-lookup"><span data-stu-id="2714e-121">Instead of linking to libraries such as kernel32.lib and advapi32.lib, simply link your desktop app or driver with the umbrella library that contains the set of core OS APIs that you're interested in.</span></span>

<span data-ttu-id="2714e-122">如需詳細資訊，請參閱 [Windows 傘程式庫](windows-umbrella-libraries.md)。</span><span class="sxs-lookup"><span data-stu-id="2714e-122">For more details, see [Windows umbrella libraries](windows-umbrella-libraries.md).</span></span>

## <a name="api-set-contract-names"></a><span data-ttu-id="2714e-123">API 集合合約名稱</span><span class="sxs-lookup"><span data-stu-id="2714e-123">API set contract names</span></span>

<span data-ttu-id="2714e-124">API 集會以強式合約名稱來識別，並遵循程式庫載入器所能辨識的這些標準慣例。</span><span class="sxs-lookup"><span data-stu-id="2714e-124">API sets are identified by a strong contract name that follows these standard conventions recognized by the library loader.</span></span> 

- <span data-ttu-id="2714e-125">名稱的開頭必須是字串 **api** 或 **ext**。</span><span class="sxs-lookup"><span data-stu-id="2714e-125">The name must begin either with the string **api-** or **ext-**.</span></span> 
    - <span data-ttu-id="2714e-126">以 **api** 開頭的名稱，代表保證存在於所有 Windows 10 版本上的 api。</span><span class="sxs-lookup"><span data-stu-id="2714e-126">Names that begin with **api-** represent APIs that are guaranteed to exist on all Windows 10 versions.</span></span>
    - <span data-ttu-id="2714e-127">以 **ext** 開頭的名稱代表可能不存在於所有 Windows 10 版本上的 api。</span><span class="sxs-lookup"><span data-stu-id="2714e-127">Names that begin with **ext-** represent APIs that may not exist on all Windows 10 versions.</span></span>
- <span data-ttu-id="2714e-128">名稱的結尾必須是序列 **l \<n\> - \<n\> - \<n\>**，其中 **n** 是由十進位數所組成。</span><span class="sxs-lookup"><span data-stu-id="2714e-128">The name must end with the sequence **l\<n\>-\<n\>-\<n\>**, where **n** consists of decimal digits.</span></span>
- <span data-ttu-id="2714e-129">名稱的本文可以是英數位元，也可以是連字號 (**-**) 。</span><span class="sxs-lookup"><span data-stu-id="2714e-129">The body of the name can be alphanumeric characters, or dashes (**-**).</span></span>
- <span data-ttu-id="2714e-130">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2714e-130">The name is case insensitive.</span></span>

<span data-ttu-id="2714e-131">以下是 API 集合約名稱的一些範例：</span><span class="sxs-lookup"><span data-stu-id="2714e-131">Here are some examples of API set contract names:</span></span>

- <span data-ttu-id="2714e-132">**api-ms-win--ums-l1-1-0**</span><span class="sxs-lookup"><span data-stu-id="2714e-132">**api-ms-win-core-ums-l1-1-0**</span></span>
- <span data-ttu-id="2714e-133">**ext-ms-ole32.lib-l1-1-5**</span><span class="sxs-lookup"><span data-stu-id="2714e-133">**ext-ms-win-com-ole32-l1-1-5**</span></span>
- <span data-ttu-id="2714e-134">**ext-ms-ntuser.man-window-l1-1-0**</span><span class="sxs-lookup"><span data-stu-id="2714e-134">**ext-ms-win-ntuser-window-l1-1-0**</span></span>
- <span data-ttu-id="2714e-135">**ext-ms-ntuser.man-window-l1-1-1**</span><span class="sxs-lookup"><span data-stu-id="2714e-135">**ext-ms-win-ntuser-window-l1-1-1**</span></span>

<span data-ttu-id="2714e-136">您可以在載入器作業的內容（例如 [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [P/Invoke](/dotnet/standard/native-interop/pinvoke) ）中使用 api 集合名稱，而不是 DLL 模組名稱，以確保在目前的裝置上實際實作為 API 的位置，使其正確路由。</span><span class="sxs-lookup"><span data-stu-id="2714e-136">You can use an API set name in the context of a loader operation such as [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [P/Invoke](/dotnet/standard/native-interop/pinvoke) instead of a DLL module name to ensure a correct route to the implementation no matter where the API is actually implemented on the current device.</span></span> <span data-ttu-id="2714e-137">但是，當您這樣做時，您必須在合約名稱的結尾附加字串 **.dll** 。</span><span class="sxs-lookup"><span data-stu-id="2714e-137">However, when you do this you must append the string **.dll** at the end of the contract name.</span></span> <span data-ttu-id="2714e-138">這是載入器必須正常運作的需求，且不會被視為合約名稱的一部分。</span><span class="sxs-lookup"><span data-stu-id="2714e-138">This is a requirement of the loader to function properly, and is not considered actually a part of the contract name.</span></span> <span data-ttu-id="2714e-139">雖然合約名稱在此內容中看起來類似 DLL 名稱，但它們基本上與 DLL 模組名稱不同，而且不會直接參考磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="2714e-139">Although contract names appear similar to DLL names in this context, they are fundamentally different from DLL module names and do not directly refer to a file on disk.</span></span>

<span data-ttu-id="2714e-140">除了在載入器作業中附加字串 **.dll** 之外，API 集合合約名稱也應視為與特定合約版本對應的不彈性識別碼。</span><span class="sxs-lookup"><span data-stu-id="2714e-140">Except for appending the string **.dll** in loader operations, API set contract names should be considered an immutable identifier that corresponds to a specific contract version.</span></span>

## <a name="identifying-api-sets-for-win32-apis"></a><span data-ttu-id="2714e-141">識別 Win32 Api 的 API 集合</span><span class="sxs-lookup"><span data-stu-id="2714e-141">Identifying API sets for Win32 APIs</span></span>

<span data-ttu-id="2714e-142">若要識別特定的 WIN32 API 是否屬於某個 API 集合，請參閱 API 參考檔中的需求資料表。</span><span class="sxs-lookup"><span data-stu-id="2714e-142">To identify whether a particular Win32 API belongs to an API set, review the requirements table in the reference documentation for the API.</span></span> <span data-ttu-id="2714e-143">如果 API 屬於 API 集，則文章中的需求資料表會列出 api 集合名稱，以及 api 首次引進 API 集的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="2714e-143">If the API belongs to an API set, the requirements table in the article lists the API set name and the Windows version in which the API was first introduced to the API set.</span></span> <span data-ttu-id="2714e-144">如需屬於 API 集合的 Api 範例，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="2714e-144">For examples of APIs that belong to an API set, see these articles:</span></span>

- [<span data-ttu-id="2714e-145">AllowSetForegroundWindow</span><span class="sxs-lookup"><span data-stu-id="2714e-145">AllowSetForegroundWindow</span></span>](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [<span data-ttu-id="2714e-146">FindWindowsEx</span><span class="sxs-lookup"><span data-stu-id="2714e-146">FindWindowsEx</span></span>](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [<span data-ttu-id="2714e-147">GetClassFile</span><span class="sxs-lookup"><span data-stu-id="2714e-147">GetClassFile</span></span>](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a><span data-ttu-id="2714e-148">本節內容</span><span class="sxs-lookup"><span data-stu-id="2714e-148">In this section</span></span>

* [<span data-ttu-id="2714e-149">API 集合載入器作業</span><span class="sxs-lookup"><span data-stu-id="2714e-149">API set loader operation</span></span>](api-set-loader-operation.md)
* [<span data-ttu-id="2714e-150">偵測 API 集合可用性</span><span class="sxs-lookup"><span data-stu-id="2714e-150">Detect API set availability</span></span>](detect-api-set-availability.md)
* [<span data-ttu-id="2714e-151">Windows 傘程式庫</span><span class="sxs-lookup"><span data-stu-id="2714e-151">Windows umbrella libraries</span></span>](windows-umbrella-libraries.md)