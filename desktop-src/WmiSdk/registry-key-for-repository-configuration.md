---
description: Windows Management Instrumentation (WMI) 具有新的登錄機碼，可啟用或停用 AutoRestore 存放庫功能。
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: 存放庫設定的登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989934"
---
# <a name="registry-key-for-repository-configuration"></a><span data-ttu-id="c5f2a-103">存放庫設定的登錄機碼</span><span class="sxs-lookup"><span data-stu-id="c5f2a-103">Registry Key for Repository Configuration</span></span>

<span data-ttu-id="c5f2a-104">Windows Management Instrumentation (WMI) 具有新的登錄機碼，可啟用或停用 AutoRestore 存放庫功能。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-104">Windows Management Instrumentation (WMI) has a new registry key to enable or disable the AutoRestore repository feature..</span></span> <span data-ttu-id="c5f2a-105">如需還原 WMI 儲存機制的詳細資訊，請參閱 [備份或還原 wmi 存放庫](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-105">For more information on restoring the WMI repository, see [Backup or Restore WMI Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span></span>

<span data-ttu-id="c5f2a-106">在 Windows 7 中，預設行為是在偵測到存放庫損毀時，從備份的版本自動還原存放庫。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-106">In Windows 7, the default behavior is to auto-restore a repository from a backed-up version if a repository corruption is detected.</span></span> <span data-ttu-id="c5f2a-107">WMI 提供 **AutoRestoreEnabled** 登錄值以停用此功能。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-107">WMI provides the **AutoRestoreEnabled** registry value to disable this feature.</span></span>

<span data-ttu-id="c5f2a-108">WMI 的登錄機碼位於 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ 的登錄中。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-108">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<dl> <dt>

<span data-ttu-id="c5f2a-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span><span class="sxs-lookup"><span data-stu-id="c5f2a-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="c5f2a-110">可讓使用者決定是否要使用 AutoRestore 存放庫功能。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-110">Enables the user to determine whether or not to use the AutoRestore repository feature.</span></span> <span data-ttu-id="c5f2a-111">依預設，此機碼設定為1，且已啟用 AutoRestore 存放庫功能。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-111">By default this key is set to 1 and the AutoRestore Repository feature is enabled.</span></span>

<span data-ttu-id="c5f2a-112">可能的設定如下：</span><span class="sxs-lookup"><span data-stu-id="c5f2a-112">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="c5f2a-113"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="c5f2a-113"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="c5f2a-114">Disabled</span><span class="sxs-lookup"><span data-stu-id="c5f2a-114">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="c5f2a-115"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="c5f2a-115"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="c5f2a-116">已啟用</span><span class="sxs-lookup"><span data-stu-id="c5f2a-116">Enabled</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="c5f2a-117">您可以使用群組原則管理主控台 (GPMC) 來修改 **AutoRestoreEnabled** 登錄值。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-117">The **AutoRestoreEnabled** registry value can be modified by using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="c5f2a-118">如需詳細資訊，請參閱 [群組原則管理主控台](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-118">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="c5f2a-119">此程式提供有關如何啟用或停用 AutoRestore 儲存機制功能的詳細資料：</span><span class="sxs-lookup"><span data-stu-id="c5f2a-119">This procedure provides details about how to enable or disable the AutoRestore repository feature:</span></span>

<span data-ttu-id="c5f2a-120">**使用群組原則來變更 **AutoRestoreEnabled** 索引鍵的預設值**</span><span class="sxs-lookup"><span data-stu-id="c5f2a-120">**To change the default value of the **AutoRestoreEnabled** key by using Group Policy**</span></span>

1.  <span data-ttu-id="c5f2a-121">開啟 GPMC。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-121">Open the GPMC.</span></span>
2.  <span data-ttu-id="c5f2a-122"> (GPO) 建立群組原則物件。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-122">Create a Group Policy object (GPO).</span></span>
3.  <span data-ttu-id="c5f2a-123">編輯 GPO。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-123">Edit the GPO.</span></span>
4.  <span data-ttu-id="c5f2a-124">流覽至 [喜好設定]/[Windows 設定]/[登錄]。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-124">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="c5f2a-125">以滑鼠右鍵按一下並選取 [新增]。 登錄。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-125">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="c5f2a-126">此動作會顯示使用者介面，您可以在其中輸入登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-126">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="c5f2a-127">選取 [ **更新** ] 命令。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-127">Select the **Update** command.</span></span>
7.  <span data-ttu-id="c5f2a-128">選取下列登錄機碼路徑： **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ WBEM \\ CIMOM**。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-128">Select the following registry key path: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM**.</span></span>
8.  <span data-ttu-id="c5f2a-129">在 [ **名稱** ] 欄位中，輸入 **AutoRestoreEnabled**。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-129">In the **name** field, enter **AutoRestoreEnabled**.</span></span>
9.  <span data-ttu-id="c5f2a-130">在 [ **資料** ] 欄位中，輸入0以停用，或輸入1以啟用 AutoRestore 存放庫功能。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-130">In the **data** field, enter 0 to disable or 1 to enable the AutoRestore repository feature.</span></span>
10. <span data-ttu-id="c5f2a-131">按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="c5f2a-131">Click OK.</span></span>

 

 
