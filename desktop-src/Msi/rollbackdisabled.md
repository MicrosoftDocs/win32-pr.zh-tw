---
description: 停用 rollback 時，安裝程式會設定 RollbackDisabled 屬性。
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: RollbackDisabled 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982565"
---
# <a name="rollbackdisabled-property"></a><span data-ttu-id="38d2e-103">RollbackDisabled 屬性</span><span class="sxs-lookup"><span data-stu-id="38d2e-103">RollbackDisabled property</span></span>

<span data-ttu-id="38d2e-104">停用 rollback 時，安裝程式會設定 **RollbackDisabled** 屬性。</span><span class="sxs-lookup"><span data-stu-id="38d2e-104">The installer sets the **RollbackDisabled** property when rollback has been disabled.</span></span> <span data-ttu-id="38d2e-105">**RollbackDisabled** 可供需要確認安裝程式未停用復原的封裝作者使用。</span><span class="sxs-lookup"><span data-stu-id="38d2e-105">**RollbackDisabled** is used by package authors who need to ensure that the installer has not disabled rollback.</span></span> <span data-ttu-id="38d2e-106">**RollbackDisabled** 屬性可以在條件運算式中使用，以在設定 **RollbackDisabled** 屬性時有效拒絕繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="38d2e-106">The **RollbackDisabled** property can be used in a conditional expression that effectively refuses to continue with the installation if **RollbackDisabled** property is set.</span></span>

## <a name="default-value"></a><span data-ttu-id="38d2e-107">預設值</span><span class="sxs-lookup"><span data-stu-id="38d2e-107">Default Value</span></span>

<span data-ttu-id="38d2e-108">預設會啟用復原。</span><span class="sxs-lookup"><span data-stu-id="38d2e-108">By default, rollback is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="38d2e-109">備註</span><span class="sxs-lookup"><span data-stu-id="38d2e-109">Remarks</span></span>

<span data-ttu-id="38d2e-110">由於 [rollback](rollback-custom-actions.md) 和 [commit](commit-custom-actions.md) 在停用回復時不會執行，因此安裝程式無法在安裝期間正確地安裝在交易中使用這些自訂動作類型的封裝。</span><span class="sxs-lookup"><span data-stu-id="38d2e-110">Because [rollback](rollback-custom-actions.md) and [commit](commit-custom-actions.md) do not run while rollback is disabled, the installer cannot properly install a package that uses these types of custom actions in a transaction during the installation.</span></span> <span data-ttu-id="38d2e-111">在此情況下，套件的作者應包含使用 DisableRollback 的條件，以防止在停用復原時繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="38d2e-111">In this case, the author of the package should include a condition using DisableRollback that prevents the installation from continuing if rollback is disabled.</span></span>

<span data-ttu-id="38d2e-112">系統管理員可以設定 DisableRollback 原則值，作為指派系統策略的一部分。</span><span class="sxs-lookup"><span data-stu-id="38d2e-112">The DisableRollback policy value can be set by an administrator as a part of assigning system policy.</span></span> <span data-ttu-id="38d2e-113">除非必要，否則建議系統管理員不要停用復原。</span><span class="sxs-lookup"><span data-stu-id="38d2e-113">Administrators are advised to not disable rollback unless necessary.</span></span> <span data-ttu-id="38d2e-114">如需 DisableRollback 原則值的詳細資訊，請參閱 [系統原則](system-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="38d2e-114">For more information about DisableRollback policy value, see [System Policy](system-policy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38d2e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="38d2e-115">Requirements</span></span>



| <span data-ttu-id="38d2e-116">需求</span><span class="sxs-lookup"><span data-stu-id="38d2e-116">Requirement</span></span> | <span data-ttu-id="38d2e-117">值</span><span class="sxs-lookup"><span data-stu-id="38d2e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38d2e-118">版本</span><span class="sxs-lookup"><span data-stu-id="38d2e-118">Version</span></span><br/> | <span data-ttu-id="38d2e-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="38d2e-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="38d2e-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="38d2e-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="38d2e-121">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="38d2e-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="38d2e-122">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="38d2e-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38d2e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38d2e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d2e-124">屬性</span><span class="sxs-lookup"><span data-stu-id="38d2e-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="38d2e-125">復原安裝</span><span class="sxs-lookup"><span data-stu-id="38d2e-125">Rollback Installation</span></span>](rollback-installation.md)
</dt> <dt>

[<span data-ttu-id="38d2e-126">系統原則</span><span class="sxs-lookup"><span data-stu-id="38d2e-126">System Policy</span></span>](system-policy.md)
</dt> <dt>

[<span data-ttu-id="38d2e-127">復原自訂動作</span><span class="sxs-lookup"><span data-stu-id="38d2e-127">rollback custom actions</span></span>](rollback-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="38d2e-128">認可自訂動作</span><span class="sxs-lookup"><span data-stu-id="38d2e-128">commit custom actions</span></span>](commit-custom-actions.md)
</dt> </dl>

 

 




