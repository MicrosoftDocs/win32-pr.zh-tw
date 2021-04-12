---
description: 傳回透過連接器傳輸之視訊訊號的描述。
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: 'OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318744"
---
# <a name="opm_get_actual_output_format"></a><span data-ttu-id="72c57-103">OPM \_ 取得 \_ 實際 \_ 輸出 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="72c57-103">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>

<span data-ttu-id="72c57-104">傳回透過連接器傳輸之視訊訊號的描述。</span><span class="sxs-lookup"><span data-stu-id="72c57-104">Returns a description of the video signal that is being transmitted over the connector.</span></span>



| <span data-ttu-id="72c57-105">需求</span><span class="sxs-lookup"><span data-stu-id="72c57-105">Requirement</span></span> | <span data-ttu-id="72c57-106">值</span><span class="sxs-lookup"><span data-stu-id="72c57-106">Value</span></span> |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="72c57-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="72c57-107">Request GUID</span></span> | <span data-ttu-id="72c57-108">OPM \_ 取得 \_ 實際 \_ 輸出 \_ 格式</span><span class="sxs-lookup"><span data-stu-id="72c57-108">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>                                             |
| <span data-ttu-id="72c57-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="72c57-109">Input data</span></span>   | <span data-ttu-id="72c57-110">無</span><span class="sxs-lookup"><span data-stu-id="72c57-110">None</span></span>                                                                         |
| <span data-ttu-id="72c57-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="72c57-111">Return data</span></span>  | <span data-ttu-id="72c57-112">[**OPM \_ 實際 \_ 輸出 \_ 格式**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)結構</span><span class="sxs-lookup"><span data-stu-id="72c57-112">An [**OPM\_ACTUAL\_OUTPUT\_FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="72c57-113">備註</span><span class="sxs-lookup"><span data-stu-id="72c57-113">Remarks</span></span>

<span data-ttu-id="72c57-114">透過連接器傳送的視訊訊號不一定會與桌面顯示模式具有相同的格式。</span><span class="sxs-lookup"><span data-stu-id="72c57-114">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="72c57-115">例如，桌面顯示模式可能是 1024 x 768 圖元（85 Hz），而連接器可能是以 720 x 480 圖元為單位傳輸視訊訊號的 S-video 連接器，60/1.01 Hz。</span><span class="sxs-lookup"><span data-stu-id="72c57-115">For example, the desktop display mode might be 1024 x 768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720 x 480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="72c57-116">在此情況下，驅動程式會傳回 S-video 信號的解析度，而不是電腦解析度。</span><span class="sxs-lookup"><span data-stu-id="72c57-116">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

<span data-ttu-id="72c57-117">此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryDisplayData 查詢。</span><span class="sxs-lookup"><span data-stu-id="72c57-117">This query is equivalent to the DXVA\_COPPQueryDisplayData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="72c57-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="72c57-118">Requirements</span></span>



| <span data-ttu-id="72c57-119">需求</span><span class="sxs-lookup"><span data-stu-id="72c57-119">Requirement</span></span> | <span data-ttu-id="72c57-120">值</span><span class="sxs-lookup"><span data-stu-id="72c57-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="72c57-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72c57-121">Minimum supported client</span></span><br/> | <span data-ttu-id="72c57-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72c57-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="72c57-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72c57-123">Minimum supported server</span></span><br/> | <span data-ttu-id="72c57-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72c57-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="72c57-125">標頭</span><span class="sxs-lookup"><span data-stu-id="72c57-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="72c57-126"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="72c57-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72c57-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72c57-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c57-128">**IOPMVideoOutput：： COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="72c57-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="72c57-129">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="72c57-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="72c57-130">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="72c57-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




