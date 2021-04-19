---
description: 傳回目前影片輸出所使用 (SRM) 的系統 renewability 訊息版本號碼。
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: 'OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969245"
---
# <a name="opm_get_current_hdcp_srm_version"></a><span data-ttu-id="fc920-103">OPM \_ 取得 \_ 目前的 \_ HDCP \_ SRM \_ 版本</span><span class="sxs-lookup"><span data-stu-id="fc920-103">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>

<span data-ttu-id="fc920-104">傳回目前影片輸出所使用 (SRM) 的系統 renewability 訊息版本號碼。</span><span class="sxs-lookup"><span data-stu-id="fc920-104">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>



| <span data-ttu-id="fc920-105">需求</span><span class="sxs-lookup"><span data-stu-id="fc920-105">Requirement</span></span> | <span data-ttu-id="fc920-106">值</span><span class="sxs-lookup"><span data-stu-id="fc920-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="fc920-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="fc920-107">Request GUID</span></span> | <span data-ttu-id="fc920-108">OPM \_ 取得 \_ 目前的 \_ HDCP \_ SRM \_ 版本</span><span class="sxs-lookup"><span data-stu-id="fc920-108">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>                                       |
| <span data-ttu-id="fc920-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="fc920-109">Input data</span></span>   | <span data-ttu-id="fc920-110">無</span><span class="sxs-lookup"><span data-stu-id="fc920-110">None</span></span>                                                                        |
| <span data-ttu-id="fc920-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="fc920-111">Return data</span></span>  | <span data-ttu-id="fc920-112">[**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構</span><span class="sxs-lookup"><span data-stu-id="fc920-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fc920-113">備註</span><span class="sxs-lookup"><span data-stu-id="fc920-113">Remarks</span></span>

<span data-ttu-id="fc920-114">如果此查詢成功， [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員會包含 SRM 版本號碼（以位元組由小到大格式）。</span><span class="sxs-lookup"><span data-stu-id="fc920-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains the SRM version number, in little-endian format.</span></span>

<span data-ttu-id="fc920-115">SRMs 可用來更新已撤銷 High-Bandwidth 數位內容保護 (HDCP) 裝置的清單。</span><span class="sxs-lookup"><span data-stu-id="fc920-115">SRMs are used to update the list of revoked High-Bandwidth Digital Content Protection (HDCP) devices.</span></span> <span data-ttu-id="fc920-116">SRMs 是以影片內容提供。</span><span class="sxs-lookup"><span data-stu-id="fc920-116">SRMs are delivered with the video content.</span></span> <span data-ttu-id="fc920-117">若要設定 SRM，請傳送 [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="fc920-117">To set the SRM, send the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="fc920-118">此查詢可能會導致 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) 方法傳回下列任何錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fc920-118">This query can cause the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method to return any of the following error codes.</span></span>



| <span data-ttu-id="fc920-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fc920-119">Return code</span></span>                                            | <span data-ttu-id="fc920-120">Description</span><span class="sxs-lookup"><span data-stu-id="fc920-120">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="fc920-121">錯誤 \_ 圖形 \_ OPM \_ \_ \_ 尚未設定 HDCP \_ SRM</span><span class="sxs-lookup"><span data-stu-id="fc920-121">ERROR\_GRAPHICS\_OPM\_HDCP\_SRM\_NEVER\_SET</span></span>            | <span data-ttu-id="fc920-122">應用程式未設定 SRM。</span><span class="sxs-lookup"><span data-stu-id="fc920-122">The application did not set an SRM.</span></span>     |
| <span data-ttu-id="fc920-123">錯誤 \_ 圖形 \_ OPM \_ 輸出 \_ 不 \_ \_ 支援 \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="fc920-123">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="fc920-124">影片輸出不支援 HDCP。</span><span class="sxs-lookup"><span data-stu-id="fc920-124">The video output does not support HDCP.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="fc920-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc920-125">Requirements</span></span>



| <span data-ttu-id="fc920-126">需求</span><span class="sxs-lookup"><span data-stu-id="fc920-126">Requirement</span></span> | <span data-ttu-id="fc920-127">值</span><span class="sxs-lookup"><span data-stu-id="fc920-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fc920-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc920-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fc920-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc920-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fc920-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc920-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fc920-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc920-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fc920-132">標頭</span><span class="sxs-lookup"><span data-stu-id="fc920-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc920-133"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc920-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc920-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc920-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc920-135">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="fc920-135">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="fc920-136">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="fc920-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




