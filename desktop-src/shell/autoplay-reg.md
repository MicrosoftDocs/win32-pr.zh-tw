---
description: 在許多情況下，自動安裝可能需要暫時或持續停用。
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: 啟用和停用自動啟動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567f50db75cd129346e193e66ba0ae5f74fa955
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386122"
---
# <a name="enabling-and-disabling-autorun"></a><span data-ttu-id="d3017-103">啟用和停用自動啟動</span><span class="sxs-lookup"><span data-stu-id="d3017-103">Enabling and Disabling AutoRun</span></span>

<span data-ttu-id="d3017-104">在許多情況下，自動安裝可能需要暫時或持續停用。</span><span class="sxs-lookup"><span data-stu-id="d3017-104">There are many situations where AutoRun may need to be temporarily or persistently disabled.</span></span> <span data-ttu-id="d3017-105">例如，自動執行可能會干擾正在執行之應用程式的作業，而且必須在持續期間內停用。</span><span class="sxs-lookup"><span data-stu-id="d3017-105">For example, AutoRun might interfere with the operation of a running application and need to be disabled for the duration.</span></span> <span data-ttu-id="d3017-106">系統提供數種方式來停用自動運行。</span><span class="sxs-lookup"><span data-stu-id="d3017-106">The system provides several ways to disable AutoRun.</span></span>

