---
description: 傳回影片輸出的實體接點類型。
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: 'OPM_GET_CONNECTOR_TYPE (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191771"
---
# <a name="opm_get_connector_type"></a><span data-ttu-id="6e7e8-103">OPM \_ 取得 \_ 連接器 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6e7e8-103">OPM\_GET\_CONNECTOR\_TYPE</span></span>

<span data-ttu-id="6e7e8-104">傳回影片輸出的實體接點類型。</span><span class="sxs-lookup"><span data-stu-id="6e7e8-104">Returns the physical connector type of the video output.</span></span>



| <span data-ttu-id="6e7e8-105">需求</span><span class="sxs-lookup"><span data-stu-id="6e7e8-105">Requirement</span></span> | <span data-ttu-id="6e7e8-106">值</span><span class="sxs-lookup"><span data-stu-id="6e7e8-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6e7e8-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="6e7e8-107">Request GUID</span></span> | <span data-ttu-id="6e7e8-108">OPM \_ 取得 \_ 連接器 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6e7e8-108">OPM\_GET\_CONNECTOR\_TYPE</span></span>                                                   |
| <span data-ttu-id="6e7e8-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="6e7e8-109">Input data</span></span>   | <span data-ttu-id="6e7e8-110">無</span><span class="sxs-lookup"><span data-stu-id="6e7e8-110">None</span></span>                                                                        |
| <span data-ttu-id="6e7e8-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="6e7e8-111">Return data</span></span>  | <span data-ttu-id="6e7e8-112">[**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構</span><span class="sxs-lookup"><span data-stu-id="6e7e8-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6e7e8-113">備註</span><span class="sxs-lookup"><span data-stu-id="6e7e8-113">Remarks</span></span>

<span data-ttu-id="6e7e8-114">連接器類型會以 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員傳回。</span><span class="sxs-lookup"><span data-stu-id="6e7e8-114">The connector type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="6e7e8-115">**UlInformation** 的值等於 [**OPM 連接器類型旗標**](opm-connector-type-flags.md)中列出的其中一個連接器類型。</span><span class="sxs-lookup"><span data-stu-id="6e7e8-115">The value of **ulInformation** is equal to one of the connector types listed in [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="6e7e8-116">在 COPP 模擬模式中，連接器類型可能會與 **OPM \_ COPP 相容的 \_ \_ 連接器 \_ 類型 \_ 內部** 旗標合併。</span><span class="sxs-lookup"><span data-stu-id="6e7e8-116">In COPP emulation mode, the connector type might be combined with the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="6e7e8-117">使用位 **and** 來將連接器型別解壓縮：</span><span class="sxs-lookup"><span data-stu-id="6e7e8-117">Use a bitwise **AND** to extract the connector type:</span></span>

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

<span data-ttu-id="6e7e8-118">應用程式應該忽略 **OPM \_ COPP \_ 相容的 \_ 連接器 \_ 類型 \_ 內部** 旗標。</span><span class="sxs-lookup"><span data-stu-id="6e7e8-118">Applications should ignore the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="6e7e8-119">如需詳細資訊，請參閱 [**OPM 連接器類型旗標**](opm-connector-type-flags.md)的備註一節。</span><span class="sxs-lookup"><span data-stu-id="6e7e8-119">For more information, see the Remarks section of [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="6e7e8-120">此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryConnectorType 查詢。</span><span class="sxs-lookup"><span data-stu-id="6e7e8-120">This query is equivalent to the DXVA\_COPPQueryConnectorType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7e8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e7e8-121">Requirements</span></span>



| <span data-ttu-id="6e7e8-122">需求</span><span class="sxs-lookup"><span data-stu-id="6e7e8-122">Requirement</span></span> | <span data-ttu-id="6e7e8-123">值</span><span class="sxs-lookup"><span data-stu-id="6e7e8-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7e8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e7e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e7e8-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e7e8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6e7e8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e7e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e7e8-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e7e8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6e7e8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6e7e8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e7e8-129"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e7e8-129"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e7e8-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e7e8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7e8-131">**IOPMVideoOutput：： COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="6e7e8-131">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="6e7e8-132">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="6e7e8-132">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="6e7e8-133">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="6e7e8-133">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




