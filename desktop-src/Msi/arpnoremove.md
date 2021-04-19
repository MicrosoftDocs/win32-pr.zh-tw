---
description: 設定 ARPNOREMOVE 屬性會在移除產品的主控台中停用 [新增或移除程式] 功能。
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: ARPNOREMOVE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf8960234456a7010fb81cb195d63d4c5c79bb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000802"
---
# <a name="arpnoremove-property"></a><span data-ttu-id="4c470-103">ARPNOREMOVE 屬性</span><span class="sxs-lookup"><span data-stu-id="4c470-103">ARPNOREMOVE property</span></span>

<span data-ttu-id="4c470-104">設定 **ARPNOREMOVE** 屬性會在移除產品的 **主控台** 中停用 [**新增或移除程式**] 功能。</span><span class="sxs-lookup"><span data-stu-id="4c470-104">Setting the **ARPNOREMOVE** property disables the **Add or Remove Programs** functionality in **Control Panel** that removes the product.</span></span> <span data-ttu-id="4c470-105">針對 Windows 2000，這會從 **主控台** 中的 [**新增或移除程式**] 停用產品的 [**移除**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4c470-105">For Windows 2000, this disables the **Remove** button for the product from the **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="4c470-106">針對較舊的作業系統，這會影響在 **主控台** 的 [**新增或移除程式**] 上，將產品從已安裝的產品清單中移除。</span><span class="sxs-lookup"><span data-stu-id="4c470-106">For earlier operating systems, this has the effect of removing the product from the list of installed products on the **Add or Remove Programs** in **Control Panel**.</span></span>

<span data-ttu-id="4c470-107">如果已設定 **ARPNOREMOVE** 屬性， [RegisterProduct 動作](registerproduct-action.md) 會在登錄機碼下寫入 "NoRemove" 值：</span><span class="sxs-lookup"><span data-stu-id="4c470-107">If the **ARPNOREMOVE** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoRemove" under the registry key:</span></span>

<span data-ttu-id="4c470-108">**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**卸載** \\ **{*產品金鑰*}**</span><span class="sxs-lookup"><span data-stu-id="4c470-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="4c470-109">設定 **ARPNOREMOVE** 屬性可防止在此機碼下寫入 UninstallString 值。</span><span class="sxs-lookup"><span data-stu-id="4c470-109">Setting the **ARPNOREMOVE** property prevents the UninstallString value from being written under this key.</span></span> <span data-ttu-id="4c470-110">UnistallString 值是用來移除產品的命令列，而不是重新設定產品。</span><span class="sxs-lookup"><span data-stu-id="4c470-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c470-111">備註</span><span class="sxs-lookup"><span data-stu-id="4c470-111">Remarks</span></span>

<span data-ttu-id="4c470-112">例如，您可以在自訂轉換期間設定這個屬性，以防止使用者移除系統管理員自訂。</span><span class="sxs-lookup"><span data-stu-id="4c470-112">For example, this property can be set during a customization transform to prevent users from removing an administrator customization.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c470-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c470-113">Requirements</span></span>



| <span data-ttu-id="4c470-114">需求</span><span class="sxs-lookup"><span data-stu-id="4c470-114">Requirement</span></span> | <span data-ttu-id="4c470-115">值</span><span class="sxs-lookup"><span data-stu-id="4c470-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c470-116">版本</span><span class="sxs-lookup"><span data-stu-id="4c470-116">Version</span></span><br/> | <span data-ttu-id="4c470-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4c470-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4c470-118">Windows Vista Windows Installer 4.0 或 Windows Installer 4.5 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4c470-118">Windows Installer 4.0 or Windows Installer 4.5 or later on Windows Vista.</span></span> <span data-ttu-id="4c470-119">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="4c470-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4c470-120">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="4c470-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c470-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c470-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c470-122">屬性</span><span class="sxs-lookup"><span data-stu-id="4c470-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




