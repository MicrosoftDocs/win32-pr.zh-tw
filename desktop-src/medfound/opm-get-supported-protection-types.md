---
description: 傳回連接器所支援的保護機制清單。
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: 'OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943729"
---
# <a name="opm_get_supported_protection_types"></a><span data-ttu-id="853e7-103">OPM \_ 取得 \_ 支援的 \_ 保護 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="853e7-103">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>

<span data-ttu-id="853e7-104">傳回連接器所支援的保護機制清單。</span><span class="sxs-lookup"><span data-stu-id="853e7-104">Returns the list of protection mechanisms that are supported by the connector.</span></span>



| <span data-ttu-id="853e7-105">需求</span><span class="sxs-lookup"><span data-stu-id="853e7-105">Requirement</span></span> | <span data-ttu-id="853e7-106">值</span><span class="sxs-lookup"><span data-stu-id="853e7-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="853e7-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="853e7-107">Request GUID</span></span> | <span data-ttu-id="853e7-108">OPM \_ 取得 \_ 支援的 \_ 保護 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="853e7-108">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>                                      |
| <span data-ttu-id="853e7-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="853e7-109">Input data</span></span>   | <span data-ttu-id="853e7-110">無</span><span class="sxs-lookup"><span data-stu-id="853e7-110">None</span></span>                                                                        |
| <span data-ttu-id="853e7-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="853e7-111">Return data</span></span>  | <span data-ttu-id="853e7-112">[**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構</span><span class="sxs-lookup"><span data-stu-id="853e7-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="853e7-113">備註</span><span class="sxs-lookup"><span data-stu-id="853e7-113">Remarks</span></span>

<span data-ttu-id="853e7-114">保護機制會以 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員傳回。</span><span class="sxs-lookup"><span data-stu-id="853e7-114">The protection mechanisms are returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="853e7-115">值是 [OPM 保護類型旗標](opm-protection-type-flags.md)的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="853e7-115">The value is a bitwise **OR** of [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span>

<span data-ttu-id="853e7-116">此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryProtectionType 查詢。</span><span class="sxs-lookup"><span data-stu-id="853e7-116">This query is equivalent to the DXVA\_COPPQueryProtectionType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="853e7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="853e7-117">Requirements</span></span>



| <span data-ttu-id="853e7-118">需求</span><span class="sxs-lookup"><span data-stu-id="853e7-118">Requirement</span></span> | <span data-ttu-id="853e7-119">值</span><span class="sxs-lookup"><span data-stu-id="853e7-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="853e7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="853e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="853e7-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="853e7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="853e7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="853e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="853e7-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="853e7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="853e7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="853e7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="853e7-125"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="853e7-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="853e7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="853e7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="853e7-127">**IOPMVideoOutput：： COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="853e7-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="853e7-128">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="853e7-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="853e7-129">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="853e7-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




