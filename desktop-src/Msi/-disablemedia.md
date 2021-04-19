---
description: 設定 DISABLEMEDIA 屬性可防止安裝程式將任何媒體來源（例如 CD-ROM）註冊為產品的有效來源。 但是，如果已啟用流覽，使用者仍可流覽至媒體來源。
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: DISABLEMEDIA 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994071"
---
# <a name="disablemedia-property"></a><span data-ttu-id="69f33-104">DISABLEMEDIA 屬性</span><span class="sxs-lookup"><span data-stu-id="69f33-104">DISABLEMEDIA property</span></span>

<span data-ttu-id="69f33-105">設定 [**DISABLEMEDIA**](disablemedia.md) 屬性可防止安裝程式將任何媒體來源（例如 cd-rom）註冊為產品的有效來源。</span><span class="sxs-lookup"><span data-stu-id="69f33-105">Setting the [**DISABLEMEDIA**](disablemedia.md) property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="69f33-106">但是，如果已啟用流覽，使用者仍可流覽至媒體來源。</span><span class="sxs-lookup"><span data-stu-id="69f33-106">If browsing is enabled, however, a user may still browse to a media source.</span></span>

## <a name="remarks"></a><span data-ttu-id="69f33-107">備註</span><span class="sxs-lookup"><span data-stu-id="69f33-107">Remarks</span></span>

<span data-ttu-id="69f33-108">請注意， [**DISABLEMEDIA**](disablemedia.md) 屬性與設定 DISABLEMEDIA 原則的效果不同。</span><span class="sxs-lookup"><span data-stu-id="69f33-108">Note that the [**DISABLEMEDIA**](disablemedia.md) property has a different effect than setting the DisableMedia policy.</span></span> <span data-ttu-id="69f33-109">設定 **DISABLEMEDIA** 可防止註冊任何媒體來源，這也會防止第一次從媒體來源安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="69f33-109">Setting **DISABLEMEDIA** prevents the registration of any media source, and this also prevents the first time installation of an application from a media sources.</span></span>

<span data-ttu-id="69f33-110">如需保護 [*受管理應用程式*](m-gly.md) 的媒體來源以避免由非系統管理使用者進行流覽和安裝的詳細資訊，請參閱 [來源復原](source-resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="69f33-110">For details about securing the media sources of [*managed application*](m-gly.md) against browsing and installation by non-administrative users, see [Source Resiliency](source-resiliency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69f33-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="69f33-111">Requirements</span></span>



| <span data-ttu-id="69f33-112">需求</span><span class="sxs-lookup"><span data-stu-id="69f33-112">Requirement</span></span> | <span data-ttu-id="69f33-113">值</span><span class="sxs-lookup"><span data-stu-id="69f33-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f33-114">版本</span><span class="sxs-lookup"><span data-stu-id="69f33-114">Version</span></span><br/> | <span data-ttu-id="69f33-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="69f33-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="69f33-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="69f33-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="69f33-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="69f33-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="69f33-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="69f33-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69f33-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69f33-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f33-120">屬性</span><span class="sxs-lookup"><span data-stu-id="69f33-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




