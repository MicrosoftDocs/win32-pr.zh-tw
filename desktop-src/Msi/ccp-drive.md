---
description: '[CCP \_ 磁片磁碟機] 屬性會設定為 RMCCPSearch 所要搜尋之抽取式磁碟區的根路徑。'
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: CCP_DRIVE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998788"
---
# <a name="ccp_drive-property"></a><span data-ttu-id="6514d-103">CCP \_ 磁片磁碟機屬性</span><span class="sxs-lookup"><span data-stu-id="6514d-103">CCP\_DRIVE property</span></span>

<span data-ttu-id="6514d-104">[ **CCP \_ 磁片磁碟機** ] 屬性會設定為 [RMCCPSearch](rmccpsearch-action.md)所要搜尋之抽取式磁碟區的根路徑。</span><span class="sxs-lookup"><span data-stu-id="6514d-104">The **CCP\_DRIVE** property is set to the root path of the removable volume that is to be searched by [RMCCPSearch](rmccpsearch-action.md).</span></span> <span data-ttu-id="6514d-105">RMCCPSearch 動作會使用檔案簽章來驗證合格產品是否已安裝在系統上，然後再執行升級安裝。</span><span class="sxs-lookup"><span data-stu-id="6514d-105">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before performing an upgrade installation.</span></span>

<span data-ttu-id="6514d-106">通常會透過使用者介面或自訂動作來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="6514d-106">This property is typically set via the user interface or a custom action.</span></span> <span data-ttu-id="6514d-107">在執行 [RMCCPSearch](rmccpsearch-action.md) 動作之前，應該先設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="6514d-107">This property should be set before the [RMCCPSearch](rmccpsearch-action.md) action is run.</span></span>

## <a name="requirements"></a><span data-ttu-id="6514d-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="6514d-108">Requirements</span></span>



| <span data-ttu-id="6514d-109">需求</span><span class="sxs-lookup"><span data-stu-id="6514d-109">Requirement</span></span> | <span data-ttu-id="6514d-110">值</span><span class="sxs-lookup"><span data-stu-id="6514d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6514d-111">版本</span><span class="sxs-lookup"><span data-stu-id="6514d-111">Version</span></span><br/> | <span data-ttu-id="6514d-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="6514d-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6514d-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="6514d-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6514d-114">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="6514d-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6514d-115">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="6514d-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6514d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6514d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6514d-117">屬性</span><span class="sxs-lookup"><span data-stu-id="6514d-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