-   [<span data-ttu-id="d3017-107">以程式設計方式隱藏自動運行</span><span class="sxs-lookup"><span data-stu-id="d3017-107">Suppressing AutoRun Programmatically</span></span>](#suppressing-autorun-programmatically)
-   [<span data-ttu-id="d3017-108">使用登錄來停用自動播放</span><span class="sxs-lookup"><span data-stu-id="d3017-108">Using the Registry to Disable AutoRun</span></span>](#using-the-registry-to-disable-autorun)
-   [<span data-ttu-id="d3017-109">其他類型儲存體媒體的自動運行</span><span class="sxs-lookup"><span data-stu-id="d3017-109">AutoRun for Other Types of Storage Media</span></span>](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a><span data-ttu-id="d3017-110">以程式設計方式隱藏自動運行</span><span class="sxs-lookup"><span data-stu-id="d3017-110">Suppressing AutoRun Programmatically</span></span>

<span data-ttu-id="d3017-111">有許多情況下，可能需要以程式設計的方式隱藏自動安裝。</span><span class="sxs-lookup"><span data-stu-id="d3017-111">There are a variety of situations where AutoRun may need to be suppressed programmatically.</span></span> <span data-ttu-id="d3017-112">以下為兩個範例：</span><span class="sxs-lookup"><span data-stu-id="d3017-112">Two examples are:</span></span>

-   <span data-ttu-id="d3017-113">您的應用程式有一個安裝程式，要求使用者插入另一個可能包含自動播放 .inf 檔案的光碟片。</span><span class="sxs-lookup"><span data-stu-id="d3017-113">Your application has a setup program that requires the user to insert another disc that may contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="d3017-114">在應用程式的作業期間，使用者可能需要插入另一張可能包含自動執行 .inf 檔案的光碟片。</span><span class="sxs-lookup"><span data-stu-id="d3017-114">During the operation of your application, the user may need to insert another disc that may contain an Autorun.inf file.</span></span>

<span data-ttu-id="d3017-115">在任一種情況下，您通常不會想要在原始進行中時啟動另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="d3017-115">In either case, you will normally not want to launch another application while the original is in progress.</span></span>

<span data-ttu-id="d3017-116">使用者可以在插入 cd-rom 時按住 SHIFT 鍵，以手動隱藏自動安裝。</span><span class="sxs-lookup"><span data-stu-id="d3017-116">Users can manually suppress AutoRun by holding down the SHIFT key when they insert the CD-ROM.</span></span> <span data-ttu-id="d3017-117">不過，通常最好是以程式設計方式處理這項作業，而不是根據使用者。</span><span class="sxs-lookup"><span data-stu-id="d3017-117">However, it is usually preferable to handle this operation programmatically rather than depending on the user.</span></span>

<span data-ttu-id="d3017-118">使用具有 Shell [4.70 版](versions.md) 和更新版本的系統，Windows 會將 "QueryCancelAutoPlay" 訊息傳送到前景視窗。</span><span class="sxs-lookup"><span data-stu-id="d3017-118">With systems that have Shell [version 4.70](versions.md) and later, Windows sends a "QueryCancelAutoPlay" message to the foreground window.</span></span> <span data-ttu-id="d3017-119">您的應用程式可以回應此訊息以抑制自動運行。</span><span class="sxs-lookup"><span data-stu-id="d3017-119">Your application can respond to this message to suppress AutoRun.</span></span> <span data-ttu-id="d3017-120">這種方法是由系統公用程式（例如 [ [開啟](../dlgbox/open-and-save-as-dialog-boxes.md) 一般] 對話方塊）用來停用自動運行。</span><span class="sxs-lookup"><span data-stu-id="d3017-120">This approach is used by system utilities such as the [Open](../dlgbox/open-and-save-as-dialog-boxes.md) common dialog box to disable AutoRun.</span></span>

<span data-ttu-id="d3017-121">下列程式碼片段說明如何設定和處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="d3017-121">The following code fragments illustrate how to set up and handle this message.</span></span> <span data-ttu-id="d3017-122">您的應用程式必須在前景視窗中執行。</span><span class="sxs-lookup"><span data-stu-id="d3017-122">Your application must be running in the foreground window.</span></span> <span data-ttu-id="d3017-123">首先，將 "QueryCancelAutoPlay" 註冊為 Windows 訊息：</span><span class="sxs-lookup"><span data-stu-id="d3017-123">First, register "QueryCancelAutoPlay" as a Windows message:</span></span>


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



<span data-ttu-id="d3017-124">您應用程式的視窗必須在前景才能接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d3017-124">Your application's window must be in the foreground to receive this message.</span></span> <span data-ttu-id="d3017-125">訊息處理常式應該會傳回 **TRUE** 以取消自動運行，並傳回 **FALSE** 來啟用它。</span><span class="sxs-lookup"><span data-stu-id="d3017-125">The message handler should return **TRUE** to cancel AutoRun and **FALSE** to enable it.</span></span> <span data-ttu-id="d3017-126">下列程式碼片段說明如何使用此訊息來停用自動執行。</span><span class="sxs-lookup"><span data-stu-id="d3017-126">The following code fragment illustrates how to use this message to disable AutoRun.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



<span data-ttu-id="d3017-127">如果您的應用程式使用對話方塊，而且必須回應 "QueryCancelAutoPlay" 訊息，則不會直接傳回 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d3017-127">If your application is using a dialog box and needs to respond to a "QueryCancelAutoPlay" message, it cannot simply return **TRUE** or **FALSE**.</span></span> <span data-ttu-id="d3017-128">請改為呼叫 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ，並將 *NIndex* 設定為 **DWL \_ MSGRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d3017-128">Instead, call [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) with *nIndex* set to **DWL\_MSGRESULT**.</span></span> <span data-ttu-id="d3017-129">將 *dwNewLong* 參數設定為 **TRUE** 以取消自動啟動，並將 FALSE 設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d3017-129">Set the *dwNewLong* parameter to **TRUE** to cancel AutoRun, and **FALSE** to enable it.</span></span> <span data-ttu-id="d3017-130">例如，下列範例對話方塊程式會在收到「QueryCancelAutoPlay」訊息時，取消自動執行。</span><span class="sxs-lookup"><span data-stu-id="d3017-130">For example, the following sample dialog box procedure cancels AutoRun when it receives a "QueryCancelAutoPlay" message.</span></span>


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a><span data-ttu-id="d3017-131">使用登錄來停用自動播放</span><span class="sxs-lookup"><span data-stu-id="d3017-131">Using the Registry to Disable AutoRun</span></span>

<span data-ttu-id="d3017-132">有兩個可用來持續停用自動執行的登錄值： NoDriveAutoRun 和 NoDriveTypeAutoRun。</span><span class="sxs-lookup"><span data-stu-id="d3017-132">There are two registry values that can be used to persistently disable AutoRun: NoDriveAutoRun and NoDriveTypeAutoRun.</span></span> <span data-ttu-id="d3017-133">第一個值會停用指定磁碟機號的自動運行，而第二個值會停用磁片磁碟機類別的自動運行。</span><span class="sxs-lookup"><span data-stu-id="d3017-133">The first value disables AutoRun for specified drive letters and the second disables AutoRun for a class of drives.</span></span> <span data-ttu-id="d3017-134">如果其中一個值設定為停用特定裝置的自動安裝，則會停用。</span><span class="sxs-lookup"><span data-stu-id="d3017-134">If either of these values is set to disable AutoRun for a particular device, it will be disabled.</span></span> <span data-ttu-id="d3017-135">如需停用自動播放功能的詳細資訊，請參閱知識庫文章 [如何停用 Windows 中的自動播放功能](https://support.microsoft.com/kb/967715) 。</span><span class="sxs-lookup"><span data-stu-id="d3017-135">See the Knowledge Base article [How to disable the Autorun functionality in Windows](https://support.microsoft.com/kb/967715) for more information on disabling AutoRun functionality.</span></span> <span data-ttu-id="d3017-136">本文列出您必須安裝才能正確停用自動播放功能的不同更新。</span><span class="sxs-lookup"><span data-stu-id="d3017-136">This article lists the different updates that you must have installed to correctly disable the Autorun functionality.</span></span>

> [!Note]  
> <span data-ttu-id="d3017-137">NoDriveAutoRun 和 NoDriveTypeAutoRun 值只能由系統管理員修改，以變更整個系統的值，以供測試或管理之用。</span><span class="sxs-lookup"><span data-stu-id="d3017-137">The NoDriveAutoRun and NoDriveTypeAutoRun values should only be modified by system administrators to change the value for the entire system for testing or administrative purposes.</span></span> <span data-ttu-id="d3017-138">應用程式不應該修改這些值，因為無法將它們可靠地還原為其原始值。</span><span class="sxs-lookup"><span data-stu-id="d3017-138">Applications should not modify these values, as there is no way to reliably restore them to their original values.</span></span>

 

<span data-ttu-id="d3017-139">NoDriveAutoRun 值會停用指定磁碟機號的自動運行。</span><span class="sxs-lookup"><span data-stu-id="d3017-139">The NoDriveAutoRun value disables AutoRun for specified drive letters.</span></span> <span data-ttu-id="d3017-140">它是登錄 \_ 的 DWORD 資料值，可在下列機碼下找到：</span><span class="sxs-lookup"><span data-stu-id="d3017-140">It is a REG\_DWORD data value, found under the following key:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="d3017-141">值的第一個位對應到磁片磁碟機 A：，第二個是 B：，依此類推。</span><span class="sxs-lookup"><span data-stu-id="d3017-141">The first bit of the value corresponds to drive A:, the second to B:, and so on.</span></span> <span data-ttu-id="d3017-142">若要停用一或多個磁碟機號的自動播放，請設定對應的位。</span><span class="sxs-lookup"><span data-stu-id="d3017-142">To disable AutoRun for one or more drive letters, set the corresponding bits.</span></span> <span data-ttu-id="d3017-143">例如，若要停用 A：和 C：磁片磁碟機，請將 NoDriveAutoRun 設定為 `0x00000005` 。</span><span class="sxs-lookup"><span data-stu-id="d3017-143">For example, to disable the A: and C: drives, set NoDriveAutoRun to `0x00000005`.</span></span>

<span data-ttu-id="d3017-144">NoDriveTypeAutoRun 值會停用磁片磁碟機類別的自動運行。</span><span class="sxs-lookup"><span data-stu-id="d3017-144">The NoDriveTypeAutoRun value disables AutoRun for a class of drives.</span></span> <span data-ttu-id="d3017-145">它是登錄 \_ DWORD 或4位元組的 reg \_ 二進位資料值，可在相同的索引鍵下找到。</span><span class="sxs-lookup"><span data-stu-id="d3017-145">It is a REG\_DWORD or 4-byte REG\_BINARY data value, found under the same key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

<span data-ttu-id="d3017-146">藉由設定此值的第一個位元組的位，可以排除不同的磁片磁碟機，而不使用自動執行。</span><span class="sxs-lookup"><span data-stu-id="d3017-146">By setting the bits of this value's first byte, different drives can be excluded from working with AutoRun.</span></span>

<span data-ttu-id="d3017-147">下表提供位和位元遮罩常數，可在 NoDriveTypeAutoRun 的第一個位元組中設定，以停用特定磁片磁碟機類型的自動執行。</span><span class="sxs-lookup"><span data-stu-id="d3017-147">The following table gives the bits and bitmask constants, that can be set in the first byte of NoDriveTypeAutoRun to disable AutoRun for a particular drive type.</span></span> <span data-ttu-id="d3017-148">您必須重新開機 Windows 檔案總管，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="d3017-148">You must restart Windows Explorer before the changes take effect.</span></span>



| <span data-ttu-id="d3017-149">位數位</span><span class="sxs-lookup"><span data-stu-id="d3017-149">Bit Number</span></span> | <span data-ttu-id="d3017-150">位元遮罩常數</span><span class="sxs-lookup"><span data-stu-id="d3017-150">Bitmask Constant</span></span>      | <span data-ttu-id="d3017-151">Description</span><span class="sxs-lookup"><span data-stu-id="d3017-151">Description</span></span>                                             |
|------------|-----------------------|---------------------------------------------------------|
| <span data-ttu-id="d3017-152">0x04</span><span class="sxs-lookup"><span data-stu-id="d3017-152">0x04</span></span>       | <span data-ttu-id="d3017-153">**磁片磁碟機 \_ 可移動**</span><span class="sxs-lookup"><span data-stu-id="d3017-153">**DRIVE\_REMOVEABLE**</span></span> | <span data-ttu-id="d3017-154">磁片可以從磁片磁碟機 (（例如磁片) ）移除。</span><span class="sxs-lookup"><span data-stu-id="d3017-154">Disk can be removed from drive (such as a floppy disk).</span></span> |
| <span data-ttu-id="d3017-155">0x08</span><span class="sxs-lookup"><span data-stu-id="d3017-155">0x08</span></span>       | <span data-ttu-id="d3017-156">**磁片磁碟機 \_ 修正**</span><span class="sxs-lookup"><span data-stu-id="d3017-156">**DRIVE\_FIXED**</span></span>      | <span data-ttu-id="d3017-157">無法從磁片磁碟機 (硬碟) 中移除磁片。</span><span class="sxs-lookup"><span data-stu-id="d3017-157">Disk cannot be removed from drive (a hard disk).</span></span>        |
| <span data-ttu-id="d3017-158">0x10</span><span class="sxs-lookup"><span data-stu-id="d3017-158">0x10</span></span>       | <span data-ttu-id="d3017-159">**遠端磁片磁碟機 \_**</span><span class="sxs-lookup"><span data-stu-id="d3017-159">**DRIVE\_REMOTE**</span></span>     | <span data-ttu-id="d3017-160">網路磁碟機機。</span><span class="sxs-lookup"><span data-stu-id="d3017-160">Network drive.</span></span>                                          |
| <span data-ttu-id="d3017-161">0x20</span><span class="sxs-lookup"><span data-stu-id="d3017-161">0x20</span></span>       | <span data-ttu-id="d3017-162">**光碟機 \_ 磁片磁碟機**</span><span class="sxs-lookup"><span data-stu-id="d3017-162">**DRIVE\_CDROM**</span></span>      | <span data-ttu-id="d3017-163">CD-ROM 光碟機。</span><span class="sxs-lookup"><span data-stu-id="d3017-163">CD-ROM drive.</span></span>                                           |
| <span data-ttu-id="d3017-164">0x40</span><span class="sxs-lookup"><span data-stu-id="d3017-164">0x40</span></span>       | <span data-ttu-id="d3017-165">**驅動 \_ RAMDISK**</span><span class="sxs-lookup"><span data-stu-id="d3017-165">**DRIVE\_RAMDISK**</span></span>    | <span data-ttu-id="d3017-166">RAM 磁碟。</span><span class="sxs-lookup"><span data-stu-id="d3017-166">RAM disk.</span></span>                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a><span data-ttu-id="d3017-167">其他類型儲存體媒體的自動運行</span><span class="sxs-lookup"><span data-stu-id="d3017-167">AutoRun for Other Types of Storage Media</span></span>

<span data-ttu-id="d3017-168">自動執行主要是用來在 CD-ROM 和 DVD-ROM 上將應用程式公開散發，而且不建議將其用於其他儲存體媒體。</span><span class="sxs-lookup"><span data-stu-id="d3017-168">AutoRun is primarily intended for public distribution of applications on CD-ROM and DVD-ROM, and its use is discouraged for other storage media.</span></span> <span data-ttu-id="d3017-169">不過，在其他類型的卸除式存放裝置媒體上啟用自動啟動通常會很有用。</span><span class="sxs-lookup"><span data-stu-id="d3017-169">However, it is often useful to enable AutoRun on other types of removable storage media.</span></span> <span data-ttu-id="d3017-170">這項功能通常是用來簡化自動播放 .inf 檔案的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="d3017-170">This feature is typically used simplify the debugging of AutoRun.inf files.</span></span> <span data-ttu-id="d3017-171">當符合下列準則時，自動執行只適用于卸除式存放裝置裝置：</span><span class="sxs-lookup"><span data-stu-id="d3017-171">AutoRun only works on removable storage devices when the following criteria are met:</span></span>

-   <span data-ttu-id="d3017-172">裝置必須具有自動運行時相容的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d3017-172">The device must have AutoRun-compatible drivers.</span></span> <span data-ttu-id="d3017-173">若要與自動相容，驅動程式必須透過傳送 [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) 訊息，通知系統已插入磁片。</span><span class="sxs-lookup"><span data-stu-id="d3017-173">To be AutoRun-compatible, a driver must notify the system that a disk has been inserted by sending a [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) message.</span></span>
-   <span data-ttu-id="d3017-174">插入之媒體的根目錄必須包含自動運行的 .inf 檔案。</span><span class="sxs-lookup"><span data-stu-id="d3017-174">The root directory of the inserted media must contain an Autorun.inf file.</span></span>
-   <span data-ttu-id="d3017-175">裝置不能透過登錄停用自動執行[。](#using-the-registry-to-disable-autorun)</span><span class="sxs-lookup"><span data-stu-id="d3017-175">The device must not have AutoRun disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>
-   <span data-ttu-id="d3017-176">前景應用程式未 [隱藏](#suppressing-autorun-programmatically) 自動運行。</span><span class="sxs-lookup"><span data-stu-id="d3017-176">The foreground application has not [suppressed](#suppressing-autorun-programmatically) AutoRun.</span></span>

> [!Note]  
> <span data-ttu-id="d3017-177">這項功能不應用來將應用程式散發至卸載式媒體。</span><span class="sxs-lookup"><span data-stu-id="d3017-177">This feature should not be used to distribute applications on removable media.</span></span> <span data-ttu-id="d3017-178">由於在卸載式媒體上執行自動執行可提供簡單的方式來散佈電腦病毒，因此使用者應該會懷疑包含自動執行 .inf 檔案的任何公開分散式磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d3017-178">Because implementing AutoRun on removable media provides an easy way to spread computer viruses, users should be suspicious of any publicly distributed floppy disk that contains an Autorun.inf file.</span></span>

 

<span data-ttu-id="d3017-179">通常，自動啟動會自動啟動，但也可以手動啟動。</span><span class="sxs-lookup"><span data-stu-id="d3017-179">Normally, AutoRun starts automatically, but it can also be started manually.</span></span> <span data-ttu-id="d3017-180">如果裝置符合上面所列的條件，磁碟機號的快捷方式功能表就會包含 [ **自動播放** ] 命令。</span><span class="sxs-lookup"><span data-stu-id="d3017-180">If the device meets the criteria listed above, the drive letter's shortcut menu will include an **AutoPlay** command.</span></span> <span data-ttu-id="d3017-181">若要手動執行自動執行，請在磁片磁碟機圖示上按一下滑鼠右鍵，然後從快捷方式功能表選取 [ **自動播放** ]，或按兩下磁片磁碟機圖示。</span><span class="sxs-lookup"><span data-stu-id="d3017-181">To run AutoRun manually, either right-click the drive icon and select **AutoPlay** from the shortcut menu or double-click the drive icon.</span></span> <span data-ttu-id="d3017-182">如果驅動程式不相容，則快捷方式功能表將不會有 [ **自動播放** ] 專案，而且無法啟動自動啟動。</span><span class="sxs-lookup"><span data-stu-id="d3017-182">If the drivers are not AutoRun-compatible, the shortcut menu will not have an **AutoPlay** item and AutoRun cannot be started.</span></span>

<span data-ttu-id="d3017-183">自動運行時相容的驅動程式會隨附于一些卸載式磁片磁碟機，以及一些其他類型的卸載式媒體，例如 CompactFlash 卡。</span><span class="sxs-lookup"><span data-stu-id="d3017-183">AutoRun-compatible drivers are provided with some removable disk drives, as well as some other types of removable media such as CompactFlash cards.</span></span> <span data-ttu-id="d3017-184">自動播放也適用于對應至磁碟機號 Windows 檔案總管的網路磁碟機機，或透過 [Microsoft Management Console (MMC) ](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page)掛接。</span><span class="sxs-lookup"><span data-stu-id="d3017-184">AutoRun also works with network drives that are mapped to a drive letter with Windows Explorer or mounted with the [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page).</span></span> <span data-ttu-id="d3017-185">如同掛接的硬體一樣，掛接的網路磁碟機機在其根目錄中必須有執行中的 .inf 檔案，而且不得透過登錄來停[用。](#using-the-registry-to-disable-autorun)</span><span class="sxs-lookup"><span data-stu-id="d3017-185">As with mounted hardware, a mounted network drive must have an Autorun.inf file in its root directory, and must not be disabled through the [registry](#using-the-registry-to-disable-autorun).</span></span>

 

 
