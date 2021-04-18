---
description: 將 TRANSFORMSSECURE 屬性設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: TRANSFORMSSECURE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976253"
---
# <a name="transformssecure-property"></a><span data-ttu-id="e6085-103">TRANSFORMSSECURE 屬性</span><span class="sxs-lookup"><span data-stu-id="e6085-103">TRANSFORMSSECURE property</span></span>

<span data-ttu-id="e6085-104">將 **TRANSFORMSSECURE** 屬性設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。</span><span class="sxs-lookup"><span data-stu-id="e6085-104">Setting the **TRANSFORMSSECURE** property to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="e6085-105">設定此屬性就像是設定 [TransformsSecure 原則](transformssecure-policy.md) ，但範圍不同。</span><span class="sxs-lookup"><span data-stu-id="e6085-105">Setting this property is like setting the [TransformsSecure policy](transformssecure-policy.md) except that the scope is different.</span></span> <span data-ttu-id="e6085-106">設定 TransformsSecure 原則會套用至指定使用者所安裝的所有套件。</span><span class="sxs-lookup"><span data-stu-id="e6085-106">Setting TransformsSecure policy applies to all packages installed by a given user.</span></span> <span data-ttu-id="e6085-107">無論使用者是哪一種，設定 **TRANSFORMSSECURE** 屬性都會套用至封裝。</span><span class="sxs-lookup"><span data-stu-id="e6085-107">Setting the **TRANSFORMSSECURE** property applies to the package regardless of the user.</span></span>

<span data-ttu-id="e6085-108">這個屬性的目的是要為安全轉換儲存提供 Windows 2000 的旅遊使用者。</span><span class="sxs-lookup"><span data-stu-id="e6085-108">The purpose of this property is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="e6085-109">設定這個屬性時， [維護安裝](maintenance-installation.md) 只能從指定的路徑使用轉換。</span><span class="sxs-lookup"><span data-stu-id="e6085-109">When this property is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the specified path.</span></span> <span data-ttu-id="e6085-110">如果路徑無法使用，維護安裝將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e6085-110">If the path is not available the maintenance installation fails.</span></span> <span data-ttu-id="e6085-111">因此，每個安全轉換的來源都必須位於安裝套件來源的位置。</span><span class="sxs-lookup"><span data-stu-id="e6085-111">A source for each secure transform must therefore reside at the location of the source of the installation package.</span></span> <span data-ttu-id="e6085-112">然後，如果安裝程式發現本機電腦上缺少轉換，就可以從這個來源還原轉換。</span><span class="sxs-lookup"><span data-stu-id="e6085-112">Then if the installer finds that the transform is missing on the local computer, it can restore the transform from this source.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6085-113">備註</span><span class="sxs-lookup"><span data-stu-id="e6085-113">Remarks</span></span>

<span data-ttu-id="e6085-114">Windows Installer 會將 [**TRANSFORMSATSOURCE**](transformsatsource.md) 屬性解釋為與 **TRANSFORMSSECURE** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="e6085-114">Windows Installer interprets the [**TRANSFORMSATSOURCE**](transformsatsource.md) property to be the same as the **TRANSFORMSSECURE** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6085-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6085-115">Requirements</span></span>



| <span data-ttu-id="e6085-116">需求</span><span class="sxs-lookup"><span data-stu-id="e6085-116">Requirement</span></span> | <span data-ttu-id="e6085-117">值</span><span class="sxs-lookup"><span data-stu-id="e6085-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6085-118">版本</span><span class="sxs-lookup"><span data-stu-id="e6085-118">Version</span></span><br/> | <span data-ttu-id="e6085-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e6085-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6085-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e6085-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6085-121">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="e6085-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e6085-122">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="e6085-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6085-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6085-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6085-124">屬性</span><span class="sxs-lookup"><span data-stu-id="e6085-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="e6085-125">資料庫轉換</span><span class="sxs-lookup"><span data-stu-id="e6085-125">Database Transforms</span></span>](database-transforms.md)
</dt> </dl>

 

 




