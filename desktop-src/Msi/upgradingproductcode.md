---
description: 當升級移除應用程式時，Windows Installer 會設定 UPGRADINGPRODUCTCODE 屬性。
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: UPGRADINGPRODUCTCODE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984064"
---
# <a name="upgradingproductcode-property"></a><span data-ttu-id="2434d-103">UPGRADINGPRODUCTCODE 屬性</span><span class="sxs-lookup"><span data-stu-id="2434d-103">UPGRADINGPRODUCTCODE property</span></span>

<span data-ttu-id="2434d-104">當升級移除應用程式時，Windows Installer 會設定 **UPGRADINGPRODUCTCODE** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2434d-104">The **UPGRADINGPRODUCTCODE** property is set by Windows Installer when an upgrade removes an application.</span></span> <span data-ttu-id="2434d-105">當安裝程式執行 [RemoveExistingProducts 動作](removeexistingproducts-action.md)時，會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="2434d-105">The installer sets this property when it runs the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="2434d-106">使用主控台中的 [新增或移除程式] 移除應用程式，就不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="2434d-106">This property is not set by removing an application using the Add or Remove Programs in Control Panel.</span></span> <span data-ttu-id="2434d-107">應用程式會藉由檢查 **UPGRADINGPRODUCTCODE**，來判斷升級或新增或移除程式是否正在移除。</span><span class="sxs-lookup"><span data-stu-id="2434d-107">An application determines whether it is being removed by an upgrade or the Add or Remove Programs by checking **UPGRADINGPRODUCTCODE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2434d-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="2434d-108">Requirements</span></span>



| <span data-ttu-id="2434d-109">需求</span><span class="sxs-lookup"><span data-stu-id="2434d-109">Requirement</span></span> | <span data-ttu-id="2434d-110">值</span><span class="sxs-lookup"><span data-stu-id="2434d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2434d-111">版本</span><span class="sxs-lookup"><span data-stu-id="2434d-111">Version</span></span><br/> | <span data-ttu-id="2434d-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="2434d-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2434d-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="2434d-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2434d-114">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="2434d-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2434d-115">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="2434d-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2434d-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2434d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2434d-117">屬性</span><span class="sxs-lookup"><span data-stu-id="2434d-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




