---
description: 在屬性資料表或命令列中，將 MSIUNINSTALLSUPERSEDEDCOMPONENTS 屬性設定為1。
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: MSIUNINSTALLSUPERSEDEDCOMPONENTS 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979508"
---
# <a name="msiuninstallsupersededcomponents-property"></a><span data-ttu-id="ab104-103">MSIUNINSTALLSUPERSEDEDCOMPONENTS 屬性</span><span class="sxs-lookup"><span data-stu-id="ab104-103">MSIUNINSTALLSUPERSEDEDCOMPONENTS property</span></span>

<span data-ttu-id="ab104-104">在 [屬性資料表](property-table.md)或命令列中，將 **MSIUNINSTALLSUPERSEDEDCOMPONENTS** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="ab104-104">Set the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** property to 1 in the [Property table](property-table.md) or on a command line.</span></span> <span data-ttu-id="ab104-105">當這個屬性設定為1時，安裝程式會判斷是否有任何已取代修補程式中的元件變成多餘的。</span><span class="sxs-lookup"><span data-stu-id="ab104-105">When this property has been set to 1, the installer determines whether the components in any superseded patches are becoming redundant.</span></span> <span data-ttu-id="ab104-106">安裝程式可以取消註冊並卸載多餘的元件，以防止在電腦上留下孤立的元件。</span><span class="sxs-lookup"><span data-stu-id="ab104-106">The installer can unregister and uninstall redundant components to prevent leaving behind orphan components on the computer.</span></span>

<span data-ttu-id="ab104-107">設定此屬性會影響所有修補程式中所取代的元件。</span><span class="sxs-lookup"><span data-stu-id="ab104-107">Setting this property affects the components in all patches being superseded.</span></span> <span data-ttu-id="ab104-108">若要為單一元件啟用這項功能，請使用 [元件資料表](component-table.md)中的 **msidbComponentAttributesUninstallOnSupersedence** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ab104-108">To enable this functionality for single components, use the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md).</span></span>

<span data-ttu-id="ab104-109">**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="ab104-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="ab104-110">早于 Windows Installer 4.5 的版本會忽略 **MSIUNINSTALLSUPERSEDEDCOMPONENTS** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ab104-110">Versions earlier than Windows Installer 4.5 ignore the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** Property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab104-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab104-111">Requirements</span></span>



| <span data-ttu-id="ab104-112">需求</span><span class="sxs-lookup"><span data-stu-id="ab104-112">Requirement</span></span> | <span data-ttu-id="ab104-113">值</span><span class="sxs-lookup"><span data-stu-id="ab104-113">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab104-114">版本</span><span class="sxs-lookup"><span data-stu-id="ab104-114">Version</span></span><br/> | <span data-ttu-id="ab104-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ab104-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ab104-116">Windows Vista、Windows XP、Windows Server 2003 和 Windows Server 2008 上的 Windows Installer 4.5 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ab104-116">Windows Installer 4.5 or Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="ab104-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="ab104-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab104-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab104-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab104-119">屬性</span><span class="sxs-lookup"><span data-stu-id="ab104-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




