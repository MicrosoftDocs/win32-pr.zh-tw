---
description: 表示憑證的基本條件約束延伸。
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: BasicConstraints 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981654"
---
# <a name="basicconstraints-object"></a><span data-ttu-id="615f4-103">BasicConstraints 物件</span><span class="sxs-lookup"><span data-stu-id="615f4-103">BasicConstraints object</span></span>

<span data-ttu-id="615f4-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="615f4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="615f4-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="615f4-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="615f4-106">**BasicConstraints** 物件代表憑證的基本限制延伸。</span><span class="sxs-lookup"><span data-stu-id="615f4-106">The **BasicConstraints** object represents the basic constraints extension of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="615f4-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="615f4-107">When to use</span></span>

<span data-ttu-id="615f4-108">**BasicConstraints** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="615f4-108">The **BasicConstraints** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="615f4-109">判斷基本條件約束延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="615f4-109">Determine whether the basic constraints extension is present.</span></span>
-   <span data-ttu-id="615f4-110">判斷基本條件約束延伸是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="615f4-110">Determine whether the basic constraints extension is marked critical.</span></span>
-   <span data-ttu-id="615f4-111">判斷憑證是否受限於憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="615f4-111">Determine whether the certificate is constrained to certificate authorities.</span></span>
-   <span data-ttu-id="615f4-112">判斷路徑長度條件約束是否存在，並取得路徑長度條件約束值。</span><span class="sxs-lookup"><span data-stu-id="615f4-112">Determine whether the path length constraint is present and retrieve the path length constraint value.</span></span>

## <a name="members"></a><span data-ttu-id="615f4-113">成員</span><span class="sxs-lookup"><span data-stu-id="615f4-113">Members</span></span>

<span data-ttu-id="615f4-114">**BasicConstraints** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="615f4-114">The **BasicConstraints** object has these types of members:</span></span>

-   [<span data-ttu-id="615f4-115">屬性</span><span class="sxs-lookup"><span data-stu-id="615f4-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="615f4-116">屬性</span><span class="sxs-lookup"><span data-stu-id="615f4-116">Properties</span></span>

<span data-ttu-id="615f4-117">**BasicConstraints** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="615f4-117">The **BasicConstraints** object has these properties.</span></span>



| <span data-ttu-id="615f4-118">屬性</span><span class="sxs-lookup"><span data-stu-id="615f4-118">Property</span></span>                                                                                     | <span data-ttu-id="615f4-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="615f4-119">Access type</span></span>          | <span data-ttu-id="615f4-120">Description</span><span class="sxs-lookup"><span data-stu-id="615f4-120">Description</span></span>                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="615f4-121">**IsCertificateAuthority**</span><span class="sxs-lookup"><span data-stu-id="615f4-121">**IsCertificateAuthority**</span></span>](basicconstraints-iscertificateauthority.md)<br/>         | <span data-ttu-id="615f4-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="615f4-122">Read-only</span></span><br/> | <span data-ttu-id="615f4-123">取得布林值，指出憑證是否為證書 [*頒發機構*](../secgloss/c-gly.md) 單位 (CA) 。</span><span class="sxs-lookup"><span data-stu-id="615f4-123">Retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span><br/> |
| [<span data-ttu-id="615f4-124">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="615f4-124">**IsCritical**</span></span>](basicconstraints-iscritical.md)<br/>                                 | <span data-ttu-id="615f4-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="615f4-125">Read-only</span></span><br/> | <span data-ttu-id="615f4-126">抓取布林值，指出基本條件約束延伸是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="615f4-126">Retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="615f4-127">**IsPathLenConstraintPresent**</span><span class="sxs-lookup"><span data-stu-id="615f4-127">**IsPathLenConstraintPresent**</span></span>](basicconstraints-ispathlenconstraintpresent.md)<br/> | <span data-ttu-id="615f4-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="615f4-128">Read-only</span></span><br/> | <span data-ttu-id="615f4-129">抓取布林值，指出憑證的路徑長度條件約束是否存在。</span><span class="sxs-lookup"><span data-stu-id="615f4-129">Retrieves a Boolean value that indicates whether the certificate's path length constraint is present.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="615f4-130">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="615f4-130">**IsPresent**</span></span>](basicconstraints-ispresent.md)<br/>                                   | <span data-ttu-id="615f4-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="615f4-131">Read-only</span></span><br/> | <span data-ttu-id="615f4-132">抓取布林值，這個值會指出基本條件約束延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="615f4-132">Retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="615f4-133">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="615f4-133">This is the default property.</span></span><br/>                                                                              |
| [<span data-ttu-id="615f4-134">**PathLenConstraint**</span><span class="sxs-lookup"><span data-stu-id="615f4-134">**PathLenConstraint**</span></span>](basicconstraints-pathlenconstraint.md)<br/>                   | <span data-ttu-id="615f4-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="615f4-135">Read-only</span></span><br/> | <span data-ttu-id="615f4-136">抓取路徑長度條件約束的值。</span><span class="sxs-lookup"><span data-stu-id="615f4-136">Retrieves the value of the path length constraint.</span></span><br/>                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="615f4-137">備註</span><span class="sxs-lookup"><span data-stu-id="615f4-137">Remarks</span></span>

<span data-ttu-id="615f4-138">無法建立 **BasicConstraints** 物件。</span><span class="sxs-lookup"><span data-stu-id="615f4-138">The **BasicConstraints** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="615f4-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="615f4-139">Requirements</span></span>



| <span data-ttu-id="615f4-140">需求</span><span class="sxs-lookup"><span data-stu-id="615f4-140">Requirement</span></span> | <span data-ttu-id="615f4-141">值</span><span class="sxs-lookup"><span data-stu-id="615f4-141">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="615f4-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="615f4-142">End of client support</span></span><br/> | <span data-ttu-id="615f4-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="615f4-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="615f4-144">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="615f4-144">End of server support</span></span><br/> | <span data-ttu-id="615f4-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="615f4-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="615f4-146">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="615f4-146">Redistributable</span></span><br/>       | <span data-ttu-id="615f4-147">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="615f4-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="615f4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="615f4-148">DLL</span></span><br/>                   | <dl> <span data-ttu-id="615f4-149"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="615f4-149"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="615f4-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="615f4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="615f4-151">加密物件</span><span class="sxs-lookup"><span data-stu-id="615f4-151">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
