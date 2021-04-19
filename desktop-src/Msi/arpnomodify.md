---
description: 設定 ARPNOMODIFY 屬性會在修改產品的主控台中停用 [新增或移除程式] 功能。
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: ARPNOMODIFY 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984061"
---
# <a name="arpnomodify-property"></a><span data-ttu-id="850bc-103">ARPNOMODIFY 屬性</span><span class="sxs-lookup"><span data-stu-id="850bc-103">ARPNOMODIFY property</span></span>

<span data-ttu-id="850bc-104">設定 **ARPNOMODIFY** 屬性會在修改產品的主控台中停用 [新增或移除程式] 功能。</span><span class="sxs-lookup"><span data-stu-id="850bc-104">Setting the **ARPNOMODIFY** property disables Add or Remove Programs functionality in Control Panel that modifies the product.</span></span> <span data-ttu-id="850bc-105">針對 Windows 2000，這會在 **主控台** 的 [**新增或移除程式**] 中停用產品的 [**修改**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="850bc-105">For Windows 2000, this disables the **Modify** button for the product in **Add or Remove Programs** in **Control Panel**.</span></span> <span data-ttu-id="850bc-106">在舊版作業系統上，按一下 [ **新增或移除程式** ] 按鈕會卸載產品，而不是輸入維護模式的 wizard。</span><span class="sxs-lookup"><span data-stu-id="850bc-106">On earlier operating systems, clicking the **Add or Remove Programs** button uninstalls the product rather than entering the maintenance mode wizard.</span></span>

<span data-ttu-id="850bc-107">如果已設定 **ARPNOMODIFY** 屬性， [RegisterProduct 動作](registerproduct-action.md) 會在登錄機碼下寫入 "NoModify" 值：</span><span class="sxs-lookup"><span data-stu-id="850bc-107">If the **ARPNOMODIFY** property is set, the [RegisterProduct action](registerproduct-action.md) writes the value "NoModify" under the registry key:</span></span>

<span data-ttu-id="850bc-108">**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**卸載** \\ **{*產品金鑰*}**</span><span class="sxs-lookup"><span data-stu-id="850bc-108">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\ **{*product key*}**</span></span>

<span data-ttu-id="850bc-109">如果已設定 **ARPNOMODIFY** 屬性，而且未設定 [**ARPNOREMOVE**](arpnoremove.md) 屬性，則 RegisterProduct 動作也會在此機碼下寫入 UninstallString 值。</span><span class="sxs-lookup"><span data-stu-id="850bc-109">If the **ARPNOMODIFY** property is set and the [**ARPNOREMOVE**](arpnoremove.md) property is not set, the RegisterProduct action also writes the UninstallString value under this key.</span></span> <span data-ttu-id="850bc-110">UnistallString 值是用來移除產品的命令列，而不是重新設定產品。</span><span class="sxs-lookup"><span data-stu-id="850bc-110">The UnistallString value is a command line for removing the product, rather than reconfiguring the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="850bc-111">備註</span><span class="sxs-lookup"><span data-stu-id="850bc-111">Remarks</span></span>

<span data-ttu-id="850bc-112">在 Windows 2000 上，這會在 **主控台** 的 [**新增或移除程式**] 中停用產品的 [**變更**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="850bc-112">On Windows 2000, this disables the **Change** button for the product in the **Add or Remove Programs** of the **Control Panel**.</span></span>

<span data-ttu-id="850bc-113">這個屬性可以透過自訂轉換來設定，以防止使用者透過 [ **新增或移除程式**] 來變更系統管理員的自訂。</span><span class="sxs-lookup"><span data-stu-id="850bc-113">This property can be set by a customization transform to prevent users from changing an administrator's customization through **Add or Remove Programs**.</span></span> <span data-ttu-id="850bc-114">這個屬性只會影響 [ **新增或移除程式**]。</span><span class="sxs-lookup"><span data-stu-id="850bc-114">This property only affects **Add or Remove Programs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="850bc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="850bc-115">Requirements</span></span>



| <span data-ttu-id="850bc-116">需求</span><span class="sxs-lookup"><span data-stu-id="850bc-116">Requirement</span></span> | <span data-ttu-id="850bc-117">值</span><span class="sxs-lookup"><span data-stu-id="850bc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="850bc-118">版本</span><span class="sxs-lookup"><span data-stu-id="850bc-118">Version</span></span><br/> | <span data-ttu-id="850bc-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="850bc-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="850bc-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="850bc-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="850bc-121">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="850bc-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="850bc-122">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="850bc-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="850bc-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="850bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="850bc-124">屬性</span><span class="sxs-lookup"><span data-stu-id="850bc-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="850bc-125">自訂轉換範例</span><span class="sxs-lookup"><span data-stu-id="850bc-125">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> </dl>

 

 




