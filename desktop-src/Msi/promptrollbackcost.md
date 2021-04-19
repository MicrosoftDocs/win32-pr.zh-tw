---
description: PROMPTROLLBACKCOST 屬性會指定如果已啟用復原安裝功能，且沒有足夠的磁碟空間來完成安裝，則安裝程式所採取的動作。PROMPTROLLBACKCOST 可能的值如下所示。ValueActionPDisplay 對話方塊，詢問是否要在沒有回復的情況下繼續進行。DDisable 復原並繼續，而不要求使用者。FFail 與磁碟空間不足的錯誤提示。
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: PROMPTROLLBACKCOST 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000975"
---
# <a name="promptrollbackcost-property"></a><span data-ttu-id="12531-103">PROMPTROLLBACKCOST 屬性</span><span class="sxs-lookup"><span data-stu-id="12531-103">PROMPTROLLBACKCOST property</span></span>

<span data-ttu-id="12531-104">**PROMPTROLLBACKCOST** 屬性會指定如果已啟用 [復原安裝](rollback-installation.md)功能，且沒有足夠的磁碟空間來完成安裝，則安裝程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="12531-104">The **PROMPTROLLBACKCOST** property specifies the action the installer takes if [rollback installation](rollback-installation.md) capabilities are enabled and there is insufficient disk space to complete the installation.</span></span>

<span data-ttu-id="12531-105">**PROMPTROLLBACKCOST** 可能的值如下所示。</span><span class="sxs-lookup"><span data-stu-id="12531-105">The possible values of **PROMPTROLLBACKCOST** are as follows.</span></span>



| <span data-ttu-id="12531-106">值</span><span class="sxs-lookup"><span data-stu-id="12531-106">Value</span></span> | <span data-ttu-id="12531-107">動作</span><span class="sxs-lookup"><span data-stu-id="12531-107">Action</span></span>                                                              |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="12531-108">P</span><span class="sxs-lookup"><span data-stu-id="12531-108">P</span></span>     | <span data-ttu-id="12531-109">顯示對話方塊，詢問是否要在沒有回復的情況下繼續進行。</span><span class="sxs-lookup"><span data-stu-id="12531-109">Display a dialog box asking whether to continue without a rollback.</span></span> |
| <span data-ttu-id="12531-110">D</span><span class="sxs-lookup"><span data-stu-id="12531-110">D</span></span>     | <span data-ttu-id="12531-111">停用復原並繼續，而不要求使用者。</span><span class="sxs-lookup"><span data-stu-id="12531-111">Disable rollback and continue without asking user.</span></span>                  |
| <span data-ttu-id="12531-112">F</span><span class="sxs-lookup"><span data-stu-id="12531-112">F</span></span>     | <span data-ttu-id="12531-113">發生磁碟空間不足的錯誤提示時失敗。</span><span class="sxs-lookup"><span data-stu-id="12531-113">Fail with the out-of-disk-space error prompt.</span></span>                       |



 

## <a name="remarks"></a><span data-ttu-id="12531-114">備註</span><span class="sxs-lookup"><span data-stu-id="12531-114">Remarks</span></span>

<span data-ttu-id="12531-115">當使用者介面是在基本或無 UI 層級執行時，安裝程式會自動處理所有的磁碟空間邏輯。</span><span class="sxs-lookup"><span data-stu-id="12531-115">When the user interface is run at the Basic or no UI level, the installer handles all the out-of-disk-space logic automatically.</span></span>

<span data-ttu-id="12531-116">當使用者介面在完整層級執行時，可以提供其他選項（例如，在繼續進行復原之前提示）、停用復原，或在磁片已滿時繼續進行而不回復。</span><span class="sxs-lookup"><span data-stu-id="12531-116">When the user interface runs at the Full level, the user can be given additional options, such as prompting before proceeding with a rollback, disabling rollback, or proceeding without rollback when the disk is full.</span></span> <span data-ttu-id="12531-117">封裝開發人員可自行撰寫對話方塊順序，為使用者提供適當的選擇。</span><span class="sxs-lookup"><span data-stu-id="12531-117">It is up to the package developer to author the dialog box sequence to provide the appropriate choices to the user.</span></span> <span data-ttu-id="12531-118">可用來進行這項作業的元素有 [EnableRollback ControlEvent](enablerollback-controlevent.md)、 [**OutOfDiskSpace**](outofdiskspace.md) property、 [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) 屬性和 **PROMPTROLLBACKCOST** 屬性。</span><span class="sxs-lookup"><span data-stu-id="12531-118">The elements available to do this are the [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property, and the **PROMPTROLLBACKCOST** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="12531-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="12531-119">Requirements</span></span>



| <span data-ttu-id="12531-120">需求</span><span class="sxs-lookup"><span data-stu-id="12531-120">Requirement</span></span> | <span data-ttu-id="12531-121">值</span><span class="sxs-lookup"><span data-stu-id="12531-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12531-122">版本</span><span class="sxs-lookup"><span data-stu-id="12531-122">Version</span></span><br/> | <span data-ttu-id="12531-123">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="12531-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="12531-124">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="12531-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="12531-125">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="12531-125">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="12531-126">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="12531-126">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12531-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12531-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12531-128">屬性</span><span class="sxs-lookup"><span data-stu-id="12531-128">Properties</span></span>](properties.md)
</dt> </dl>

 

 




