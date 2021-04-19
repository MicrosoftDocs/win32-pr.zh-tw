---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: 移除 Windows 登錄反映
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975471"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="5d970-103">移除 Windows 登錄反映</span><span class="sxs-lookup"><span data-stu-id="5d970-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="5d970-104">平台</span><span class="sxs-lookup"><span data-stu-id="5d970-104">Platform</span></span>

<span data-ttu-id="5d970-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="5d970-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="5d970-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5d970-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="5d970-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="5d970-107">Feature Impact</span></span>

 <span data-ttu-id="5d970-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="5d970-108">**Severity** - Low</span></span>  
<span data-ttu-id="5d970-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="5d970-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="5d970-110">Description</span><span class="sxs-lookup"><span data-stu-id="5d970-110">Description</span></span>

<span data-ttu-id="5d970-111">登錄反映程式會在兩個登錄視圖之間複製登錄機碼和值，讓它們保持同步。在64舊版的 Windows 中，此程式會反映32位和64位之間的重新導向登錄機碼子集。</span><span class="sxs-lookup"><span data-stu-id="5d970-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="5d970-112">但是，這種方式的執行會導致登錄的狀態不一致。</span><span class="sxs-lookup"><span data-stu-id="5d970-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="5d970-113"> (如需登錄反映的詳細資訊，請參閱下面的 *其他資源連結* 中的對應 MSDN 文章。 ) </span><span class="sxs-lookup"><span data-stu-id="5d970-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="5d970-114">從 Windows 7 開始，我們已完全移除登錄反映，併合並用來反映的金鑰：</span><span class="sxs-lookup"><span data-stu-id="5d970-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="5d970-115">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別</span><span class="sxs-lookup"><span data-stu-id="5d970-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="5d970-116">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ COM3</span><span class="sxs-lookup"><span data-stu-id="5d970-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="5d970-117">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="5d970-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="5d970-118">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Ole</span><span class="sxs-lookup"><span data-stu-id="5d970-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="5d970-119">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Rpc</span><span class="sxs-lookup"><span data-stu-id="5d970-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="5d970-120">HKEY \_ 使用者 \\ \* \\ 軟體 \\ 類別</span><span class="sxs-lookup"><span data-stu-id="5d970-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="5d970-121">HKEY \_ USERS \\ \* \_ 類別</span><span class="sxs-lookup"><span data-stu-id="5d970-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="5d970-122">實際上，這會提供相同的反映行為，因為這些金鑰的變更會立即適用于32位和64位應用程式。</span><span class="sxs-lookup"><span data-stu-id="5d970-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="5d970-123">有條件地反映的索引鍵會保持分割：</span><span class="sxs-lookup"><span data-stu-id="5d970-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="5d970-124">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="5d970-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="5d970-125">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ 介面</span><span class="sxs-lookup"><span data-stu-id="5d970-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="5d970-126">HKEY \_ 使用者 \\ \* \\ 軟體 \\ 類別 \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="5d970-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="5d970-127">HKEY \_ 使用者 \\ \* \\ 軟體 \\ 類別 \\ 介面</span><span class="sxs-lookup"><span data-stu-id="5d970-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="5d970-128">HKEY \_ 使用者 \\ \* \_ 類別 \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="5d970-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="5d970-129">HKEY \_ 使用者 \\ \* \_ 類別 \\ 介面</span><span class="sxs-lookup"><span data-stu-id="5d970-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="5d970-130">它們是用來保留不應在32位和64位應用程式之間共用的資料。</span><span class="sxs-lookup"><span data-stu-id="5d970-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="5d970-131">表現</span><span class="sxs-lookup"><span data-stu-id="5d970-131">Manifestation</span></span>

<span data-ttu-id="5d970-132">上述清單中的 CLSID 和介面金鑰在仍重新導向時，不會再反映出來。</span><span class="sxs-lookup"><span data-stu-id="5d970-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="5d970-133">雖然在大部分情況下，這是所需的行為，但應用程式可能會相依于 Vista 中反映的行為。</span><span class="sxs-lookup"><span data-stu-id="5d970-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="5d970-134">允許應用程式控制反映 (RegDisableReflectionKey 和 RegEnableReflectionKey) 的函式在 Windows 7 中不是 ops。</span><span class="sxs-lookup"><span data-stu-id="5d970-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="5d970-135">影響緩和措施</span><span class="sxs-lookup"><span data-stu-id="5d970-135">Mitigation of Impact</span></span>

<span data-ttu-id="5d970-136">COM 是登錄反映的主要取用者。</span><span class="sxs-lookup"><span data-stu-id="5d970-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="5d970-137">已更新 COM 和其他取用者以配合此變更。</span><span class="sxs-lookup"><span data-stu-id="5d970-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="5d970-138">此變更不會影響使用標準 COM Api 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5d970-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="5d970-139">解決方法</span><span class="sxs-lookup"><span data-stu-id="5d970-139">Solution</span></span>

<span data-ttu-id="5d970-140">如果您要依賴登錄反映來同步處理32位和64位的視圖，請套用下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="5d970-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="5d970-141">在安裝期間明確地在這兩個視圖中建立金鑰</span><span class="sxs-lookup"><span data-stu-id="5d970-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="5d970-142">將金鑰移出反映的索引鍵範圍</span><span class="sxs-lookup"><span data-stu-id="5d970-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="5d970-143">查詢反映的金鑰時，檢查登錄的兩個視圖</span><span class="sxs-lookup"><span data-stu-id="5d970-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="5d970-144">**注意：**\_ \_ 無法合併 key wow64 32KEY 和 key \_ wow64 \_ 64KEY 旗標</span><span class="sxs-lookup"><span data-stu-id="5d970-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="5d970-145">如果您要依賴 RegDisableReflectionKey 函式來停用登錄反映，請套用下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="5d970-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="5d970-146">在安裝期間明確地在這兩個視圖中建立金鑰</span><span class="sxs-lookup"><span data-stu-id="5d970-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="5d970-147">將金鑰移出反映的索引鍵範圍</span><span class="sxs-lookup"><span data-stu-id="5d970-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="5d970-148">使用平臺特定的子機碼 (例如 x86、amd64 和 ia64) 來分隔位特定的資料</span><span class="sxs-lookup"><span data-stu-id="5d970-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="5d970-149">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="5d970-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="5d970-150">登錄反映文章</span><span class="sxs-lookup"><span data-stu-id="5d970-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="5d970-151">登錄重新導向程式文章中的重新導向金鑰清單</span><span class="sxs-lookup"><span data-stu-id="5d970-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="5d970-152">Wow64 的最佳作法</span><span class="sxs-lookup"><span data-stu-id="5d970-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="5d970-153">這些資源可能無法在某些語言及國家/地區中使用。</span><span class="sxs-lookup"><span data-stu-id="5d970-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
