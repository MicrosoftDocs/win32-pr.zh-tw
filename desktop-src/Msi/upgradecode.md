---
description: UpgradeCode 屬性是 GUID，代表一組相關的產品。 UpgradeCode 可用於升級資料表中，以搜尋已安裝之產品的相關版本。RegisterProduct 動作會使用這個屬性。
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: UpgradeCode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977718"
---
# <a name="upgradecode-property"></a><span data-ttu-id="613e2-104">UpgradeCode 屬性</span><span class="sxs-lookup"><span data-stu-id="613e2-104">UpgradeCode property</span></span>

<span data-ttu-id="613e2-105">**UpgradeCode** 屬性是 GUID，代表一組相關的產品。</span><span class="sxs-lookup"><span data-stu-id="613e2-105">The **UpgradeCode** property is a GUID representing a related set of products.</span></span> <span data-ttu-id="613e2-106">**UpgradeCode** 可用於 [升級資料表](upgrade-table.md)中，以搜尋已安裝之產品的相關版本。</span><span class="sxs-lookup"><span data-stu-id="613e2-106">The **UpgradeCode** is used in the [Upgrade Table](upgrade-table.md) to search for related versions of the product that are already installed.</span></span>

<span data-ttu-id="613e2-107">[RegisterProduct 動作](registerproduct-action.md)會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="613e2-107">This property is used by the [RegisterProduct action](registerproduct-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="613e2-108">備註</span><span class="sxs-lookup"><span data-stu-id="613e2-108">Remarks</span></span>

<span data-ttu-id="613e2-109">強烈建議安裝套件的作者為其應用程式指定 **UpgradeCode** 。</span><span class="sxs-lookup"><span data-stu-id="613e2-109">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span>

## <a name="requirements"></a><span data-ttu-id="613e2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="613e2-110">Requirements</span></span>



| <span data-ttu-id="613e2-111">需求</span><span class="sxs-lookup"><span data-stu-id="613e2-111">Requirement</span></span> | <span data-ttu-id="613e2-112">值</span><span class="sxs-lookup"><span data-stu-id="613e2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613e2-113">版本</span><span class="sxs-lookup"><span data-stu-id="613e2-113">Version</span></span><br/> | <span data-ttu-id="613e2-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="613e2-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="613e2-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="613e2-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="613e2-116">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="613e2-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="613e2-117">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="613e2-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="613e2-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="613e2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="613e2-119">屬性</span><span class="sxs-lookup"><span data-stu-id="613e2-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="613e2-120">修補和升級</span><span class="sxs-lookup"><span data-stu-id="613e2-120">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="613e2-121">準備應用程式以進行未來的主要升級</span><span class="sxs-lookup"><span data-stu-id="613e2-121">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




