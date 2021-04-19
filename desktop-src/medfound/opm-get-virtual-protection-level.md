---
description: 傳回所指定保護機制的虛擬保護層級。
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: 'OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985620"
---
# <a name="opm_get_virtual_protection_level"></a><span data-ttu-id="50384-103">OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級</span><span class="sxs-lookup"><span data-stu-id="50384-103">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="50384-104">傳回所指定保護機制的虛擬保護層級。</span><span class="sxs-lookup"><span data-stu-id="50384-104">Returns the virtual protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="50384-105">*虛擬* 保護層級是在目前的輸出保護管理員 (OPM) 會話期間，應用程式所要求的層級。</span><span class="sxs-lookup"><span data-stu-id="50384-105">The *virtual* protection level is the level requested by the application during the current Output Protection Manager (OPM) session.</span></span> <span data-ttu-id="50384-106">驅動程式可能會因為此 OPM 會話外的事件而套用較高的層級。</span><span class="sxs-lookup"><span data-stu-id="50384-106">The driver might apply a higher level, due to events outside of this OPM session.</span></span> <span data-ttu-id="50384-107">若要找出實際的保護層級，請傳送 [**OPM \_ 取得實際 \_ 的 \_ 保護 \_ 等級**](opm-get-actual-protection-level.md) 查詢。</span><span class="sxs-lookup"><span data-stu-id="50384-107">To find the actual protection level that is in effect, send the [**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**](opm-get-actual-protection-level.md) query.</span></span>



| <span data-ttu-id="50384-108">需求</span><span class="sxs-lookup"><span data-stu-id="50384-108">Requirement</span></span> | <span data-ttu-id="50384-109">值</span><span class="sxs-lookup"><span data-stu-id="50384-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50384-110">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="50384-110">Request GUID</span></span> | <span data-ttu-id="50384-111">OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級</span><span class="sxs-lookup"><span data-stu-id="50384-111">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                          |
| <span data-ttu-id="50384-112">輸入資料</span><span class="sxs-lookup"><span data-stu-id="50384-112">Input data</span></span>   | <span data-ttu-id="50384-113">要查詢的保護機制，指定為32位整數。</span><span class="sxs-lookup"><span data-stu-id="50384-113">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="50384-114">此值會被解釋為 [**OPM 保護類型旗標**](opm-protection-type-flags.md)的成員。</span><span class="sxs-lookup"><span data-stu-id="50384-114">The value is interpreted as a member of the [**OPM Protection Type Flags**](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="50384-115">傳回資料</span><span class="sxs-lookup"><span data-stu-id="50384-115">Return data</span></span>  | <span data-ttu-id="50384-116">[**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構</span><span class="sxs-lookup"><span data-stu-id="50384-116">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="50384-117">備註</span><span class="sxs-lookup"><span data-stu-id="50384-117">Remarks</span></span>

<span data-ttu-id="50384-118">保護層級會在 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員中傳回。</span><span class="sxs-lookup"><span data-stu-id="50384-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="50384-119">此值的意義取決於所查詢的保護機制。</span><span class="sxs-lookup"><span data-stu-id="50384-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="50384-120">針對每個保護機制， **ulInformation** 的值是來自不同列舉的旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="50384-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="50384-121">保護機制</span><span class="sxs-lookup"><span data-stu-id="50384-121">Protection mechanism</span></span> | <span data-ttu-id="50384-122">列舉型別</span><span class="sxs-lookup"><span data-stu-id="50384-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="50384-123">ACP</span><span class="sxs-lookup"><span data-stu-id="50384-123">ACP</span></span>                  | [<span data-ttu-id="50384-124">**OPM \_ ACP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="50384-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="50384-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="50384-125">CGMS-A</span></span>               | [<span data-ttu-id="50384-126">**CGMS-保護旗標**</span><span class="sxs-lookup"><span data-stu-id="50384-126">**CGMS-A Protection Flags**</span></span>](cgms-a-protection-flags.md)        |
| <span data-ttu-id="50384-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="50384-127">DPCP</span></span>                 | [<span data-ttu-id="50384-128">**OPM \_ DPCP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="50384-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="50384-129">觀看</span><span class="sxs-lookup"><span data-stu-id="50384-129">HDCP</span></span>                 | [<span data-ttu-id="50384-130">**OPM \_ HDCP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="50384-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="50384-131">此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryLocalProtectionLevel 查詢。</span><span class="sxs-lookup"><span data-stu-id="50384-131">This query is equivalent to the DXVA\_COPPQueryLocalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="50384-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="50384-132">Requirements</span></span>



| <span data-ttu-id="50384-133">需求</span><span class="sxs-lookup"><span data-stu-id="50384-133">Requirement</span></span> | <span data-ttu-id="50384-134">值</span><span class="sxs-lookup"><span data-stu-id="50384-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50384-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50384-135">Minimum supported client</span></span><br/> | <span data-ttu-id="50384-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50384-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="50384-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50384-137">Minimum supported server</span></span><br/> | <span data-ttu-id="50384-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50384-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="50384-139">標頭</span><span class="sxs-lookup"><span data-stu-id="50384-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="50384-140"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="50384-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50384-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50384-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50384-142">**IOPMVideoOutput：： COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="50384-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="50384-143">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="50384-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="50384-144">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="50384-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




