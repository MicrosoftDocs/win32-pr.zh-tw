---
description: Windows API 的參考內容清單。
ms.assetid: 9CA123F9-92F1-4761-9468-266DA422F70E
title: Windows API 索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cace235af1c729e450bdf99b276eca1bfc000
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106993462"
---
# <a name="windows-api-index"></a><span data-ttu-id="93f9d-103">Windows API 索引</span><span class="sxs-lookup"><span data-stu-id="93f9d-103">Windows API index</span></span>

<span data-ttu-id="93f9d-104">以下是適用于桌面和伺服器應用程式之 Windows 應用程式設計介面 (API) 的參考內容清單。</span><span class="sxs-lookup"><span data-stu-id="93f9d-104">The following is a list of the reference content for the Windows application programming interface (API) for desktop and server applications.</span></span>

<span data-ttu-id="93f9d-105">您可以使用 Windows API 來開發可在所有 Windows 版本上順利執行的應用程式，同時充分利用每個版本特有的特性和功能。</span><span class="sxs-lookup"><span data-stu-id="93f9d-105">Using the Windows API, you can develop applications that run successfully on all versions of Windows while taking advantage of the features and capabilities unique to each version.</span></span> <span data-ttu-id="93f9d-106"> (請注意，這先前稱為 WIN32 API。</span><span class="sxs-lookup"><span data-stu-id="93f9d-106">(Note that this was formerly called the Win32 API.</span></span> <span data-ttu-id="93f9d-107">名稱 Windows API 更準確地反映其在16位 Windows 的根目錄，以及其在64位 Windows 上的支援。 ) </span><span class="sxs-lookup"><span data-stu-id="93f9d-107">The name Windows API more accurately reflects its roots in 16-bit Windows and its support on 64-bit Windows.)</span></span>

## <a name="user-interface"></a><span data-ttu-id="93f9d-108">使用者介面</span><span class="sxs-lookup"><span data-stu-id="93f9d-108">User interface</span></span>

<span data-ttu-id="93f9d-109">Windows UI API 會建立和使用 windows 來顯示輸出、提示輸入使用者輸入，以及執行其他支援與使用者互動的工作。</span><span class="sxs-lookup"><span data-stu-id="93f9d-109">The Windows UI API create and use windows to display output, prompt for user input, and carry out the other tasks that support interaction with the user.</span></span> <span data-ttu-id="93f9d-110">大部分的應用程式會建立至少一個視窗。</span><span class="sxs-lookup"><span data-stu-id="93f9d-110">Most applications create at least one window.</span></span>

-   [<span data-ttu-id="93f9d-111">協助工具</span><span class="sxs-lookup"><span data-stu-id="93f9d-111">Accessibility</span></span>](../winauto/windows-accessibility-features-reference.md)
-   [<span data-ttu-id="93f9d-112">桌面視窗管理員 (DWM) </span><span class="sxs-lookup"><span data-stu-id="93f9d-112">Desktop Window Manager (DWM)</span></span>](../dwm/reference.md)
-   [<span data-ttu-id="93f9d-113">全球化服務</span><span class="sxs-lookup"><span data-stu-id="93f9d-113">Globalization Services</span></span>](../intl/globalization-services.md)
-   [<span data-ttu-id="93f9d-114">高 DPI</span><span class="sxs-lookup"><span data-stu-id="93f9d-114">High DPI</span></span>](../hidpi/high-dpi-reference.md)
-   [<span data-ttu-id="93f9d-115">多語系消費者介面 (MUI) </span><span class="sxs-lookup"><span data-stu-id="93f9d-115">Multilingual User Interface (MUI)</span></span>](../intl/multilingual-user-interface-reference.md)
-   [<span data-ttu-id="93f9d-116"> (NLS 的國家語言支援) </span><span class="sxs-lookup"><span data-stu-id="93f9d-116">National Language Support (NLS)</span></span>](../intl/national-language-support-reference.md)
-   <span data-ttu-id="93f9d-117">[消費者介面元素](../devnotes/user-interface.md)：</span><span class="sxs-lookup"><span data-stu-id="93f9d-117">[User Interface elements](../devnotes/user-interface.md):</span></span>

    -   [<span data-ttu-id="93f9d-118">按鈕</span><span class="sxs-lookup"><span data-stu-id="93f9d-118">Buttons</span></span>](../controls/bumper-button-button-control-reference.md)
    -   [<span data-ttu-id="93f9d-119">游標</span><span class="sxs-lookup"><span data-stu-id="93f9d-119">Carets</span></span>](../menurc/caret-functions.md)
    -   [<span data-ttu-id="93f9d-120">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="93f9d-120">Combo Boxes</span></span>](../controls/bumper-combobox-combobox-control-reference.md)
    -   [<span data-ttu-id="93f9d-121">通用對話方塊</span><span class="sxs-lookup"><span data-stu-id="93f9d-121">Common Dialog Boxes</span></span>](../dlgbox/common-dialog-box-reference.md)
    -   [<span data-ttu-id="93f9d-122">通用控制項</span><span class="sxs-lookup"><span data-stu-id="93f9d-122">Common Controls</span></span>](../controls/individual-control-info.md)
    -   [<span data-ttu-id="93f9d-123">資料指標</span><span class="sxs-lookup"><span data-stu-id="93f9d-123">Cursors</span></span>](../menurc/cursor-reference.md)
    -   [<span data-ttu-id="93f9d-124">對話方塊</span><span class="sxs-lookup"><span data-stu-id="93f9d-124">Dialog Boxes</span></span>](../dlgbox/dialog-box-reference.md)
    -   [<span data-ttu-id="93f9d-125">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="93f9d-125">Edit Controls</span></span>](../controls/bumper-edit-control-edit-control-reference.md)
    -   [<span data-ttu-id="93f9d-126">標題控制項</span><span class="sxs-lookup"><span data-stu-id="93f9d-126">Header Controls</span></span>](../controls/bumper-header-control-header-control-reference.md)
    -   [<span data-ttu-id="93f9d-127">圖示</span><span class="sxs-lookup"><span data-stu-id="93f9d-127">Icons</span></span>](../menurc/icon-reference.md)
    -   [<span data-ttu-id="93f9d-128">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="93f9d-128">Keyboard Accelerators</span></span>](../menurc/keyboard-accelerator-reference.md)
    -   [<span data-ttu-id="93f9d-129">清單方塊</span><span class="sxs-lookup"><span data-stu-id="93f9d-129">List Boxes</span></span>](../controls/bumper-list-box-list-box-control-reference.md)
    -   [<span data-ttu-id="93f9d-130">清單視圖控制項</span><span class="sxs-lookup"><span data-stu-id="93f9d-130">List-View Controls</span></span>](../controls/bumper-list-view-list-view-control-reference.md)
    -   [<span data-ttu-id="93f9d-131">功能表</span><span class="sxs-lookup"><span data-stu-id="93f9d-131">Menus</span></span>](../menurc/menu-reference.md)
    -   [<span data-ttu-id="93f9d-132">進度列</span><span class="sxs-lookup"><span data-stu-id="93f9d-132">Progress Bars</span></span>](../controls/bumper-progress-bar-progress-bar-control-reference.md)
    -   [<span data-ttu-id="93f9d-133">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="93f9d-133">Property Sheets</span></span>](../controls/bumper-property-sheet-property-sheets-reference.md)
    -   [<span data-ttu-id="93f9d-134">Rich Edit 控制項</span><span class="sxs-lookup"><span data-stu-id="93f9d-134">Rich Edit Controls</span></span>](../controls/bumper-rich-edit-rich-edit-control-reference.md)
    -   [<span data-ttu-id="93f9d-135">捲軸</span><span class="sxs-lookup"><span data-stu-id="93f9d-135">Scroll Bars</span></span>](../controls/bumper-scroll-bar-scroll-bars-reference.md)
    -   [<span data-ttu-id="93f9d-136">靜態控制項</span><span class="sxs-lookup"><span data-stu-id="93f9d-136">Static Controls</span></span>](../controls/bumper-static-control-static-control-reference.md)
    -   [<span data-ttu-id="93f9d-137">字串</span><span class="sxs-lookup"><span data-stu-id="93f9d-137">Strings</span></span>](../menurc/string-reference.md)
    -   [<span data-ttu-id="93f9d-138">工具列</span><span class="sxs-lookup"><span data-stu-id="93f9d-138">Toolbars</span></span>](../controls/bumper-toolbar-toolbar-control-reference.md)
    -   [<span data-ttu-id="93f9d-139">工具提示</span><span class="sxs-lookup"><span data-stu-id="93f9d-139">Tooltips</span></span>](../controls/bumper-tooltip-tooltip-control-reference.md)
    -   [<span data-ttu-id="93f9d-140">Trackbars</span><span class="sxs-lookup"><span data-stu-id="93f9d-140">Trackbars</span></span>](../controls/bumper-trackbar-trackbar-control-reference.md)
    -   [<span data-ttu-id="93f9d-141">樹狀檢視控制項</span><span class="sxs-lookup"><span data-stu-id="93f9d-141">Tree-View Controls</span></span>](../controls/bumper-tree-view-tree-view-control-reference.md)

