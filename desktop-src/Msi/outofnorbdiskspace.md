---
description: 如果任何以安裝目標為目標的磁片區都沒有足夠的磁碟空間可容納安裝，安裝程式會將 OutOfNoRbDiskSpace 屬性設定為 True。
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: OutOfNoRbDiskSpace 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990708"
---
# <a name="outofnorbdiskspace-property"></a><span data-ttu-id="69ad1-103">OutOfNoRbDiskSpace 屬性</span><span class="sxs-lookup"><span data-stu-id="69ad1-103">OutOfNoRbDiskSpace property</span></span>

<span data-ttu-id="69ad1-104">如果任何以安裝目標為目標的磁片區都沒有足夠的磁碟空間可容納安裝，安裝程式會將 **OutOfNoRbDiskSpace** 屬性設定為 True。</span><span class="sxs-lookup"><span data-stu-id="69ad1-104">The installer sets the **OutOfNoRbDiskSpace** property to True if any volume that is a target of the installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="69ad1-105">在此情況下，即使已停用 rollback， **OutOfNoRbDiskSpace** 屬性也會設定為 True。</span><span class="sxs-lookup"><span data-stu-id="69ad1-105">In this case, the **OutOfNoRbDiskSpace** property is set to True even if rollback has been disabled.</span></span> <span data-ttu-id="69ad1-106">如果所有磁片區有足夠的空間，此值會是 False。</span><span class="sxs-lookup"><span data-stu-id="69ad1-106">If all volumes have sufficient space, the value is False.</span></span>

<span data-ttu-id="69ad1-107">當 [**OutOfDiskSpace**](outofdiskspace.md) 屬性為 True，而且 **OutOfNoRbDiskSpace** 屬性為 False 時，安裝封裝的開發人員可以處理這種情況，方法是撰寫使用者介面，讓使用者可以選擇停用復原並繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="69ad1-107">A developer of an installation package can handle the situation when the [**OutOfDiskSpace**](outofdiskspace.md) property is True and the **OutOfNoRbDiskSpace** property is False by authoring a user interface that presents the user with an option to disable rollback and continue the installation.</span></span> <span data-ttu-id="69ad1-108">如需有條件地顯示對話方塊的詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="69ad1-108">For information about conditionally displaying a dialog box, see [ControlEvent Overview](controlevent-overview.md).</span></span> <span data-ttu-id="69ad1-109">如需停用回復的詳細資訊，請參閱 [EnableRollback ControlEvent](enablerollback-controlevent.md)。</span><span class="sxs-lookup"><span data-stu-id="69ad1-109">For information about disabling rollback, see [EnableRollback ControlEvent](enablerollback-controlevent.md).</span></span>

<span data-ttu-id="69ad1-110">**OutOfNoRbDiskSpace** 屬性在 [CostFinalize 動作](costfinalize-action.md)執行之後的任何時間都有效。</span><span class="sxs-lookup"><span data-stu-id="69ad1-110">The **OutOfNoRbDiskSpace** property is valid at any time after the [CostFinalize action](costfinalize-action.md) has been executed.</span></span> <span data-ttu-id="69ad1-111">**OutOfNoRbDiskSpace** 屬性狀態會在重新計算總安裝成本時動態更新 (例如，任何功能的安裝狀態透過 [選取對話方塊](selection-dialog.md)) 變更時。</span><span class="sxs-lookup"><span data-stu-id="69ad1-111">The **OutOfNoRbDiskSpace** property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection dialog](selection-dialog.md)).</span></span> <span data-ttu-id="69ad1-112">選取解決動作會使用這個值來取消安裝並產生對話方塊。</span><span class="sxs-lookup"><span data-stu-id="69ad1-112">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="69ad1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="69ad1-113">Requirements</span></span>



| <span data-ttu-id="69ad1-114">需求</span><span class="sxs-lookup"><span data-stu-id="69ad1-114">Requirement</span></span> | <span data-ttu-id="69ad1-115">值</span><span class="sxs-lookup"><span data-stu-id="69ad1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69ad1-116">版本</span><span class="sxs-lookup"><span data-stu-id="69ad1-116">Version</span></span><br/> | <span data-ttu-id="69ad1-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="69ad1-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="69ad1-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="69ad1-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="69ad1-119">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="69ad1-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="69ad1-120">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="69ad1-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69ad1-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69ad1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ad1-122">屬性</span><span class="sxs-lookup"><span data-stu-id="69ad1-122">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="69ad1-123">ControlEvent 總覽</span><span class="sxs-lookup"><span data-stu-id="69ad1-123">ControlEvent Overview</span></span>](controlevent-overview.md)
</dt> <dt>

[<span data-ttu-id="69ad1-124">**OutOfDiskSpace 屬性**</span><span class="sxs-lookup"><span data-stu-id="69ad1-124">**OutOfDiskSpace property**</span></span>](outofdiskspace.md)
</dt> <dt>

[<span data-ttu-id="69ad1-125">EnableRollback ControlEvent</span><span class="sxs-lookup"><span data-stu-id="69ad1-125">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)
</dt> <dt>

[<span data-ttu-id="69ad1-126">CostFinalize 動作</span><span class="sxs-lookup"><span data-stu-id="69ad1-126">CostFinalize action</span></span>](costfinalize-action.md)
</dt> <dt>

[<span data-ttu-id="69ad1-127">選取對話方塊</span><span class="sxs-lookup"><span data-stu-id="69ad1-127">Selection dialog</span></span>](selection-dialog.md)
</dt> </dl>

 

 




