---
description: 傳回影片輸出所使用的 i/o 匯流排型別。
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: 'OPM_GET_ADAPTER_BUS_TYPE (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982298"
---
# <a name="opm_get_adapter_bus_type"></a><span data-ttu-id="3e170-103">OPM \_ 取得 \_ 介面卡 \_ 匯流排 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="3e170-103">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>

<span data-ttu-id="3e170-104">傳回影片輸出所使用的 i/o 匯流排型別。</span><span class="sxs-lookup"><span data-stu-id="3e170-104">Returns the type of I/O bus used by the video output.</span></span>



| <span data-ttu-id="3e170-105">需求</span><span class="sxs-lookup"><span data-stu-id="3e170-105">Requirement</span></span> | <span data-ttu-id="3e170-106">值</span><span class="sxs-lookup"><span data-stu-id="3e170-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="3e170-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="3e170-107">Request GUID</span></span> | <span data-ttu-id="3e170-108">OPM \_ 取得 \_ 介面卡 \_ 匯流排 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="3e170-108">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>                                                |
| <span data-ttu-id="3e170-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="3e170-109">Input data</span></span>   | <span data-ttu-id="3e170-110">無</span><span class="sxs-lookup"><span data-stu-id="3e170-110">None</span></span>                                                                        |
| <span data-ttu-id="3e170-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="3e170-111">Return data</span></span>  | <span data-ttu-id="3e170-112">[**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構</span><span class="sxs-lookup"><span data-stu-id="3e170-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3e170-113">備註</span><span class="sxs-lookup"><span data-stu-id="3e170-113">Remarks</span></span>

<span data-ttu-id="3e170-114">匯流排類型會以 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員傳回。</span><span class="sxs-lookup"><span data-stu-id="3e170-114">The bus type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="3e170-115">值是 [**OPM 匯流排類型旗標**](opm-bus-type-flags.md)的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="3e170-115">The value is a bitwise **OR** of [**OPM Bus Type Flags**](opm-bus-type-flags.md).</span></span>

<span data-ttu-id="3e170-116">此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryBusData 查詢。</span><span class="sxs-lookup"><span data-stu-id="3e170-116">This query is equivalent to the DXVA\_COPPQueryBusData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e170-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e170-117">Requirements</span></span>



| <span data-ttu-id="3e170-118">需求</span><span class="sxs-lookup"><span data-stu-id="3e170-118">Requirement</span></span> | <span data-ttu-id="3e170-119">值</span><span class="sxs-lookup"><span data-stu-id="3e170-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3e170-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e170-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e170-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e170-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3e170-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e170-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e170-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e170-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3e170-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3e170-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e170-125"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e170-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e170-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e170-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e170-127">**IOPMVideoOutput：： COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="3e170-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="3e170-128">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="3e170-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="3e170-129">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="3e170-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