-   [<span data-ttu-id="93f9d-142">Windows 動畫管理員</span><span class="sxs-lookup"><span data-stu-id="93f9d-142">Windows Animation Manager</span></span>](../uianimation/windows-animation-reference.md)
-   [<span data-ttu-id="93f9d-143">Windows 功能區架構</span><span class="sxs-lookup"><span data-stu-id="93f9d-143">Windows Ribbon Framework</span></span>](../windowsribbon/windowsribbon-reference-entry.md)

## <a name="windows-environment-shell"></a><span data-ttu-id="93f9d-144">Windows 環境 (Shell) </span><span class="sxs-lookup"><span data-stu-id="93f9d-144">Windows environment (Shell)</span></span>

-   [<span data-ttu-id="93f9d-145">Windows 屬性系統</span><span class="sxs-lookup"><span data-stu-id="93f9d-145">Windows Property System</span></span>](../properties/property-system-reference.md)
-   <span data-ttu-id="93f9d-146">[Windows Shell](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-146">[Windows Shell](/previous-versions/windows/desktop/legacy/ff521731(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-147">Windows 搜尋</span><span class="sxs-lookup"><span data-stu-id="93f9d-147">Windows Search</span></span>](../search/-search-reference-entry-page.md)
-   [<span data-ttu-id="93f9d-148">主控台</span><span class="sxs-lookup"><span data-stu-id="93f9d-148">Consoles</span></span>](/windows/console/console-reference)

## <a name="user-input-and-messaging"></a><span data-ttu-id="93f9d-149">使用者輸入和訊息</span><span class="sxs-lookup"><span data-stu-id="93f9d-149">User input and messaging</span></span>

