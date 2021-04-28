---
description: IShellDispatch4. GetSetting 方法-捕獲全域 Shell 設定。
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: 'IShellDispatch4. GetSetting 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a4345812925849831a6f0064c608f0c4be052c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116836"
---
# <a name="ishelldispatch4getsetting-method"></a><span data-ttu-id="c0c11-103">IShellDispatch4. GetSetting 方法</span><span class="sxs-lookup"><span data-stu-id="c0c11-103">IShellDispatch4.GetSetting method</span></span>

<span data-ttu-id="c0c11-104">捕獲全域 Shell 設定。</span><span class="sxs-lookup"><span data-stu-id="c0c11-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c11-105">語法</span><span class="sxs-lookup"><span data-stu-id="c0c11-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="c0c11-106">參數</span><span class="sxs-lookup"><span data-stu-id="c0c11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0c11-107">*lSetting* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c0c11-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0c11-108">類型： **long**</span><span class="sxs-lookup"><span data-stu-id="c0c11-108">Type: **long**</span></span>

<span data-ttu-id="c0c11-109">值，指定要取出的目前 Shell 設定。</span><span class="sxs-lookup"><span data-stu-id="c0c11-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="c0c11-110">每次呼叫中只能取出一個設定。</span><span class="sxs-lookup"><span data-stu-id="c0c11-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="c0c11-111">此方法可辨識下列值。</span><span class="sxs-lookup"><span data-stu-id="c0c11-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="c0c11-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_AUTOCHECKSELECT** (0x00800000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-113">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c0c11-113">**Windows Vista and later**.</span></span> <span data-ttu-id="c0c11-114">[ **使用核取方塊來選取專案** ] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="c0c11-115">當系統已設定畫筆輸入裝置時，會自動啟用此選項。</span><span class="sxs-lookup"><span data-stu-id="c0c11-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="c0c11-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_DESKTOPHTML** (0x00000200) </span><span class="sxs-lookup"><span data-stu-id="c0c11-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="c0c11-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_DONTPRETTYPATH** (0x00000800) </span><span class="sxs-lookup"><span data-stu-id="c0c11-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-119">[ **允許所有大寫名稱** ] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="c0c11-120">從 Windows Vista，此資料夾選項已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="c0c11-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_DOUBLECLICKINWEBVIEW** (0x00000080) </span><span class="sxs-lookup"><span data-stu-id="c0c11-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-122">**按兩下以開啟專案的狀態 (按一下以選取)** 選項。</span><span class="sxs-lookup"><span data-stu-id="c0c11-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="c0c11-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_篩選** (0x00010000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="c0c11-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_HIDDENFILEEXTS** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="c0c11-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="c0c11-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_HIDEICONS** (0x00004000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-128">圖示的狀態會顯示在 Windows 檔案總管清單視圖中。</span><span class="sxs-lookup"><span data-stu-id="c0c11-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="c0c11-129">如果此選項為使用中，則清單視圖中不會顯示任何圖示。</span><span class="sxs-lookup"><span data-stu-id="c0c11-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="c0c11-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ICONSONLY** (0x01000000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-131">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c0c11-131">**Windows Vista and later**.</span></span> <span data-ttu-id="c0c11-132">顯示名稱的狀態會顯示在 Windows 檔案總管清單視圖中。</span><span class="sxs-lookup"><span data-stu-id="c0c11-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="c0c11-133">如果此選項為 [使用中]，圖示就會顯示在清單視圖中，但不會顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c0c11-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="c0c11-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_MAPNETDRVBUTTON** (0x00001000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-135">[ **顯示對應網路磁碟機機] 按鈕在工具列選項中** 的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="c0c11-136">在 Windows Vista 中，此選項已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="c0c11-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_NOCONFIRMRECYCLE** (0x00008000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-138">資源回收筒的 [ **顯示刪除確認] 對話方塊** 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="c0c11-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_NONETCRAWLING** (0x00100000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-140">**自動搜尋網路資料夾和印表機** 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="c0c11-141">在 Windows Vista 中，此選項已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="c0c11-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_SEPPROCESS** (0x00080000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-143">**在不同的進程選項中開機檔案夾視窗** 的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="c0c11-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_SERVERADMINUI** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="c0c11-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-145">未使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="c0c11-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_SHOWALLOBJECTS** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="c0c11-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-147">[隱藏的檔案 **和資料夾** ] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="c0c11-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_SHOWATTRIBCOL** (0x00000100) </span><span class="sxs-lookup"><span data-stu-id="c0c11-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-149">**詳細資料檢視選項中顯示檔案屬性** 的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="c0c11-150">在 Windows Vista 中，此選項已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="c0c11-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_SHOWCOMPCOLOR** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="c0c11-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-152">[ **顯示已加密或壓縮的 NTFS** 檔案的色彩] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="c0c11-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_SHOWEXTENSIONS** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="c0c11-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-154">[ **隱藏已知檔案類型的副檔名** ] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="c0c11-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_SHOWINFOTIP** (0x00002000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-156">[ **顯示資料夾和桌面專案** 的快顯描述] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="c0c11-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_SHOWSTARTPAGE** (0x00400000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-158">未使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="c0c11-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_SHOWSUPERHIDDEN** (0x00040000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-160">[ **隱藏受保護的作業系統** 檔案] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="c0c11-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_SHOWSYSFILES** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="c0c11-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-162">[隱藏的檔案 **和資料夾** ] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="c0c11-163">在 Windows Vista 和更新版本中，這相當於 SSF \_ SHOWALLOBJECTS。</span><span class="sxs-lookup"><span data-stu-id="c0c11-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="c0c11-164">在 Windows Vista 之前的 Windows 版本中，此值指的是 [ **不要顯示隱藏的檔案和資料夾** ] 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="c0c11-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_SHOWTYPEOVERLAY** (0x02000000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-166">**Windows Vista**（含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c0c11-166">**Windows Vista and later**.</span></span> <span data-ttu-id="c0c11-167">**縮圖選項上顯示檔案圖示** 的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="c0c11-168">如果此選項為 [使用中]，當檔案提供縮圖表示時，會套用檔案類型重迭。</span><span class="sxs-lookup"><span data-stu-id="c0c11-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="c0c11-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_SORTCOLUMNS** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="c0c11-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-170">未使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="c0c11-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_STARTPANELON** (0x00200000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-172">Windows XP 顯示選項的狀態，會在 Windows XP 樣式和傳統樣式之間進行選取。</span><span class="sxs-lookup"><span data-stu-id="c0c11-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="c0c11-173">在 Windows Vista 中，此選項已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="c0c11-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_WEB** (0x00020000) </span><span class="sxs-lookup"><span data-stu-id="c0c11-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-175">**顯示為 web view 選項** 的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="c0c11-176">在 Windows Vista 中，此選項已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="c0c11-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_WIN95CLASSIC** (0x00000400) </span><span class="sxs-lookup"><span data-stu-id="c0c11-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="c0c11-178">**傳統樣式** 選項的狀態。</span><span class="sxs-lookup"><span data-stu-id="c0c11-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="c0c11-179">在 Windows Vista 中，此選項已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="c0c11-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0c11-180">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0c11-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c0c11-181">JScript</span><span class="sxs-lookup"><span data-stu-id="c0c11-181">JScript</span></span>

<span data-ttu-id="c0c11-182">Type： **VARIANT \_ BOOL \***</span><span class="sxs-lookup"><span data-stu-id="c0c11-182">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="c0c11-183">如果設定存在，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="c0c11-183">Set to **true** if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="c0c11-184">VB</span><span class="sxs-lookup"><span data-stu-id="c0c11-184">VB</span></span>

<span data-ttu-id="c0c11-185">Type： **VARIANT \_ BOOL \***</span><span class="sxs-lookup"><span data-stu-id="c0c11-185">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="c0c11-186">如果設定存在，則設定為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="c0c11-186">Set to **true** if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="c0c11-187">範例</span><span class="sxs-lookup"><span data-stu-id="c0c11-187">Examples</span></span>

<span data-ttu-id="c0c11-188">下列範例示範如何使用 JScript、VBScript 和 Visual Basic 的 **GetSetting** 。</span><span class="sxs-lookup"><span data-stu-id="c0c11-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c0c11-189">Jscript：</span><span class="sxs-lookup"><span data-stu-id="c0c11-189">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="c0c11-190">VBScript</span><span class="sxs-lookup"><span data-stu-id="c0c11-190">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
</script>
```



<span data-ttu-id="c0c11-191">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="c0c11-191">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c0c11-192">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0c11-192">Requirements</span></span>



| <span data-ttu-id="c0c11-193">需求</span><span class="sxs-lookup"><span data-stu-id="c0c11-193">Requirement</span></span> | <span data-ttu-id="c0c11-194">值</span><span class="sxs-lookup"><span data-stu-id="c0c11-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c11-195">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0c11-195">Minimum supported client</span></span><br/> | <span data-ttu-id="c0c11-196">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0c11-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="c0c11-197">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0c11-197">Minimum supported server</span></span><br/> | <span data-ttu-id="c0c11-198">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0c11-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c0c11-199">標頭</span><span class="sxs-lookup"><span data-stu-id="c0c11-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0c11-200"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0c11-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c0c11-201">Idl</span><span class="sxs-lookup"><span data-stu-id="c0c11-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0c11-202"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0c11-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c0c11-203">DLL</span><span class="sxs-lookup"><span data-stu-id="c0c11-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0c11-204"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="c0c11-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




