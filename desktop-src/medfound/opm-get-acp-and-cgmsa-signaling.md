---
description: 深入瞭解： OPM_GET_ACP_AND_CGMSA_SIGNALING
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: 'OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978843"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a><span data-ttu-id="b19b7-103">OPM \_ 取得 \_ ACP \_ 和 \_ CGMSA \_ 信號</span><span class="sxs-lookup"><span data-stu-id="b19b7-103">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="b19b7-104">傳回關於影片輸出的下列資訊：</span><span class="sxs-lookup"><span data-stu-id="b19b7-104">Returns the following information about a video output:</span></span>

-   <span data-ttu-id="b19b7-105">驅動程式支援的電視保護標準清單。</span><span class="sxs-lookup"><span data-stu-id="b19b7-105">A list of television protection standards supported by the driver.</span></span>
-   <span data-ttu-id="b19b7-106">目前作用中的標準。</span><span class="sxs-lookup"><span data-stu-id="b19b7-106">The standard that is currently active.</span></span>
-   <span data-ttu-id="b19b7-107">目前的外觀比例或其他信號資料。</span><span class="sxs-lookup"><span data-stu-id="b19b7-107">The current aspect ratio or other signaling data.</span></span>



| <span data-ttu-id="b19b7-108">需求</span><span class="sxs-lookup"><span data-stu-id="b19b7-108">Requirement</span></span> | <span data-ttu-id="b19b7-109">值</span><span class="sxs-lookup"><span data-stu-id="b19b7-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b19b7-110">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="b19b7-110">Request GUID</span></span> | <span data-ttu-id="b19b7-111">OPM \_ 取得 \_ ACP \_ 和 \_ CGMSA \_ 信號</span><span class="sxs-lookup"><span data-stu-id="b19b7-111">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                |
| <span data-ttu-id="b19b7-112">輸入資料</span><span class="sxs-lookup"><span data-stu-id="b19b7-112">Input data</span></span>   | <span data-ttu-id="b19b7-113">無</span><span class="sxs-lookup"><span data-stu-id="b19b7-113">None</span></span>                                                                                |
| <span data-ttu-id="b19b7-114">傳回資料</span><span class="sxs-lookup"><span data-stu-id="b19b7-114">Return data</span></span>  | <span data-ttu-id="b19b7-115">[**OPM \_ ACP \_ 和 \_ CGMSA \_ 信號**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)結構</span><span class="sxs-lookup"><span data-stu-id="b19b7-115">An [**OPM\_ACP\_AND\_CGMSA\_SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b19b7-116">備註</span><span class="sxs-lookup"><span data-stu-id="b19b7-116">Remarks</span></span>

<span data-ttu-id="b19b7-117">此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQuerySignaling 查詢。</span><span class="sxs-lookup"><span data-stu-id="b19b7-117">This query is equivalent to the DXVA\_COPPQuerySignaling query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="b19b7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b19b7-118">Requirements</span></span>



| <span data-ttu-id="b19b7-119">需求</span><span class="sxs-lookup"><span data-stu-id="b19b7-119">Requirement</span></span> | <span data-ttu-id="b19b7-120">值</span><span class="sxs-lookup"><span data-stu-id="b19b7-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b19b7-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b19b7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b19b7-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b19b7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b19b7-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b19b7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b19b7-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b19b7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b19b7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b19b7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b19b7-126"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b19b7-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b19b7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b19b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b19b7-128">**IOPMVideoOutput：： COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="b19b7-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="b19b7-129">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="b19b7-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="b19b7-130">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="b19b7-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




