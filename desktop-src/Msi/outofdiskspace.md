---
description: 如果目前安裝的目標磁片區沒有足夠的磁碟空間可容納安裝，安裝程式會將 OutOfDiskSpace 屬性設定為 TRUE。
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: OutOfDiskSpace 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983028"
---
# <a name="outofdiskspace-property"></a><span data-ttu-id="02a97-103">OutOfDiskSpace 屬性</span><span class="sxs-lookup"><span data-stu-id="02a97-103">OutOfDiskSpace property</span></span>

<span data-ttu-id="02a97-104">如果目前安裝的目標磁片區沒有足夠的磁碟空間可容納安裝，安裝程式會將 **OutOfDiskSpace** 屬性設定為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="02a97-104">The installer sets the **OutOfDiskSpace** property to TRUE if any volume that is a target of the current installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="02a97-105">如果所有磁片區有足夠的空間，此值會是 FALSE。</span><span class="sxs-lookup"><span data-stu-id="02a97-105">If all volumes have sufficient space, the value is FALSE.</span></span> <span data-ttu-id="02a97-106">選取解決動作會使用這個值來取消安裝並產生對話方塊。</span><span class="sxs-lookup"><span data-stu-id="02a97-106">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

<span data-ttu-id="02a97-107">此屬性在 [CostFinalize 動作](costfinalize-action.md) 執行之後隨時都有效。</span><span class="sxs-lookup"><span data-stu-id="02a97-107">This property is valid at any time after the [CostFinalize action](costfinalize-action.md) is executed.</span></span> <span data-ttu-id="02a97-108">[**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)屬性狀態會在重新計算總安裝成本時動態更新 (例如，任何功能的安裝狀態透過 [選取](selection-dialog.md)對話方塊) 變更時。</span><span class="sxs-lookup"><span data-stu-id="02a97-108">The [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection](selection-dialog.md) dialog).</span></span>

## <a name="remarks"></a><span data-ttu-id="02a97-109">備註</span><span class="sxs-lookup"><span data-stu-id="02a97-109">Remarks</span></span>

<span data-ttu-id="02a97-110">任何依賴 **OutOfDiskSpace** 屬性來判斷是否要顯示對話方塊的對話方塊都必須設定對話方塊的 [TrackDiskSpace 對話方塊樣式位](trackdiskspace-dialog-style-bit.md) ，以動態更新目標磁片區上的空間。</span><span class="sxs-lookup"><span data-stu-id="02a97-110">Any dialog relying on the **OutOfDiskSpace** property to determine whether to bring up a dialog must set the [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a97-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="02a97-111">Requirements</span></span>



| <span data-ttu-id="02a97-112">需求</span><span class="sxs-lookup"><span data-stu-id="02a97-112">Requirement</span></span> | <span data-ttu-id="02a97-113">值</span><span class="sxs-lookup"><span data-stu-id="02a97-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02a97-114">版本</span><span class="sxs-lookup"><span data-stu-id="02a97-114">Version</span></span><br/> | <span data-ttu-id="02a97-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="02a97-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="02a97-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="02a97-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="02a97-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="02a97-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="02a97-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="02a97-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02a97-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02a97-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02a97-120">屬性</span><span class="sxs-lookup"><span data-stu-id="02a97-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




