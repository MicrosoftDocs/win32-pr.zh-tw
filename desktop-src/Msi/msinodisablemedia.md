---
description: 設定 MSINODISABLEMEDIA 屬性，以防止安裝程式設定 DISABLEMEDIA 屬性。 設定 DISABLEMEDIA 屬性可防止安裝程式將任何媒體來源（例如 CD-ROM）註冊為產品的有效來源。
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: MSINODISABLEMEDIA 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976153"
---
# <a name="msinodisablemedia-property"></a><span data-ttu-id="66600-104">MSINODISABLEMEDIA 屬性</span><span class="sxs-lookup"><span data-stu-id="66600-104">MSINODISABLEMEDIA property</span></span>

<span data-ttu-id="66600-105">設定 **MSINODISABLEMEDIA** 屬性，以防止安裝程式設定 [**DISABLEMEDIA**](-disablemedia.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="66600-105">Set the **MSINODISABLEMEDIA** property to prevent the installer from setting the [**DISABLEMEDIA**](-disablemedia.md) property.</span></span> <span data-ttu-id="66600-106">設定 **DISABLEMEDIA** 屬性可防止安裝程式將任何媒體來源（例如 cd-rom）註冊為產品的有效來源。</span><span class="sxs-lookup"><span data-stu-id="66600-106">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span>

<span data-ttu-id="66600-107">如果未設定 **MSINODISABLEMEDIA** ，安裝程式可能會在執行 [系統管理安裝](administrative-installation.md)時，將 [**DISABLEMEDIA**](-disablemedia.md)新增至系統管理屬性資料流程。</span><span class="sxs-lookup"><span data-stu-id="66600-107">When **MSINODISABLEMEDIA** is not set, the installer might add [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream when performing an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="66600-108">這可防止從系統管理映射安裝的使用者從媒體安裝，例如 CD-ROM。</span><span class="sxs-lookup"><span data-stu-id="66600-108">This prevents users who install from the administrative image from ever installing from media, such as a CD-ROM.</span></span>

-   <span data-ttu-id="66600-109">執行系統管理安裝時，如果 [[**頁面計數摘要**](page-count-summary.md)] 屬性小於150，則安裝程式只會將 [**DISABLEMEDIA**](-disablemedia.md)新增至系統管理屬性串流。</span><span class="sxs-lookup"><span data-stu-id="66600-109">When performing an administrative installation, the installer only adds [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream if the [**Page Count Summary**](page-count-summary.md) Property is less than 150.</span></span>

<span data-ttu-id="66600-110">如果 [**DISABLEMEDIA**](-disablemedia.md) 列在 [**AdminProperties**](adminproperties.md) 屬性中，則設定 **MSINODISABLEMEDIA** 會防止在系統管理安裝期間設定 **DISABLEMEDIA** 。</span><span class="sxs-lookup"><span data-stu-id="66600-110">If [**DISABLEMEDIA**](-disablemedia.md) is listed in the [**AdminProperties**](adminproperties.md) property, setting **MSINODISABLEMEDIA** prevents **DISABLEMEDIA** from being set during an administrative installation.</span></span> <span data-ttu-id="66600-111">在此情況下，安裝程式可能會註冊媒體來源，如果原始系統管理安裝映射稍後無法使用，則使用者可以選擇從媒體來源重新安裝。</span><span class="sxs-lookup"><span data-stu-id="66600-111">In this case, the installer may register a media source and a user could then have the option to reinstall from the media source if the original administrative installation image became unavailable later.</span></span>

## <a name="requirements"></a><span data-ttu-id="66600-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="66600-112">Requirements</span></span>



| <span data-ttu-id="66600-113">需求</span><span class="sxs-lookup"><span data-stu-id="66600-113">Requirement</span></span> | <span data-ttu-id="66600-114">值</span><span class="sxs-lookup"><span data-stu-id="66600-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66600-115">版本</span><span class="sxs-lookup"><span data-stu-id="66600-115">Version</span></span><br/> | <span data-ttu-id="66600-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="66600-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="66600-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="66600-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="66600-118">Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="66600-118">Windows Installer on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="66600-119">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="66600-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66600-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66600-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66600-121">屬性</span><span class="sxs-lookup"><span data-stu-id="66600-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




