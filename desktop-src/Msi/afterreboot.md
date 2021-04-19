---
description: 當 ForceReboot 動作叫用重新開機之後，安裝程式會將 AFTERREBOOT 屬性設定為1。 安裝程式會在重新開機之後，將 AFTERREBOOT = 1 新增至命令列執行。
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: AFTERREBOOT 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990962"
---
# <a name="afterreboot-property"></a><span data-ttu-id="5d830-104">AFTERREBOOT 屬性</span><span class="sxs-lookup"><span data-stu-id="5d830-104">AFTERREBOOT property</span></span>

<span data-ttu-id="5d830-105">當 [ForceReboot 動作](forcereboot-action.md)叫用重新開機之後，安裝程式會將 **AFTERREBOOT** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="5d830-105">The installer sets the **AFTERREBOOT** property to 1 after a reboot invoked by the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="5d830-106">安裝程式會在重新開機之後，將 AFTERREBOOT = 1 新增至命令列執行。</span><span class="sxs-lookup"><span data-stu-id="5d830-106">The installer adds AFTERREBOOT=1 to the command line run immediately after the reboot.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d830-107">備註</span><span class="sxs-lookup"><span data-stu-id="5d830-107">Remarks</span></span>

<span data-ttu-id="5d830-108">[ForceReboot 動作](forcereboot-action.md)必須一律搭配條件陳述式使用，讓安裝程式只在必要時才觸發重新開機。</span><span class="sxs-lookup"><span data-stu-id="5d830-108">The [ForceReboot action](forcereboot-action.md) must always be used with a conditional statement such that the installer triggers a reboot only when necessary.</span></span> <span data-ttu-id="5d830-109">如果已取代特定檔案或已安裝特定元件，則可能需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="5d830-109">A reboot might be required if a particular file was replaced or a particular component was installed.</span></span> <span data-ttu-id="5d830-110">每項產品都有不同的案例，而且可能需要自訂動作來判斷是否需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="5d830-110">The case is different for each product and a custom action might be needed to determine whether a reboot is needed.</span></span> <span data-ttu-id="5d830-111">ForceReboot 動作的條件通常會使用 **AFTERREBOOT** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5d830-111">The condition on the ForceReboot action commonly makes use of the **AFTERREBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d830-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d830-112">Requirements</span></span>



| <span data-ttu-id="5d830-113">需求</span><span class="sxs-lookup"><span data-stu-id="5d830-113">Requirement</span></span> | <span data-ttu-id="5d830-114">值</span><span class="sxs-lookup"><span data-stu-id="5d830-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d830-115">版本</span><span class="sxs-lookup"><span data-stu-id="5d830-115">Version</span></span><br/> | <span data-ttu-id="5d830-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="5d830-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5d830-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="5d830-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5d830-118">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="5d830-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5d830-119">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d830-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d830-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d830-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d830-121">屬性</span><span class="sxs-lookup"><span data-stu-id="5d830-121">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5d830-122">系統重新開機</span><span class="sxs-lookup"><span data-stu-id="5d830-122">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




