---
description: '[重新開機] 屬性會抑制系統重新開機的特定提示。'
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: 重新開機屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998864"
---
# <a name="reboot-property"></a><span data-ttu-id="4bf5b-103">重新開機屬性</span><span class="sxs-lookup"><span data-stu-id="4bf5b-103">REBOOT property</span></span>

<span data-ttu-id="4bf5b-104">[ **重新開機** ] 屬性會抑制系統重新開機的特定提示。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-104">The **REBOOT** property suppresses certain prompts for a restart of the system.</span></span> <span data-ttu-id="4bf5b-105">系統管理員通常會使用此內容搭配一系列的安裝，在最後一次只重新開機時安裝數項產品。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-105">An administrator typically uses this property with a series of installations to install several products at the same time with only one restart at the end.</span></span> <span data-ttu-id="4bf5b-106">如需詳細資訊，請參閱 [系統重新開機](system-reboots.md)。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-106">For more information, see [System Reboots](system-reboots.md).</span></span>

<span data-ttu-id="4bf5b-107">[ForceReboot](forcereboot-action.md)和[ScheduleReboot](schedulereboot-action.md)動作會通知安裝程式提示使用者重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-107">The [ForceReboot](forcereboot-action.md) and [ScheduleReboot](schedulereboot-action.md) actions inform the installer to prompt the user to restart the system.</span></span> <span data-ttu-id="4bf5b-108">安裝程式也可以判斷序列中是否有任何 ForceReboot 或 ScheduleReboot 動作，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-108">The installer can also determine that a restart is necessary whether there are any ForceReboot or ScheduleReboot actions in the sequence.</span></span> <span data-ttu-id="4bf5b-109">例如，安裝程式在安裝期間需要取代任何使用中的檔案時，會自動提示重新開機。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-109">For example, the installer automatically prompts for a restart if it needs to replace any files in use during the installation.</span></span>

<span data-ttu-id="4bf5b-110">您可以設定 [ **重新開機** ] 屬性來隱藏某些提示以重新開機，如下所示。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-110">You can suppress certain prompts for restarts by setting the **REBOOT** property as follows.</span></span>



| <span data-ttu-id="4bf5b-111">重新開機值</span><span class="sxs-lookup"><span data-stu-id="4bf5b-111">REBOOT value</span></span>   | <span data-ttu-id="4bf5b-112">Description</span><span class="sxs-lookup"><span data-stu-id="4bf5b-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf5b-113">Force</span><span class="sxs-lookup"><span data-stu-id="4bf5b-113">Force</span></span>          | <span data-ttu-id="4bf5b-114">一律在安裝結束時提示您重新開機。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-114">Always prompt for a restart at the end of the installation.</span></span> <span data-ttu-id="4bf5b-115">UI 一律會提示使用者在結束時重新開機選項。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-115">The UI always prompts the user with an option to restart at the end.</span></span> <span data-ttu-id="4bf5b-116">如果沒有使用者介面，而且這不是 [多重封裝安裝](multiple-package-installations.md)，系統會在安裝結束時自動重新開機。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-116">If there is no user interface, and this is not a [multiple-package installation](multiple-package-installations.md), the system automatically restarts at the end of the installation.</span></span> <span data-ttu-id="4bf5b-117">如果這是多套件安裝，系統就不會自動重新開機系統，且安裝程式會傳回錯誤 \_ 成功 \_ 重新開機 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-117">If this is a multiple-package installation, there is no automatic restart of the system and the installer returns ERROR\_SUCCESS\_REBOOT\_REQUIRED.</span></span> |
| <span data-ttu-id="4bf5b-118">隱藏</span><span class="sxs-lookup"><span data-stu-id="4bf5b-118">Suppress</span></span>       | <span data-ttu-id="4bf5b-119">抑制在安裝結束時重新開機的提示。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-119">Suppress prompts for a restart at the end of the installation.</span></span> <span data-ttu-id="4bf5b-120">在安裝期間，安裝程式仍會提示使用者在遇到 [ForceReboot 動作](forcereboot-action.md)時重新開機。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-120">The installer still prompts the user with an option to restart during the installation whenever it encounters the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="4bf5b-121">如果沒有使用者介面，系統會在每個 ForceReboot 自動重新開機。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-121">If there is no user interface, the system automatically restarts at each ForceReboot.</span></span> <span data-ttu-id="4bf5b-122">在安裝結束時重新開機 (例如，嘗試安裝使用中的檔案時所造成的) 已隱藏。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-122">Restarts at the end of the installation (for example, caused by an attempt to install a file in use) are suppressed.</span></span>                                    |
| <span data-ttu-id="4bf5b-123">ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="4bf5b-123">ReallySuppress</span></span> | <span data-ttu-id="4bf5b-124">在安裝期間隱藏 ForceReboot 所起始的所有重新開機和重新開機提示。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-124">Suppress all restarts and restart prompts initiated by ForceReboot during the installation.</span></span> <span data-ttu-id="4bf5b-125">在安裝結束時隱藏所有重新開機並重新啟動提示。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-125">Suppress all restarts and restart prompts at the end of the installation.</span></span> <span data-ttu-id="4bf5b-126">重新開機提示和重新開機本身都會隱藏。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-126">Both the restart prompt and the restart itself are suppressed.</span></span> <span data-ttu-id="4bf5b-127">例如，在安裝結束時重新開機，因為嘗試安裝使用中的檔案，所以會隱藏。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-127">For example, restarts at the end of the installation, caused by an attempt to install a file in use, are suppressed.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="4bf5b-128">備註</span><span class="sxs-lookup"><span data-stu-id="4bf5b-128">Remarks</span></span>

<span data-ttu-id="4bf5b-129">安裝程式只會評估 **重新開機** 屬性的第一個字元。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-129">The installer only evaluates the first character of the **REBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf5b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bf5b-130">Requirements</span></span>



| <span data-ttu-id="4bf5b-131">需求</span><span class="sxs-lookup"><span data-stu-id="4bf5b-131">Requirement</span></span> | <span data-ttu-id="4bf5b-132">值</span><span class="sxs-lookup"><span data-stu-id="4bf5b-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf5b-133">版本</span><span class="sxs-lookup"><span data-stu-id="4bf5b-133">Version</span></span><br/> | <span data-ttu-id="4bf5b-134">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-134">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4bf5b-135">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-135">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4bf5b-136">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-136">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4bf5b-137">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="4bf5b-137">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bf5b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bf5b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf5b-139">屬性</span><span class="sxs-lookup"><span data-stu-id="4bf5b-139">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="4bf5b-140">**REBOOTPROMPT 屬性**</span><span class="sxs-lookup"><span data-stu-id="4bf5b-140">**REBOOTPROMPT Property**</span></span>](rebootprompt.md)
</dt> <dt>

[<span data-ttu-id="4bf5b-141">系統重新開機</span><span class="sxs-lookup"><span data-stu-id="4bf5b-141">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