-   [<span data-ttu-id="93f9d-150">使用者互動</span><span class="sxs-lookup"><span data-stu-id="93f9d-150">User Interaction</span></span>](../user-interaction.md)
    -   [<span data-ttu-id="93f9d-151">直接操作</span><span class="sxs-lookup"><span data-stu-id="93f9d-151">Direct Manipulation</span></span>](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)
    -   [<span data-ttu-id="93f9d-152">筆跡輸入</span><span class="sxs-lookup"><span data-stu-id="93f9d-152">Ink input</span></span>](/previous-versions/windows/desktop/input_ink/input-ink-portal)
    -   [<span data-ttu-id="93f9d-153">輸入意見設定</span><span class="sxs-lookup"><span data-stu-id="93f9d-153">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
    -   [<span data-ttu-id="93f9d-154">互動內容</span><span class="sxs-lookup"><span data-stu-id="93f9d-154">Interaction Context</span></span>](/previous-versions/windows/desktop/input_intcontext/interaction-context-portal)
    -   [<span data-ttu-id="93f9d-155">指標裝置輸入堆疊</span><span class="sxs-lookup"><span data-stu-id="93f9d-155">Pointer Device Input Stack</span></span>](/previous-versions/windows/desktop/input_pointerdevice/pointer-device-stack-portal)
    -   [<span data-ttu-id="93f9d-156">指標輸入訊息和通知</span><span class="sxs-lookup"><span data-stu-id="93f9d-156">Pointer Input Messages and Notifications</span></span>](/previous-versions/windows/desktop/inputmsg/messages-and-notifications)
    -   [<span data-ttu-id="93f9d-157">星形控制器輸入</span><span class="sxs-lookup"><span data-stu-id="93f9d-157">Radial controller input</span></span>](/previous-versions/windows/desktop/input_radial/radialcontroller-portal)
    -   [<span data-ttu-id="93f9d-158">Text Services Framework (TSF)</span><span class="sxs-lookup"><span data-stu-id="93f9d-158">Text Services Framework</span></span>](../tsf/text-services-framework.md)
    -   [<span data-ttu-id="93f9d-159">觸控點擊測試</span><span class="sxs-lookup"><span data-stu-id="93f9d-159">Touch Hit Testing</span></span>](/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal)
    -   [<span data-ttu-id="93f9d-160">觸控插入</span><span class="sxs-lookup"><span data-stu-id="93f9d-160">Touch Injection</span></span>](/previous-versions/windows/desktop/input_touchinjection/touch-injection-portal)
-   [<span data-ttu-id="93f9d-161">舊版使用者互動</span><span class="sxs-lookup"><span data-stu-id="93f9d-161">Legacy User Interaction</span></span>](../legacy-user-interaction-features.md)
    -   [<span data-ttu-id="93f9d-162">觸控輸入</span><span class="sxs-lookup"><span data-stu-id="93f9d-162">Touch Input</span></span>](../wintouch/windows-touch-portal.md)
    -   [<span data-ttu-id="93f9d-163">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="93f9d-163">Keyboard Input</span></span>](../inputdev/keyboard-input.md)
    -   [<span data-ttu-id="93f9d-164">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="93f9d-164">Mouse Input</span></span>](../inputdev/mouse-input.md)
    -   [<span data-ttu-id="93f9d-165">原始輸入</span><span class="sxs-lookup"><span data-stu-id="93f9d-165">Raw Input</span></span>](../inputdev/raw-input.md)
-   <span data-ttu-id="93f9d-166">[Windows 和訊息](../winmsg/windowing.md)：</span><span class="sxs-lookup"><span data-stu-id="93f9d-166">[Windows and Messages](../winmsg/windowing.md):</span></span>

    -   [<span data-ttu-id="93f9d-167">訊息和訊息佇列</span><span class="sxs-lookup"><span data-stu-id="93f9d-167">Messages and Message Queues</span></span>](../winmsg/message-and-message-queue-reference.md)
    -   [<span data-ttu-id="93f9d-168">Windows</span><span class="sxs-lookup"><span data-stu-id="93f9d-168">Windows</span></span>](../winmsg/window-reference.md)
    -   [<span data-ttu-id="93f9d-169">視窗類別</span><span class="sxs-lookup"><span data-stu-id="93f9d-169">Window Classes</span></span>](../winmsg/window-class-reference.md)
    -   [<span data-ttu-id="93f9d-170">視窗程式</span><span class="sxs-lookup"><span data-stu-id="93f9d-170">Window Procedures</span></span>](../winmsg/window-procedure-reference.md)
    -   [<span data-ttu-id="93f9d-171">計時器</span><span class="sxs-lookup"><span data-stu-id="93f9d-171">Timers</span></span>](../winmsg/timer-reference.md)
    -   [<span data-ttu-id="93f9d-172">視窗屬性</span><span class="sxs-lookup"><span data-stu-id="93f9d-172">Window Properties</span></span>](../winmsg/window-property-reference.md)
    -   [<span data-ttu-id="93f9d-173">鉤</span><span class="sxs-lookup"><span data-stu-id="93f9d-173">Hooks</span></span>](../winmsg/hook-reference.md)

## <a name="data-access-and-storage"></a><span data-ttu-id="93f9d-174">資料存取與存放</span><span class="sxs-lookup"><span data-stu-id="93f9d-174">Data access and storage</span></span>

-   [<span data-ttu-id="93f9d-175">背景智慧型傳送服務 (BITS)</span><span class="sxs-lookup"><span data-stu-id="93f9d-175">Background Intelligent Transfer Service (BITS)</span></span>](../bits/bits-reference.md)
-   [<span data-ttu-id="93f9d-176">資料備份</span><span class="sxs-lookup"><span data-stu-id="93f9d-176">Data Backup</span></span>](../backup/backup.md)
    -   [<span data-ttu-id="93f9d-177">Backup</span><span class="sxs-lookup"><span data-stu-id="93f9d-177">Backup</span></span>](../backup/backup-reference.md)
    -   [<span data-ttu-id="93f9d-178">重複資料刪除</span><span class="sxs-lookup"><span data-stu-id="93f9d-178">Data Deduplication</span></span>](/previous-versions/windows/desktop/dedup/data-deduplication-api-reference)
    -   [<span data-ttu-id="93f9d-179">磁碟區陰影複製</span><span class="sxs-lookup"><span data-stu-id="93f9d-179">Volume Shadow Copy</span></span>](../vss/volume-shadow-copy-reference.md)
    -   [<span data-ttu-id="93f9d-180">Windows Server Backup</span><span class="sxs-lookup"><span data-stu-id="93f9d-180">Windows Server Backup</span></span>](/previous-versions/windows/desktop/wsb/windows-server-backup-api-interfaces)
-   <span data-ttu-id="93f9d-181">[資料交換](../dataxchg/data-exchange.md)：</span><span class="sxs-lookup"><span data-stu-id="93f9d-181">[Data Exchange](../dataxchg/data-exchange.md):</span></span>

    -   [<span data-ttu-id="93f9d-182">剪貼簿</span><span class="sxs-lookup"><span data-stu-id="93f9d-182">Clipboard</span></span>](../dataxchg/clipboard-reference.md)
    -   [<span data-ttu-id="93f9d-183">動態資料交換 (DDE) </span><span class="sxs-lookup"><span data-stu-id="93f9d-183">Dynamic Data Exchange (DDE)</span></span>](../dataxchg/dynamic-data-exchange-reference.md)
    -   [<span data-ttu-id="93f9d-184">動態資料交換管理 (DDEML) </span><span class="sxs-lookup"><span data-stu-id="93f9d-184">Dynamic Data Exchange Management (DDEML)</span></span>](../dataxchg/dynamic-data-exchange-management-library-reference.md)

-   [<span data-ttu-id="93f9d-185">目錄管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-185">Directory Management</span></span>](../fileio/directory-management-reference.md)
-   [<span data-ttu-id="93f9d-186">磁碟管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-186">Disk Management</span></span>](../fileio/disk-management-reference.md)
-   [<span data-ttu-id="93f9d-187">分散式檔案系統 (DFS)</span><span class="sxs-lookup"><span data-stu-id="93f9d-187">Distributed File System (DFS)</span></span>](/previous-versions/windows/desktop/dfs/distributed-file-system-reference)
-   [<span data-ttu-id="93f9d-188">分散式檔案系統複寫</span><span class="sxs-lookup"><span data-stu-id="93f9d-188">Distributed File System Replication</span></span>](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes)
-   [<span data-ttu-id="93f9d-189">可擴充儲存引擎</span><span class="sxs-lookup"><span data-stu-id="93f9d-189">Extensible Storage Engine</span></span>](../extensible-storage-engine/extensible-storage-engine-reference.md)
-   [<span data-ttu-id="93f9d-190">檔案和 i/o (本機檔案系統) </span><span class="sxs-lookup"><span data-stu-id="93f9d-190">Files and I/O (Local file system)</span></span>](../fileio/file-management-reference.md)
-   [<span data-ttu-id="93f9d-191">iSCSI 探索程式庫 API</span><span class="sxs-lookup"><span data-stu-id="93f9d-191">iSCSI Discovery Library API</span></span>](/previous-versions/windows/desktop/iscsidisc/iscsi-discovery-library-reference)
-   [<span data-ttu-id="93f9d-192">離線檔案</span><span class="sxs-lookup"><span data-stu-id="93f9d-192">Offline Files</span></span>](/previous-versions/windows/desktop/offlinefiles/offline-files-reference)
-   [<span data-ttu-id="93f9d-193">包裝</span><span class="sxs-lookup"><span data-stu-id="93f9d-193">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging-programming-reference)
-   [<span data-ttu-id="93f9d-194">遠端差異壓縮</span><span class="sxs-lookup"><span data-stu-id="93f9d-194">Remote Differential Compression</span></span>](/previous-versions/windows/desktop/rdc/remote-differential-compression-reference)
-   [<span data-ttu-id="93f9d-195">交易式 NTFS</span><span class="sxs-lookup"><span data-stu-id="93f9d-195">Transactional NTFS</span></span>](../fileio/transactional-ntfs-reference.md)
-   [<span data-ttu-id="93f9d-196">磁碟區管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-196">Volume Management</span></span>](../fileio/volume-management-reference.md)
-   <span data-ttu-id="93f9d-197">[虛擬硬碟 (VHD) ](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-197">[Virtual Hard Disk (VHD)](/previous-versions/windows/desktop/legacy/dd323700(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-198">Windows 存放裝置管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-198">Windows Storage Management</span></span>](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
-   <span data-ttu-id="93f9d-199">[Windows Data Access Component](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-199">[Windows Data Access Components](/previous-versions/windows/desktop/legacy/aa968814(v=vs.85))</span></span>
    -   [<span data-ttu-id="93f9d-200">Microsoft 開放式資料庫連接 (ODBC)</span><span class="sxs-lookup"><span data-stu-id="93f9d-200">Microsoft Open Database Connectivity (ODBC)</span></span>](/sql/odbc/reference/syntax/odbc-reference)
    -   <span data-ttu-id="93f9d-201">[Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-201">[Microsoft OLE DB](/previous-versions/windows/desktop/ms718050(v=vs.85))</span></span>
    -   [<span data-ttu-id="93f9d-202">Microsoft ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="93f9d-202">Microsoft ActiveX Data Objects (ADO)</span></span>](/sql/ado/reference/ado-programmer-s-reference)

## <a name="diagnostics"></a><span data-ttu-id="93f9d-203">診斷</span><span class="sxs-lookup"><span data-stu-id="93f9d-203">Diagnostics</span></span>

<span data-ttu-id="93f9d-204">[診斷](/previous-versions//bb648685(v=vs.85))API 可讓您針對應用程式或系統問題進行疑難排解，並監視效能。</span><span class="sxs-lookup"><span data-stu-id="93f9d-204">The [Diagnostics](/previous-versions//bb648685(v=vs.85)) API enable you to troubleshoot application or system problems and monitor performance.</span></span>

-   [<span data-ttu-id="93f9d-205">應用程式復原和重新啟動</span><span class="sxs-lookup"><span data-stu-id="93f9d-205">Application Recovery and Restart</span></span>](../recovery/application-recovery-and-restart-reference.md)
-   [<span data-ttu-id="93f9d-206">偵錯</span><span class="sxs-lookup"><span data-stu-id="93f9d-206">Debugging</span></span>](../debug/debugging-reference.md)
-   [<span data-ttu-id="93f9d-207">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="93f9d-207">Error Handling</span></span>](../debug/error-handling-reference.md)
-   [<span data-ttu-id="93f9d-208">事件記錄</span><span class="sxs-lookup"><span data-stu-id="93f9d-208">Event Logging</span></span>](../eventlog/event-logging-reference.md)
-   [<span data-ttu-id="93f9d-209">事件追蹤</span><span class="sxs-lookup"><span data-stu-id="93f9d-209">Event Tracing</span></span>](../etw/event-tracing-reference.md)
-   [<span data-ttu-id="93f9d-210"> (HCP) 的硬體計數器分析 </span><span class="sxs-lookup"><span data-stu-id="93f9d-210">Hardware Counter Profiling (HCP)</span></span>](/previous-versions/windows/desktop/hcp/hcp-reference)
-   [<span data-ttu-id="93f9d-211">網路診斷架構 (NDF) </span><span class="sxs-lookup"><span data-stu-id="93f9d-211">Network Diagnostics Framework (NDF)</span></span>](../ndf/ndf-reference.md)
-   [<span data-ttu-id="93f9d-212">網路監視器</span><span class="sxs-lookup"><span data-stu-id="93f9d-212">Network Monitor</span></span>](../netmon2/reference.md)
-   [<span data-ttu-id="93f9d-213">效能計數器</span><span class="sxs-lookup"><span data-stu-id="93f9d-213">Performance Counters</span></span>](../perfctrs/performance-counters-reference.md)
-   [<span data-ttu-id="93f9d-214">效能記錄檔及警示 (PLA) </span><span class="sxs-lookup"><span data-stu-id="93f9d-214">Performance Logs and Alerts (PLA)</span></span>](/previous-versions/windows/desktop/pla/performance-logs-and-alerts-reference)
-   [<span data-ttu-id="93f9d-215">進程快照</span><span class="sxs-lookup"><span data-stu-id="93f9d-215">Process Snapshotting</span></span>](/previous-versions/windows/desktop/proc_snap/process-snapshotting-reference)
-   [<span data-ttu-id="93f9d-216">進程狀態 (PSAPI.DLL) </span><span class="sxs-lookup"><span data-stu-id="93f9d-216">Process Status (PSAPI)</span></span>](../psapi/psapi-reference.md)
-   [<span data-ttu-id="93f9d-217">結構化例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="93f9d-217">Structured Exception Handling</span></span>](../debug/structured-exception-handling-reference.md)
-   [<span data-ttu-id="93f9d-218">系統監視器</span><span class="sxs-lookup"><span data-stu-id="93f9d-218">System Monitor</span></span>](../sysmon/system-monitor-reference.md)
-   [<span data-ttu-id="93f9d-219">等候鏈遍歷</span><span class="sxs-lookup"><span data-stu-id="93f9d-219">Wait Chain Traversal</span></span>](../debug/wait-chain-traversal.md)
-   [<span data-ttu-id="93f9d-220">Windows 錯誤報告 (WER)</span><span class="sxs-lookup"><span data-stu-id="93f9d-220">Windows Error Reporting (WER)</span></span>](../wer/wer-reference.md)
-   [<span data-ttu-id="93f9d-221">Windows 事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="93f9d-221">Windows Event Log</span></span>](../wes/windows-event-log-reference.md)
-   [<span data-ttu-id="93f9d-222">Windows 疑難排解平臺</span><span class="sxs-lookup"><span data-stu-id="93f9d-222">Windows Troubleshooting Platform</span></span>](/previous-versions/windows/desktop/wintt/windows-troubleshooting-reference)

## <a name="graphics-and-multimedia"></a><span data-ttu-id="93f9d-223">圖形與多媒體</span><span class="sxs-lookup"><span data-stu-id="93f9d-223">Graphics and multimedia</span></span>

<span data-ttu-id="93f9d-224">[圖形、多媒體、](/previous-versions//aa969176(v=vs.85)) [音訊和影片](../audio-and-video.md)api 可讓應用程式併入格式化的文字、圖形、音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="93f9d-224">The [Graphics, multimedia,](/previous-versions//aa969176(v=vs.85)) [audio, and video](../audio-and-video.md) APIs enable applications to incorporate formatted text, graphics, audio, and video.</span></span>

-   [<span data-ttu-id="93f9d-225">核心音訊</span><span class="sxs-lookup"><span data-stu-id="93f9d-225">Core Audio</span></span>](../coreaudio/programming-reference.md)
-   [<span data-ttu-id="93f9d-226">Direct2D</span><span class="sxs-lookup"><span data-stu-id="93f9d-226">Direct2D</span></span>](../direct2d/reference.md)
-   [<span data-ttu-id="93f9d-227">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="93f9d-227">DirectComposition</span></span>](../directcomp/reference.md)
-   [<span data-ttu-id="93f9d-228">DirectShow</span><span class="sxs-lookup"><span data-stu-id="93f9d-228">DirectShow</span></span>](../directshow/directshow-reference.md)
-   [<span data-ttu-id="93f9d-229">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="93f9d-229">DirectWrite</span></span>](../directwrite/reference.md)
-   [<span data-ttu-id="93f9d-230">DirectX</span><span class="sxs-lookup"><span data-stu-id="93f9d-230">DirectX</span></span>](../directx-sdk--august-2009-.md)
-   [<span data-ttu-id="93f9d-231">圖形裝置介面 (GDI) </span><span class="sxs-lookup"><span data-stu-id="93f9d-231">Graphics Device Interface (GDI)</span></span>](../gdi/windows-gdi.md)
-   [<span data-ttu-id="93f9d-232">GDI+</span><span class="sxs-lookup"><span data-stu-id="93f9d-232">GDI+</span></span>](../gdiplus/-gdiplus-class-gdi-reference.md)
-   [<span data-ttu-id="93f9d-233">媒體串流</span><span class="sxs-lookup"><span data-stu-id="93f9d-233">Media Streaming</span></span>](../mediastreaming/media-streaming-api-portal.md)
-   [<span data-ttu-id="93f9d-234">Microsoft 媒體基礎</span><span class="sxs-lookup"><span data-stu-id="93f9d-234">Microsoft Media Foundation</span></span>](../medfound/media-foundation-programming-reference.md)
-   [<span data-ttu-id="93f9d-235">Microsoft 電視技術</span><span class="sxs-lookup"><span data-stu-id="93f9d-235">Microsoft TV Technologies</span></span>](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-application-interface)
-   [<span data-ttu-id="93f9d-236">Opengl</span><span class="sxs-lookup"><span data-stu-id="93f9d-236">OpenGL</span></span>](../opengl/opengl-reference.md)
-   [<span data-ttu-id="93f9d-237">監視設定</span><span class="sxs-lookup"><span data-stu-id="93f9d-237">Monitor Configuration</span></span>](../monitor/monitor-configuration-reference.md)
-   [<span data-ttu-id="93f9d-238">多顯示器監視</span><span class="sxs-lookup"><span data-stu-id="93f9d-238">Multiple Display Monitors</span></span>](../gdi/multiple-display-monitors-reference.md)
-   [<span data-ttu-id="93f9d-239">取得圖片</span><span class="sxs-lookup"><span data-stu-id="93f9d-239">Picture Acquisition</span></span>](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [<span data-ttu-id="93f9d-240">Windows 色彩系統</span><span class="sxs-lookup"><span data-stu-id="93f9d-240">Windows Color System</span></span>](../wcs/reference.md)
-   [<span data-ttu-id="93f9d-241">Windows 影像處理元件 (WIC)</span><span class="sxs-lookup"><span data-stu-id="93f9d-241">Windows Imaging Component (WIC)</span></span>](../wic/-wic-codec-reference.md)
-   <span data-ttu-id="93f9d-242">[Windows Media 音訊和影片編解碼器和 DSP](/previous-versions//dd443208(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-242">[Windows Media Audio and Video Codec and DSP](/previous-versions//dd443208(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-243">Windows Media Center</span><span class="sxs-lookup"><span data-stu-id="93f9d-243">Windows Media Center</span></span>](/previous-versions/windows/desktop/acquisition/programming-reference)
-   [<span data-ttu-id="93f9d-244">Windows Media 格式</span><span class="sxs-lookup"><span data-stu-id="93f9d-244">Windows Media Format</span></span>](../wmformat/programming-reference.md)
-   [<span data-ttu-id="93f9d-245">Windows Media Library 共用服務</span><span class="sxs-lookup"><span data-stu-id="93f9d-245">Windows Media Library Sharing Services</span></span>](/previous-versions/windows/desktop/wmlss/windowsmedialibrarysharingservicesportal)
-   [<span data-ttu-id="93f9d-246">Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="93f9d-246">Windows Media Player</span></span>](../wmp/windows-media-player-object-model-reference.md)
-   <span data-ttu-id="93f9d-247">[Windows Media Services](/previous-versions/windows/desktop/dd893580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-247">[Windows Media Services](/previous-versions/windows/desktop/dd893580(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-248">Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="93f9d-248">Windows Movie Maker</span></span>](/previous-versions/windows/desktop/wmmdvdm/windows-movie-maker-apis)
-   [<span data-ttu-id="93f9d-249">Windows 多媒體</span><span class="sxs-lookup"><span data-stu-id="93f9d-249">Windows Multimedia</span></span>](../multimedia/multimedia-reference.md)

## <a name="devices"></a><span data-ttu-id="93f9d-250">裝置</span><span class="sxs-lookup"><span data-stu-id="93f9d-250">Devices</span></span>

-   [<span data-ttu-id="93f9d-251">AllJoyn</span><span class="sxs-lookup"><span data-stu-id="93f9d-251">AllJoyn</span></span>](/previous-versions/windows/desktop/alljoyn/alljoyn-api-portal)
-   [<span data-ttu-id="93f9d-252">通訊資源</span><span class="sxs-lookup"><span data-stu-id="93f9d-252">Communications Resources</span></span>](../devio/communications-reference.md)
-   [<span data-ttu-id="93f9d-253">裝置存取</span><span class="sxs-lookup"><span data-stu-id="93f9d-253">Device Access</span></span>](/previous-versions/windows/desktop/deviceaccess/device-access-api-c---programming-reference)
-   [<span data-ttu-id="93f9d-254">裝置管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-254">Device Management</span></span>](../devio/device-management-reference.md)
-   [<span data-ttu-id="93f9d-255">增強的存放區</span><span class="sxs-lookup"><span data-stu-id="93f9d-255">Enhanced Storage</span></span>](/previous-versions/windows/desktop/enstor/enhanced-storage-reference)
-   [<span data-ttu-id="93f9d-256">函數探索</span><span class="sxs-lookup"><span data-stu-id="93f9d-256">Function Discovery</span></span>](/previous-versions/windows/desktop/fundisc/function-discovery-reference)
-   [<span data-ttu-id="93f9d-257">映射主控</span><span class="sxs-lookup"><span data-stu-id="93f9d-257">Image Mastering</span></span>](../imapi/imapi-reference.md)
-   [<span data-ttu-id="93f9d-258">位置</span><span class="sxs-lookup"><span data-stu-id="93f9d-258">Location</span></span>](../locationapi/windows-location-programming-reference.md)
-   [<span data-ttu-id="93f9d-259">PnP X 關聯資料庫</span><span class="sxs-lookup"><span data-stu-id="93f9d-259">PnP-X Association Database</span></span>](/previous-versions/windows/desktop/fundisc/pnp-x-association-database-reference)
-   [<span data-ttu-id="93f9d-260">列印</span><span class="sxs-lookup"><span data-stu-id="93f9d-260">Printing</span></span>](/windows-hardware/drivers/print/introduction-to-printing)
    -   [<span data-ttu-id="93f9d-261">列印多工緩衝處理器</span><span class="sxs-lookup"><span data-stu-id="93f9d-261">Print Spooler</span></span>](../printdocs/printing-and-print-spooler-reference.md)
    -   [<span data-ttu-id="93f9d-262">列印檔案套件</span><span class="sxs-lookup"><span data-stu-id="93f9d-262">Print Document Package</span></span>](../printdocs/tailored-app-printing-api.md)
    -   [<span data-ttu-id="93f9d-263">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="93f9d-263">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
    -   [<span data-ttu-id="93f9d-264">列印票證</span><span class="sxs-lookup"><span data-stu-id="93f9d-264">Print Ticket</span></span>](../printdocs/print-ticket-api.md)
    -   [<span data-ttu-id="93f9d-265">XPS 列印</span><span class="sxs-lookup"><span data-stu-id="93f9d-265">XPS Print</span></span>](../printdocs/xpsprint-api.md)
-   [<span data-ttu-id="93f9d-266">感應器</span><span class="sxs-lookup"><span data-stu-id="93f9d-266">Sensors</span></span>](../sensorsapi/sensor-api-programming-reference.md)
-   [<span data-ttu-id="93f9d-267">系統事件通知服務 (SENS) </span><span class="sxs-lookup"><span data-stu-id="93f9d-267">System Event Notification Service (SENS)</span></span>](../sens/sens-reference.md)
-   [<span data-ttu-id="93f9d-268">工具說明</span><span class="sxs-lookup"><span data-stu-id="93f9d-268">Tool Help</span></span>](../toolhelp/tool-help-reference.md)
-   [<span data-ttu-id="93f9d-269">UPnP</span><span class="sxs-lookup"><span data-stu-id="93f9d-269">UPnP</span></span>](../upnp/universal-plug-and-play-start-page.md)
-   [<span data-ttu-id="93f9d-270">裝置上的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="93f9d-270">Web Services on Devices</span></span>](../wsdapi/web-services-for-devices-reference.md)
-   [<span data-ttu-id="93f9d-271">Windows Image Acquisition (WIA)</span><span class="sxs-lookup"><span data-stu-id="93f9d-271">Windows Image Acquisition (WIA)</span></span>](../wia/-wia-reference.md)
-   [<span data-ttu-id="93f9d-272">Windows Media 裝置管理員</span><span class="sxs-lookup"><span data-stu-id="93f9d-272">Windows Media Device Manager</span></span>](../wmdm/programming-reference.md)
-   [<span data-ttu-id="93f9d-273">Windows 可攜式裝置</span><span class="sxs-lookup"><span data-stu-id="93f9d-273">Windows Portable Devices</span></span>](../wpd_sdk/programming-reference.md)

## <a name="system-services"></a><span data-ttu-id="93f9d-274">系統服務</span><span class="sxs-lookup"><span data-stu-id="93f9d-274">System services</span></span>

<span data-ttu-id="93f9d-275">[系統服務](/previous-versions//aa969179(v=vs.85))api 可讓應用程式存取電腦的資源和基礎作業系統的功能，例如記憶體、檔案系統、裝置、進程和執行緒。</span><span class="sxs-lookup"><span data-stu-id="93f9d-275">The [System Services](/previous-versions//aa969179(v=vs.85)) APIs give applications access to the resources of the computer and the features of the underlying operating system, such as memory, file systems, devices, processes, and threads.</span></span>

-   [<span data-ttu-id="93f9d-276">COM</span><span class="sxs-lookup"><span data-stu-id="93f9d-276">COM</span></span>](../com/reference.md)
-   [<span data-ttu-id="93f9d-277">Com+</span><span class="sxs-lookup"><span data-stu-id="93f9d-277">COM+</span></span>](../cossdk/com--reference.md)
-   [<span data-ttu-id="93f9d-278">壓縮 API</span><span class="sxs-lookup"><span data-stu-id="93f9d-278">Compression API</span></span>](../cmpapi/-compression-portal.md)
-   <span data-ttu-id="93f9d-279">[分散式交易協調器 (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-279">[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms686108(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-280">動態連結程式庫 (Dll) </span><span class="sxs-lookup"><span data-stu-id="93f9d-280">Dynamic-Link Libraries (DLLs)</span></span>](../dlls/dynamic-link-library-functions.md)
-   [<span data-ttu-id="93f9d-281">說明 API</span><span class="sxs-lookup"><span data-stu-id="93f9d-281">Help API</span></span>](/previous-versions/windows/desktop/helpapi/help-api-reference)
-   <span data-ttu-id="93f9d-282">[處理序間通訊](../ipc/interprocess-communications.md)：</span><span class="sxs-lookup"><span data-stu-id="93f9d-282">[Interprocess Communications](../ipc/interprocess-communications.md):</span></span>
    -   [<span data-ttu-id="93f9d-283">Mailslots</span><span class="sxs-lookup"><span data-stu-id="93f9d-283">Mailslots</span></span>](../ipc/mailslot-functions.md)
    -   [<span data-ttu-id="93f9d-284">管道</span><span class="sxs-lookup"><span data-stu-id="93f9d-284">Pipes</span></span>](../ipc/pipe-functions.md)
-   [<span data-ttu-id="93f9d-285">核心交易管理員 (KTM) </span><span class="sxs-lookup"><span data-stu-id="93f9d-285">Kernel Transaction Manager (KTM)</span></span>](../ktm/ktm-reference.md)
-   [<span data-ttu-id="93f9d-286">記憶體管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-286">Memory Management</span></span>](../memory/memory-management-reference.md)
-   [<span data-ttu-id="93f9d-287">作業錄製器</span><span class="sxs-lookup"><span data-stu-id="93f9d-287">Operation Recorder</span></span>](/previous-versions/windows/desktop/oprec/-operation-portal)
-   [<span data-ttu-id="93f9d-288">電源管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-288">Power Management</span></span>](../power/power-management-reference.md)
-   [<span data-ttu-id="93f9d-289">遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="93f9d-289">Remote Desktop Services</span></span>](../termserv/terminal-services-reference.md)
-   [<span data-ttu-id="93f9d-290">處理序</span><span class="sxs-lookup"><span data-stu-id="93f9d-290">Processes</span></span>](../procthread/process-and-thread-reference.md)
-   [<span data-ttu-id="93f9d-291">服務</span><span class="sxs-lookup"><span data-stu-id="93f9d-291">Services</span></span>](../services/service-reference.md)
-   [<span data-ttu-id="93f9d-292">同步處理</span><span class="sxs-lookup"><span data-stu-id="93f9d-292">Synchronization</span></span>](../sync/synchronization-reference.md)
-   [<span data-ttu-id="93f9d-293">執行緒</span><span class="sxs-lookup"><span data-stu-id="93f9d-293">Threads</span></span>](../procthread/process-and-thread-reference.md)
-   [<span data-ttu-id="93f9d-294">Windows 桌面共用</span><span class="sxs-lookup"><span data-stu-id="93f9d-294">Windows Desktop Sharing</span></span>](/previous-versions/windows/desktop/rdp/windows-desktop-sharing-reference)
-   [<span data-ttu-id="93f9d-295">Windows 系統資訊</span><span class="sxs-lookup"><span data-stu-id="93f9d-295">Windows System Information</span></span>](../sysinfo/windows-system-information.md)
    -   [<span data-ttu-id="93f9d-296">控制碼和物件</span><span class="sxs-lookup"><span data-stu-id="93f9d-296">Handle and Objects</span></span>](../sysinfo/handle-and-object-functions.md)
    -   [<span data-ttu-id="93f9d-297">登錄</span><span class="sxs-lookup"><span data-stu-id="93f9d-297">Registry</span></span>](../sysinfo/registry-reference.md)
    -   [<span data-ttu-id="93f9d-298">Time</span><span class="sxs-lookup"><span data-stu-id="93f9d-298">Time</span></span>](../sysinfo/time-reference.md)
    -   [<span data-ttu-id="93f9d-299">時間提供者</span><span class="sxs-lookup"><span data-stu-id="93f9d-299">Time Provider</span></span>](../sysinfo/time-provider-reference.md)

## <a name="security-and-identity"></a><span data-ttu-id="93f9d-300">安全性與身分識別</span><span class="sxs-lookup"><span data-stu-id="93f9d-300">Security and identity</span></span>

<span data-ttu-id="93f9d-301">[安全性和身分識別](../devnotes/security.md)api 會在登入時啟用密碼驗證，為所有可共用的系統物件、特殊許可權的存取控制、版權管理和安全性審核提供任意的保護。</span><span class="sxs-lookup"><span data-stu-id="93f9d-301">The [Security and Identity](../devnotes/security.md) APIs enable password authentication at logon, discretionary protection for all sharable system objects, privileged access control, rights management, and security auditing.</span></span>

-   [<span data-ttu-id="93f9d-302">驗證</span><span class="sxs-lookup"><span data-stu-id="93f9d-302">Authentication</span></span>](../secauthn/authentication-reference.md)
-   [<span data-ttu-id="93f9d-303">授權</span><span class="sxs-lookup"><span data-stu-id="93f9d-303">Authorization</span></span>](../secauthz/authorization-reference.md)
-   [<span data-ttu-id="93f9d-304">憑證註冊</span><span class="sxs-lookup"><span data-stu-id="93f9d-304">Certificate Enrollment</span></span>](../seccertenroll/certificate-enrollment-api-reference.md)
-   [<span data-ttu-id="93f9d-305">碼編譯</span><span class="sxs-lookup"><span data-stu-id="93f9d-305">Cryptography</span></span>](../seccrypto/cryptography-reference.md)
-   [<span data-ttu-id="93f9d-306">新一代密碼編譯 (CNG) </span><span class="sxs-lookup"><span data-stu-id="93f9d-306">Cryptographic Next Generation (CNG)</span></span>](../seccng/cng-reference.md)
-   <span data-ttu-id="93f9d-307">[目錄服務](/previous-versions//ms682458(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-307">[Directory Services](/previous-versions//ms682458(v=vs.85))</span></span>
    -   [<span data-ttu-id="93f9d-308">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="93f9d-308">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services-reference.md)
    -   [<span data-ttu-id="93f9d-309">Active Directory 服務介面 (ADSI) </span><span class="sxs-lookup"><span data-stu-id="93f9d-309">Active Directory Service Interfaces (ADSI)</span></span>](../adsi/adsi-reference.md)
-   [<span data-ttu-id="93f9d-310">可延伸的驗證通訊協定 (EAP)</span><span class="sxs-lookup"><span data-stu-id="93f9d-310">Extensible Authentication Protocol (EAP)</span></span>](../eap/extensible-authentication-protocol-reference.md)
-   [<span data-ttu-id="93f9d-311">可延伸的驗證通訊協定主機 (EAPHost) </span><span class="sxs-lookup"><span data-stu-id="93f9d-311">Extensible Authentication Protocol Host (EAPHost)</span></span>](../eaphost/about-eap-host.md)
-   [<span data-ttu-id="93f9d-312">MS-CHAP 密碼管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-312">MS-CHAP Password Management</span></span>](/previous-versions/windows/desktop/mschap/ms-chap-password-management-reference)
-   [<span data-ttu-id="93f9d-313">網路存取保護 (NAP)</span><span class="sxs-lookup"><span data-stu-id="93f9d-313">Network Access Protection (NAP)</span></span>](../nap/nap-reference.md)
-   [<span data-ttu-id="93f9d-314">NPS) 的網路原則伺服器擴充功能 (</span><span class="sxs-lookup"><span data-stu-id="93f9d-314">Network Policy Server Extensions (NPS)</span></span>](../nps/ias-internet-authentication-service-reference.md)
-   [<span data-ttu-id="93f9d-315">家長監護</span><span class="sxs-lookup"><span data-stu-id="93f9d-315">Parental Controls</span></span>](../parcon/parental-controls-reference.md)
-   [<span data-ttu-id="93f9d-316">安全性 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="93f9d-316">Security WMI Providers</span></span>](../secprov/security-wmi-providers-reference.md)
-   [<span data-ttu-id="93f9d-317">TPM 基本服務 (TBS)</span><span class="sxs-lookup"><span data-stu-id="93f9d-317">TPM Base Services (TBS)</span></span>](../tbs/tbs-reference.md)
-   [<span data-ttu-id="93f9d-318">Windows 生物特徵辨識架構</span><span class="sxs-lookup"><span data-stu-id="93f9d-318">Windows Biometric Framework</span></span>](../secbiomet/biometric-service-api-reference.md)

## <a name="application-installation-and-servicing"></a><span data-ttu-id="93f9d-319">應用程式安裝和維護</span><span class="sxs-lookup"><span data-stu-id="93f9d-319">Application installation and servicing</span></span>

-   <span data-ttu-id="93f9d-320">[遊戲總管](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-320">[Games Explorer](/previous-versions/windows/desktop/legacy/ee415251(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-321">並存元件</span><span class="sxs-lookup"><span data-stu-id="93f9d-321">Side-by-side Assemblies</span></span>](../sbscs/side-by-side-assemblies-reference.md)
-   [<span data-ttu-id="93f9d-322">封裝、部署和查詢 Api</span><span class="sxs-lookup"><span data-stu-id="93f9d-322">Packaging, deployment, and query APIs</span></span>](../appxpkg/api-reference.md
)
-   [<span data-ttu-id="93f9d-323">開發人員授權</span><span class="sxs-lookup"><span data-stu-id="93f9d-323">Developer License</span></span>](../devlic/developer-license-apis.md)
-   [<span data-ttu-id="93f9d-324">重新開機管理員</span><span class="sxs-lookup"><span data-stu-id="93f9d-324">Restart Manager</span></span>](../rstmgr/restart-manager-reference.md)
-   [<span data-ttu-id="93f9d-325">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="93f9d-325">Windows Installer</span></span>](../msi/windows-installer-portal.md)

## <a name="system-admin-and-management"></a><span data-ttu-id="93f9d-326">系統管理員與管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-326">System admin and management</span></span>

<span data-ttu-id="93f9d-327">[系統管理](../srvnodes/system-administration.md)介面可讓您安裝、設定及服務應用程式或系統。</span><span class="sxs-lookup"><span data-stu-id="93f9d-327">The [System administration](../srvnodes/system-administration.md) interfaces enable you to install, configure, and service applications or systems.</span></span>

-   [<span data-ttu-id="93f9d-328">開機設定資料 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="93f9d-328">Boot Configuration Data WMI Provider</span></span>](/previous-versions/windows/desktop/bcd/bcd-reference)
-   [<span data-ttu-id="93f9d-329">容錯移轉叢集</span><span class="sxs-lookup"><span data-stu-id="93f9d-329">Failover Clusters</span></span>](/previous-versions/windows/desktop/mscs/failover-cluster-apis-portal)
-   [<span data-ttu-id="93f9d-330">檔案伺服器資源管理員 (FSRM)</span><span class="sxs-lookup"><span data-stu-id="93f9d-330">File Server Resource Manager (FSRM)</span></span>](/previous-versions/windows/desktop/fsrm/fsrm-reference)
-   [<span data-ttu-id="93f9d-331">群組原則</span><span class="sxs-lookup"><span data-stu-id="93f9d-331">Group Policy</span></span>](/previous-versions/windows/desktop/Policy/group-policy-reference)
-   [<span data-ttu-id="93f9d-332">Microsoft Management Console (MMC) 2。0</span><span class="sxs-lookup"><span data-stu-id="93f9d-332">Microsoft Management Console (MMC) 2.0</span></span>](/previous-versions/windows/desktop/mmc/mmc-reference)
-   [<span data-ttu-id="93f9d-333">NetShell</span><span class="sxs-lookup"><span data-stu-id="93f9d-333">NetShell</span></span>](/previous-versions/windows/desktop/netshell/netshell-reference)
-   [<span data-ttu-id="93f9d-334">設定管理基礎結構</span><span class="sxs-lookup"><span data-stu-id="93f9d-334">Settings Management Infrastructure</span></span>](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   [<span data-ttu-id="93f9d-335">軟體清查記錄</span><span class="sxs-lookup"><span data-stu-id="93f9d-335">Software Inventory Logging</span></span>](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
-   [<span data-ttu-id="93f9d-336">軟體授權</span><span class="sxs-lookup"><span data-stu-id="93f9d-336">Software Licensing</span></span>](/previous-versions/windows/desktop/secslapi/software-licensing-api-reference)
-   [<span data-ttu-id="93f9d-337">重新開機管理員</span><span class="sxs-lookup"><span data-stu-id="93f9d-337">Restart Manager</span></span>](../rstmgr/restart-manager-portal.md)
-   [<span data-ttu-id="93f9d-338">設定管理基礎結構</span><span class="sxs-lookup"><span data-stu-id="93f9d-338">Settings Management Infrastructure</span></span>](/previous-versions/windows/desktop/smi/settings-management-infrastructure--smi-)
-   <span data-ttu-id="93f9d-339">[[系統還原]](../sr/system-restore-portal.md)</span><span class="sxs-lookup"><span data-stu-id="93f9d-339">[System Restore](../sr/system-restore-portal.md)</span></span>
-   [<span data-ttu-id="93f9d-340">系統關閉</span><span class="sxs-lookup"><span data-stu-id="93f9d-340">System Shutdown</span></span>](../shutdown/system-shutdown.md)
-   [<span data-ttu-id="93f9d-341">工作排程器</span><span class="sxs-lookup"><span data-stu-id="93f9d-341">Task Scheduler</span></span>](../taskschd/task-scheduler-start-page.md)
-   [<span data-ttu-id="93f9d-342">使用者存取記錄</span><span class="sxs-lookup"><span data-stu-id="93f9d-342">User Access Logging</span></span>](/previous-versions/windows/desktop/ual/user-access-logging-reference)
-   [<span data-ttu-id="93f9d-343">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="93f9d-343">Windows Virtual PC</span></span>](../vpc/virtual-pc-reference.md)
-   [<span data-ttu-id="93f9d-344">Microsoft Virtual Server</span><span class="sxs-lookup"><span data-stu-id="93f9d-344">Microsoft Virtual Server</span></span>](/previous-versions/windows/desktop/msvs/microsoft-virtual-server-reference)
-   [<span data-ttu-id="93f9d-345">網路負載平衡提供者</span><span class="sxs-lookup"><span data-stu-id="93f9d-345">Network Load Balancing Provider</span></span>](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-reference)
-   [<span data-ttu-id="93f9d-346">Windows Defender WMI v2</span><span class="sxs-lookup"><span data-stu-id="93f9d-346">Windows Defender WMI v2</span></span>](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
-   [<span data-ttu-id="93f9d-347">Windows Deployment Services</span><span class="sxs-lookup"><span data-stu-id="93f9d-347">Windows Deployment Services</span></span>](../wds/windows-deployment-services-portal.md)
-   [<span data-ttu-id="93f9d-348">Windows Genuine Advantage</span><span class="sxs-lookup"><span data-stu-id="93f9d-348">Windows Genuine Advantage</span></span>](/previous-versions/windows/desktop/wingen/windows-genuine-advantage-api-functions)
-   [<span data-ttu-id="93f9d-349">Windows 管理基礎結構</span><span class="sxs-lookup"><span data-stu-id="93f9d-349">Windows Management Infrastructure</span></span>](/previous-versions/windows/desktop/wmi_v2/wmi-reference)
-   [<span data-ttu-id="93f9d-350">Windows Management Instrumentation (WMI)</span><span class="sxs-lookup"><span data-stu-id="93f9d-350">Windows Management Instrumentation (WMI)</span></span>](../wmisdk/wmi-reference.md)
-   [<span data-ttu-id="93f9d-351">Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-351">Windows Remote Management</span></span>](../winrm/portal.md)
-   [<span data-ttu-id="93f9d-352">Windows 資源保護</span><span class="sxs-lookup"><span data-stu-id="93f9d-352">Windows Resource Protection</span></span>](../wfp/windows-resource-protection-portal.md)
-   <span data-ttu-id="93f9d-353">[Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-353">[Windows Server Update Services](/previous-versions/windows/desktop/ms744624(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-354">Windows 系統評定工具</span><span class="sxs-lookup"><span data-stu-id="93f9d-354">Windows System Assessment Tool</span></span>](../winsat/winsat-reference.md)
-   [<span data-ttu-id="93f9d-355">Windows Update 代理程式</span><span class="sxs-lookup"><span data-stu-id="93f9d-355">Windows Update Agent</span></span>](../wua_sdk/portal-client.md)

## <a name="networking-and-internet"></a><span data-ttu-id="93f9d-356">網路和網際網路</span><span class="sxs-lookup"><span data-stu-id="93f9d-356">Networking and internet</span></span>

<span data-ttu-id="93f9d-357">[網路](../devnotes/networking.md)api 可讓應用程式透過網路進行通訊。</span><span class="sxs-lookup"><span data-stu-id="93f9d-357">The [Networking](../devnotes/networking.md) APIs enable communication between applications over a network.</span></span> <span data-ttu-id="93f9d-358">您也可以建立和管理共用資源的存取權，例如目錄和網路印表機。</span><span class="sxs-lookup"><span data-stu-id="93f9d-358">You can also create and manage access to shared resources, such as directories and network printers.</span></span>

-   [<span data-ttu-id="93f9d-359">網域名稱系統 (DNS)</span><span class="sxs-lookup"><span data-stu-id="93f9d-359">Domain Name System (DNS)</span></span>](../dns/dns-reference.md)
-   [<span data-ttu-id="93f9d-360">動態主機設定通訊協定 (DHCP)</span><span class="sxs-lookup"><span data-stu-id="93f9d-360">Dynamic Host Configuration Protocol (DHCP)</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
-   [<span data-ttu-id="93f9d-361">傳真服務</span><span class="sxs-lookup"><span data-stu-id="93f9d-361">Fax Service</span></span>](/previous-versions/windows/desktop/fax/-mfax-fax-service-reference)
-   [<span data-ttu-id="93f9d-362">連線精靈</span><span class="sxs-lookup"><span data-stu-id="93f9d-362">Get Connected Wizard</span></span>](/previous-versions/windows/desktop/get_connected/get-connected-wizard-api-reference)
-   [<span data-ttu-id="93f9d-363">HTTP 伺服器</span><span class="sxs-lookup"><span data-stu-id="93f9d-363">HTTP Server</span></span>](../http/http-server-api-reference.md)
-   [<span data-ttu-id="93f9d-364">網際網路連線共用和防火牆</span><span class="sxs-lookup"><span data-stu-id="93f9d-364">Internet Connection Sharing and Firewall</span></span>](/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference)
-   [<span data-ttu-id="93f9d-365">IP 協助程式</span><span class="sxs-lookup"><span data-stu-id="93f9d-365">IP Helper</span></span>](../iphlp/ip-helper-function-reference.md)
-   [<span data-ttu-id="93f9d-366">IPv6 網際網路連線防火牆</span><span class="sxs-lookup"><span data-stu-id="93f9d-366">IPv6 Internet Connection Firewall</span></span>](/previous-versions/windows/desktop/ics/ipv6-firewall-configuration-reference)
-   [<span data-ttu-id="93f9d-367">管理資訊基礎</span><span class="sxs-lookup"><span data-stu-id="93f9d-367">Management Information Base</span></span>](/previous-versions/windows/desktop/mib/management-information-base-reference)
-   <span data-ttu-id="93f9d-368">[訊息佇列 (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-368">[Message Queuing (MSMQ)](/previous-versions/windows/desktop/legacy/ms700112(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-369">多播位址動態用戶端配置通訊協定 (MADCAP) </span><span class="sxs-lookup"><span data-stu-id="93f9d-369">Multicast Address Dynamic Client Allocation Protocol (MADCAP)</span></span>](/previous-versions/windows/desktop/madcap/madcap-reference)
-   [<span data-ttu-id="93f9d-370">網路位址轉譯 (NAT)</span><span class="sxs-lookup"><span data-stu-id="93f9d-370">Network Address Translation (NAT)</span></span>](/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference)
-   [<span data-ttu-id="93f9d-371">網路清單管理員 (NLM) </span><span class="sxs-lookup"><span data-stu-id="93f9d-371">Network List Manager (NLM)</span></span>](../nla/network-list-manager-api-reference.md)
-   [<span data-ttu-id="93f9d-372">網路管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-372">Network Management</span></span>](../netmgmt/network-management-reference.md)
-   [<span data-ttu-id="93f9d-373">網路共用管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-373">Network Share Management</span></span>](../netshare/network-share-management-reference.md)
-   [<span data-ttu-id="93f9d-374">對等</span><span class="sxs-lookup"><span data-stu-id="93f9d-374">Peer-to-Peer</span></span>](../p2psdk/portal.md)
-   [<span data-ttu-id="93f9d-375">QOS) 的服務品質 (</span><span class="sxs-lookup"><span data-stu-id="93f9d-375">Quality of Service (QOS)</span></span>](/previous-versions/windows/desktop/qos/qos-reference)
-   [<span data-ttu-id="93f9d-376">遠端程序呼叫</span><span class="sxs-lookup"><span data-stu-id="93f9d-376">Remote Procedure Call</span></span>](../rpc/reference.md)
-   [<span data-ttu-id="93f9d-377">路由及遠端存取服務 (RAS) </span><span class="sxs-lookup"><span data-stu-id="93f9d-377">Routing and Remote Access Service (RAS)</span></span>](../rras/portal.md)
-   [<span data-ttu-id="93f9d-378">簡易網路管理通訊協定 (SNMP)</span><span class="sxs-lookup"><span data-stu-id="93f9d-378">Simple Network Management Protocol (SNMP)</span></span>](../snmp/snmp-reference.md)
-   [<span data-ttu-id="93f9d-379">SMB 管理</span><span class="sxs-lookup"><span data-stu-id="93f9d-379">SMB Management</span></span>](/previous-versions/windows/desktop/smb/smb-management-api-portal)
-   [<span data-ttu-id="93f9d-380"> (TAPI 的電話語音應用程式設計介面) </span><span class="sxs-lookup"><span data-stu-id="93f9d-380">Telephony Application Programming Interfaces (TAPI)</span></span>](../tapi/telephony-application-programming-interfaces.md)
-   [<span data-ttu-id="93f9d-381">WebDAV</span><span class="sxs-lookup"><span data-stu-id="93f9d-381">WebDAV</span></span>](../webdav/webdav-api-reference.md)
-   [<span data-ttu-id="93f9d-382">WebSocket 通訊協定元件</span><span class="sxs-lookup"><span data-stu-id="93f9d-382">WebSocket Protocol Component</span></span>](../websock/web-socket-protocol-component-api-portal.md)
-   <span data-ttu-id="93f9d-383">無線網路功能：</span><span class="sxs-lookup"><span data-stu-id="93f9d-383">Wireless networking:</span></span>
    -   [<span data-ttu-id="93f9d-384">Bluetooth</span><span class="sxs-lookup"><span data-stu-id="93f9d-384">Bluetooth</span></span>](../bluetooth/bluetooth-reference.md)
    -   [<span data-ttu-id="93f9d-385">Irda</span><span class="sxs-lookup"><span data-stu-id="93f9d-385">IrDA</span></span>](/previous-versions/windows/desktop/irda/irda-and-windows-sockets-reference)
    -   [<span data-ttu-id="93f9d-386">行動寬頻</span><span class="sxs-lookup"><span data-stu-id="93f9d-386">Mobile Broadband</span></span>](../mbn/mobile-broadband-networks-api-reference.md)
    -   [<span data-ttu-id="93f9d-387">原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="93f9d-387">Native Wifi</span></span>](../nativewifi/native-wifi-reference.md)
    -   [<span data-ttu-id="93f9d-388">Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="93f9d-388">Windows Connect Now</span></span>](../wcn/windows-connect-now-reference.md)
    -   [<span data-ttu-id="93f9d-389">Windows 連線管理員</span><span class="sxs-lookup"><span data-stu-id="93f9d-389">Windows Connection Manager</span></span>](../wcm/windows-connection-manager-reference.md)
-   [<span data-ttu-id="93f9d-390">Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="93f9d-390">Windows Filtering Platform</span></span>](../fwp/fwp-reference.md)
-   [<span data-ttu-id="93f9d-391">具有進階安全性的 Windows 防火牆</span><span class="sxs-lookup"><span data-stu-id="93f9d-391">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference)
-   [<span data-ttu-id="93f9d-392">Windows HTTP 服務 (WinHTTP) </span><span class="sxs-lookup"><span data-stu-id="93f9d-392">Windows HTTP Services (WinHTTP)</span></span>](../winhttp/winhttp-reference.md)
-   [<span data-ttu-id="93f9d-393">Windows 網際網路 (WinINet) </span><span class="sxs-lookup"><span data-stu-id="93f9d-393">Windows Internet (WinINet)</span></span>](../wininet/wininet-reference.md)
-   [<span data-ttu-id="93f9d-394">Windows 網路 (WNet) </span><span class="sxs-lookup"><span data-stu-id="93f9d-394">Windows Networking (WNet)</span></span>](../wnet/windows-networking-reference.md)
-   [<span data-ttu-id="93f9d-395">Windows 網路虛擬化</span><span class="sxs-lookup"><span data-stu-id="93f9d-395">Windows Network Virtualization</span></span>](/previous-versions/windows/desktop/wnv/windows-network-virtualization-portal)
-   <span data-ttu-id="93f9d-396">[Windows RSS 平臺](/previous-versions/windows/desktop/ms684702(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-396">[Windows RSS Platform](/previous-versions/windows/desktop/ms684702(v=vs.85))</span></span>
-   [<span data-ttu-id="93f9d-397">Windows 通訊端 (Winsock) </span><span class="sxs-lookup"><span data-stu-id="93f9d-397">Windows Sockets (Winsock)</span></span>](../winsock/winsock-reference.md)
-   [<span data-ttu-id="93f9d-398">Windows Web 服務</span><span class="sxs-lookup"><span data-stu-id="93f9d-398">Windows Web Services</span></span>](../wsw/windows-web-services-reference.md)
-   [<span data-ttu-id="93f9d-399">XML HTTP 擴充要求</span><span class="sxs-lookup"><span data-stu-id="93f9d-399">XML HTTP Extended Request</span></span>](/previous-versions/windows/desktop/ixhr2/ixmlhttprequest2-portal)

## <a name="deprecated-or-legacy-apis"></a><span data-ttu-id="93f9d-400">已淘汰或舊版 Api</span><span class="sxs-lookup"><span data-stu-id="93f9d-400">Deprecated or legacy APIs</span></span>

<span data-ttu-id="93f9d-401">以下是從 Windows 用戶端和伺服器作業系統淘汰或取代或淘汰的技術和 Api。</span><span class="sxs-lookup"><span data-stu-id="93f9d-401">The following are technologies and APIs that are outdated or have been replaced or deprecated from the Windows client and server operating systems.</span></span>

-   <span data-ttu-id="93f9d-402">[DirectMusic](/previous-versions/ms807133(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="93f9d-402">[DirectMusic](/previous-versions/ms807133(v=msdn.10))</span></span>
-   <span data-ttu-id="93f9d-403">[DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-403">[DirectSound](/previous-versions/windows/desktop/ee416975(v=vs.85))</span></span>
-   <span data-ttu-id="93f9d-404">Microsoft [UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10))現在隨附于[microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="93f9d-404">[Microsoft UDDI SDK](/previous-versions/windows/desktop/aa966237(v=bts.10)) is now included with [Microsoft BizTalk Server](/previous-versions/bb905520(v=msdn.10)).</span></span>
-   [<span data-ttu-id="93f9d-405">網路動態資料交換 (DDE) </span><span class="sxs-lookup"><span data-stu-id="93f9d-405">Network Dynamic Data Exchange (DDE)</span></span>](../ipc/network-dde-reference.md)
-   <span data-ttu-id="93f9d-406">[遠端安裝服務](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10))：改用 [Windows 部署服務](../wds/windows-deployment-services-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="93f9d-406">[Remote Installation Service](/previous-versions/windows/it-pro/windows-server-2003/cc786442(v=ws.10)): Use [Windows Deployment Services](../wds/windows-deployment-services-portal.md) instead.</span></span>
-   <span data-ttu-id="93f9d-407">[虛擬磁碟服務 (VDS) ](../vds/vds-reference.md)：請改用 [Windows 存放裝置管理](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) 。</span><span class="sxs-lookup"><span data-stu-id="93f9d-407">[Virtual Disk Service (VDS)](../vds/vds-reference.md): Use [Windows Storage Management](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal) instead.</span></span>
-   <span data-ttu-id="93f9d-408">終端機服務：使用 [遠端桌面服務](../termserv/terminal-services-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="93f9d-408">Terminal Services: Use [Remote Desktop Services](../termserv/terminal-services-reference.md).</span></span>
-   <span data-ttu-id="93f9d-409">[Windows Media Rights Manager](/previous-versions//bb614742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f9d-409">[Windows Media Rights Manager](/previous-versions//bb614742(v=vs.85))</span></span>
-   <span data-ttu-id="93f9d-410">[Windows 訊息中心 (MAPI) ](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi)：請改用 [Office MAPI](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) 。</span><span class="sxs-lookup"><span data-stu-id="93f9d-410">[Windows Messaging (MAPI)](/previous-versions/windows/desktop/windowsmapi/mapi-stub-library-and-simple-mapi): Use [Office MAPI](/previous-versions/office/developer/office-2007/cc765775(v=office.12)) instead.</span></span>
-   <span data-ttu-id="93f9d-411">[Windows 小工具平台](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal)：改為建立 UWP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="93f9d-411">[Windows Gadget Platform](/previous-versions/windows/desktop/gadgetplatform/windows-gadget-platform-portal): Create UWP apps instead.</span></span>
-   <span data-ttu-id="93f9d-412">[Windows 提要](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry)欄位：改為建立 UWP 應用程式。</span><span class="sxs-lookup"><span data-stu-id="93f9d-412">[Windows Sidebar](/previous-versions/windows/desktop/sidebar/-sidebar-ref-entry): Create UWP apps instead.</span></span>
-   <span data-ttu-id="93f9d-413">[Windows SideShow](/previous-versions//ms744179(v=vs.85))：沒有取代。</span><span class="sxs-lookup"><span data-stu-id="93f9d-413">[Windows SideShow](/previous-versions//ms744179(v=vs.85)): No replacement.</span></span>
-   [<span data-ttu-id="93f9d-414">WPF 點陣圖效果</span><span class="sxs-lookup"><span data-stu-id="93f9d-414">WPF Bitmap Effects</span></span>](/previous-versions/windows/desktop/wibe/-wibe-about-bitmapeffects)
