---
description: 傳回所指定保護機制的全域保護層級。
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: 'OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026391"
---
# <a name="opm_get_actual_protection_level"></a><span data-ttu-id="20eed-103">OPM \_ 取得 \_ 實際的 \_ 保護 \_ 層級</span><span class="sxs-lookup"><span data-stu-id="20eed-103">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="20eed-104">傳回所指定保護機制的全域保護層級。</span><span class="sxs-lookup"><span data-stu-id="20eed-104">Returns the global protection level for a specified protection mechanism.</span></span>



| <span data-ttu-id="20eed-105">需求</span><span class="sxs-lookup"><span data-stu-id="20eed-105">Requirement</span></span> | <span data-ttu-id="20eed-106">值</span><span class="sxs-lookup"><span data-stu-id="20eed-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20eed-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="20eed-107">Request GUID</span></span> | <span data-ttu-id="20eed-108">OPM \_ 取得 \_ 實際的 \_ 保護 \_ 層級</span><span class="sxs-lookup"><span data-stu-id="20eed-108">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                       |
| <span data-ttu-id="20eed-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="20eed-109">Input data</span></span>   | <span data-ttu-id="20eed-110">要查詢的保護機制，指定為32位整數。</span><span class="sxs-lookup"><span data-stu-id="20eed-110">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="20eed-111">此值會被解釋為 [OPM 保護類型旗標](opm-protection-type-flags.md)的成員。</span><span class="sxs-lookup"><span data-stu-id="20eed-111">The value is interpreted as a member of the [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="20eed-112">傳回資料</span><span class="sxs-lookup"><span data-stu-id="20eed-112">Return data</span></span>  | <span data-ttu-id="20eed-113">[**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構</span><span class="sxs-lookup"><span data-stu-id="20eed-113">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="20eed-114">備註</span><span class="sxs-lookup"><span data-stu-id="20eed-114">Remarks</span></span>

<span data-ttu-id="20eed-115">全域保護層級是目前正在連接器上套用的保護層級，而不管圖形驅動程式如何指示套用保護。</span><span class="sxs-lookup"><span data-stu-id="20eed-115">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="20eed-116">例如，應用程式可以藉由呼叫 **ChangeDisplaySettingsEx** 函數來設定 ACP 保護層級。</span><span class="sxs-lookup"><span data-stu-id="20eed-116">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="20eed-117">在此情況下，全域保護層級會反映這項設定，即使未透過輸出保護管理員要求 (OPM) 也一樣。</span><span class="sxs-lookup"><span data-stu-id="20eed-117">In that case, the global protection level would reflect this setting, even though it was not requested through Output Protection Manager (OPM).</span></span>

<span data-ttu-id="20eed-118">保護層級會在 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員中傳回。</span><span class="sxs-lookup"><span data-stu-id="20eed-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="20eed-119">此值的意義取決於所查詢的保護機制。</span><span class="sxs-lookup"><span data-stu-id="20eed-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="20eed-120">針對每個保護機制， **ulInformation** 的值是來自不同列舉的旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="20eed-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="20eed-121">保護機制</span><span class="sxs-lookup"><span data-stu-id="20eed-121">Protection mechanism</span></span> | <span data-ttu-id="20eed-122">列舉型別</span><span class="sxs-lookup"><span data-stu-id="20eed-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="20eed-123">ACP</span><span class="sxs-lookup"><span data-stu-id="20eed-123">ACP</span></span>                  | [<span data-ttu-id="20eed-124">**OPM \_ ACP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="20eed-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="20eed-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="20eed-125">CGMS-A</span></span>               | [<span data-ttu-id="20eed-126">CGMS-保護旗標</span><span class="sxs-lookup"><span data-stu-id="20eed-126">CGMS-A Protection Flags</span></span>](cgms-a-protection-flags.md)            |
| <span data-ttu-id="20eed-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="20eed-127">DPCP</span></span>                 | [<span data-ttu-id="20eed-128">**OPM \_ DPCP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="20eed-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="20eed-129">觀看</span><span class="sxs-lookup"><span data-stu-id="20eed-129">HDCP</span></span>                 | [<span data-ttu-id="20eed-130">**OPM \_ HDCP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="20eed-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="20eed-131">此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryGlobalProtectionLevel 查詢。</span><span class="sxs-lookup"><span data-stu-id="20eed-131">This query is equivalent to the DXVA\_COPPQueryGlobalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="20eed-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="20eed-132">Requirements</span></span>



| <span data-ttu-id="20eed-133">需求</span><span class="sxs-lookup"><span data-stu-id="20eed-133">Requirement</span></span> | <span data-ttu-id="20eed-134">值</span><span class="sxs-lookup"><span data-stu-id="20eed-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="20eed-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20eed-135">Minimum supported client</span></span><br/> | <span data-ttu-id="20eed-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20eed-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="20eed-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20eed-137">Minimum supported server</span></span><br/> | <span data-ttu-id="20eed-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20eed-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="20eed-139">標頭</span><span class="sxs-lookup"><span data-stu-id="20eed-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="20eed-140"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="20eed-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20eed-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20eed-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20eed-142">**IOPMVideoOutput：： COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="20eed-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="20eed-143">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="20eed-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="20eed-144">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="20eed-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




