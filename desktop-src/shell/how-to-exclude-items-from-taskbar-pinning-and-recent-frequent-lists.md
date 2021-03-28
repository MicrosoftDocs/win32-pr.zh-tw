---
description: 應用程式、處理常式和 windows 可以選擇使其無法釘選到工作列，或包含在 [開始] 功能表最常使用的 (MFU) 清單中。
title: 如何從工作列釘選和最近/頻繁清單中排除專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973153"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a><span data-ttu-id="6205c-103">如何從工作列釘選和最近/頻繁清單中排除專案</span><span class="sxs-lookup"><span data-stu-id="6205c-103">How to Exclude Items from Taskbar Pinning and Recent/Frequent Lists</span></span>

<span data-ttu-id="6205c-104">應用程式、處理常式和 windows 可以選擇讓自己無法釘選到工作列，也可以包含在 [ **開始** ] 功能表最常使用的 (MFU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="6205c-104">Applications, processes, and windows can opt to make themselves unavailable for pinning to the taskbar or for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

## <a name="instructions"></a><span data-ttu-id="6205c-105">指示</span><span class="sxs-lookup"><span data-stu-id="6205c-105">Instructions</span></span>


<span data-ttu-id="6205c-106">有三種機制可以完成從工作列釘選和最近/頻繁清單中排除專案的機制：</span><span class="sxs-lookup"><span data-stu-id="6205c-106">There are three mechanisms to accomplish the exclusion of items from taskbar pinning and recent/frequent lists:</span></span>

-   <span data-ttu-id="6205c-107">將 NoStartPage 專案新增至應用程式的註冊，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="6205c-107">Add the NoStartPage entry to the application's registration as shown in this example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    <span data-ttu-id="6205c-108">與 NoStartPage 專案相關聯的資料會被忽略。</span><span class="sxs-lookup"><span data-stu-id="6205c-108">The data associated with the NoStartPage entry is ignored.</span></span> <span data-ttu-id="6205c-109">只需要存在專案。</span><span class="sxs-lookup"><span data-stu-id="6205c-109">Only the presence of the entry is required.</span></span> <span data-ttu-id="6205c-110">因此，NoStartPage 的理想型別為 **REG \_ NONE**。</span><span class="sxs-lookup"><span data-stu-id="6205c-110">Therefore, the ideal type for NoStartPage is **REG\_NONE**.</span></span>

    <span data-ttu-id="6205c-111">請注意，任何使用明確應用程式使用者模型識別碼 (AppUserModelID) 都會覆寫 NoStartPage 專案。</span><span class="sxs-lookup"><span data-stu-id="6205c-111">Note that any use of an explicit Application User Model ID (AppUserModelID) overrides the NoStartPage entry.</span></span> <span data-ttu-id="6205c-112">如果已將明確的 AppUserModelID 套用至快捷方式、程式或視窗，它就會變成可釘選，而且符合 [ **開始** ] 功能表的 最常使用清單的資格。</span><span class="sxs-lookup"><span data-stu-id="6205c-112">If an explicit AppUserModelID is applied to a shortcut, process, or window, it becomes pinnable and eligible for the **Start** menu MFU list.</span></span>

-   <span data-ttu-id="6205c-113">在 windows 和快捷方式上設定 [AppUserModel PreventPinning](../properties/props-system-appusermodel-preventpinning.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="6205c-113">Set the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property on windows and shortcuts.</span></span> <span data-ttu-id="6205c-114">在設定 [PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) 屬性之前，必須先在視窗上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="6205c-114">This property must be set on a window before the [PKEY\_AppUserModel\_ID](../properties/props-system-appusermodel-id.md) property is set.</span></span>
-   <span data-ttu-id="6205c-115">將明確的 AppUserModelID 新增為下列登錄子機碼底下的值，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="6205c-115">Add an explicit AppUserModelID as a value under the following registry subkey as shown in this example:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    <span data-ttu-id="6205c-116">每個專案都是具有 AppUserModelID 名稱的 **REG \_ Null** 值。</span><span class="sxs-lookup"><span data-stu-id="6205c-116">Each entry is a **REG\_NULL** value with the name of the AppUserModelID.</span></span> <span data-ttu-id="6205c-117">在此清單中找到的任何 AppUserModelID 都不會可釘選，也不適合包含在 [ **開始** ] 功能表的 最常使用清單中。</span><span class="sxs-lookup"><span data-stu-id="6205c-117">Any AppUserModelID that is found in this list is not pinnable and not eligible for inclusion in the **Start** menu MFU list.</span></span>

## <a name="remarks"></a><span data-ttu-id="6205c-118">備註</span><span class="sxs-lookup"><span data-stu-id="6205c-118">Remarks</span></span>

<span data-ttu-id="6205c-119">請注意，某些可執行檔，以及包含其名稱中特定字串的快捷方式，會自動排除在 最常使用清單中的固定和包含。</span><span class="sxs-lookup"><span data-stu-id="6205c-119">Be aware that certain executable files, as well as shortcuts that contain certain strings in their names, are automatically excluded from pinning and inclusion in the MFU list.</span></span>

> [!Note]  
> <span data-ttu-id="6205c-120">您可以套用明確的 AppUserModelID 來覆寫此自動排除。</span><span class="sxs-lookup"><span data-stu-id="6205c-120">This automatic exclusion can be overridden by applying an explicit AppUserModelID.</span></span>

 

<span data-ttu-id="6205c-121">如果下列任何一個字串（不論大小寫）都包含在快捷方式名稱中，則不會可釘選程式，也不會顯示在最常使用的清單中 (不適用於 Windows 10) ：</span><span class="sxs-lookup"><span data-stu-id="6205c-121">If any of the following strings, regardless of case, are included in the shortcut name, the program is not pinnable and is not displayed in the most frequently used list (not applicable to Windows 10):</span></span>

-   <span data-ttu-id="6205c-122">文件</span><span class="sxs-lookup"><span data-stu-id="6205c-122">Documentation</span></span>
-   <span data-ttu-id="6205c-123">Help</span><span class="sxs-lookup"><span data-stu-id="6205c-123">Help</span></span>
-   <span data-ttu-id="6205c-124">安裝</span><span class="sxs-lookup"><span data-stu-id="6205c-124">Install</span></span>
-   <span data-ttu-id="6205c-125">其他資訊</span><span class="sxs-lookup"><span data-stu-id="6205c-125">More Info</span></span>
-   <span data-ttu-id="6205c-126">自述</span><span class="sxs-lookup"><span data-stu-id="6205c-126">Read me</span></span>
-   <span data-ttu-id="6205c-127">先閱讀</span><span class="sxs-lookup"><span data-stu-id="6205c-127">Read First</span></span>
-   <span data-ttu-id="6205c-128">讀我檔案</span><span class="sxs-lookup"><span data-stu-id="6205c-128">Readme</span></span>
-   <span data-ttu-id="6205c-129">移除</span><span class="sxs-lookup"><span data-stu-id="6205c-129">Remove</span></span>
-   <span data-ttu-id="6205c-130">設定</span><span class="sxs-lookup"><span data-stu-id="6205c-130">Setup</span></span>
-   <span data-ttu-id="6205c-131">支援</span><span class="sxs-lookup"><span data-stu-id="6205c-131">Support</span></span>
-   <span data-ttu-id="6205c-132">新功能</span><span class="sxs-lookup"><span data-stu-id="6205c-132">What's New</span></span>

<span data-ttu-id="6205c-133">下列程式清單不是可釘選，而且會從最常使用的清單中排除：</span><span class="sxs-lookup"><span data-stu-id="6205c-133">The following list of programs are not pinnable and are excluded from the most frequently used list:</span></span>

-   <span data-ttu-id="6205c-134">Applaunch.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-134">Applaunch.exe</span></span>
-   <span data-ttu-id="6205c-135">Control.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-135">Control.exe</span></span>
-   <span data-ttu-id="6205c-136">Dfsvc.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-136">Dfsvc.exe</span></span>
-   <span data-ttu-id="6205c-137">Dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-137">Dllhost.exe</span></span>
-   <span data-ttu-id="6205c-138">Guestmodemsg.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-138">Guestmodemsg.exe</span></span>
-   <span data-ttu-id="6205c-139">Hh.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-139">Hh.exe</span></span>
-   <span data-ttu-id="6205c-140">Install.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-140">Install.exe</span></span>
-   <span data-ttu-id="6205c-141">Isuninst.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-141">Isuninst.exe</span></span>
-   <span data-ttu-id="6205c-142">Lnkstub.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-142">Lnkstub.exe</span></span>
-   <span data-ttu-id="6205c-143">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-143">Mmc.exe</span></span>
-   <span data-ttu-id="6205c-144">Mshta.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-144">Mshta.exe</span></span>
-   <span data-ttu-id="6205c-145">Msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-145">Msiexec.exe</span></span>
-   <span data-ttu-id="6205c-146">Msoobe.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-146">Msoobe.exe</span></span>
-   <span data-ttu-id="6205c-147">Rundll32.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-147">Rundll32.exe</span></span>
-   <span data-ttu-id="6205c-148">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-148">Setup.exe</span></span>
-   <span data-ttu-id="6205c-149">St5unst.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-149">St5unst.exe</span></span>
-   <span data-ttu-id="6205c-150">Unwise.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-150">Unwise.exe</span></span>
-   <span data-ttu-id="6205c-151">Unwise32.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-151">Unwise32.exe</span></span>
-   <span data-ttu-id="6205c-152">Werfault.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-152">Werfault.exe</span></span>
-   <span data-ttu-id="6205c-153">Winhlp32.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-153">Winhlp32.exe</span></span>
-   <span data-ttu-id="6205c-154">Wlrmdr.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-154">Wlrmdr.exe</span></span>
-   <span data-ttu-id="6205c-155">Wuapp.exe</span><span class="sxs-lookup"><span data-stu-id="6205c-155">Wuapp.exe</span></span>

<span data-ttu-id="6205c-156">上述的清單會儲存在下列登錄值中。</span><span class="sxs-lookup"><span data-stu-id="6205c-156">The preceding lists are stored in the following registry values.</span></span>

> [!Note]  
> <span data-ttu-id="6205c-157">應用程式不應修改這些清單。</span><span class="sxs-lookup"><span data-stu-id="6205c-157">These lists should not be modified by applications.</span></span> <span data-ttu-id="6205c-158">請使用本主題稍早所述的其中一個排除清單方法，以獲得相同的體驗。</span><span class="sxs-lookup"><span data-stu-id="6205c-158">Use one of the exclusion list methods described earlier in this topic for the same experience.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a><span data-ttu-id="6205c-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="6205c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6205c-160">工作列</span><span class="sxs-lookup"><span data-stu-id="6205c-160">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="6205c-161">工作列擴充功能</span><span class="sxs-lookup"><span data-stu-id="6205c-161">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
