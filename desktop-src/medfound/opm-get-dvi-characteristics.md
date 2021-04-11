---
description: 查詢數位視訊介面 (DVI) 連接器是否支援 DVI 1.1 版或更新版本。
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: 'OPM_GET_DVI_CHARACTERISTICS (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026389"
---
# <a name="opm_get_dvi_characteristics"></a><span data-ttu-id="514cd-103">OPM \_ 取得 \_ DVI \_ 特性</span><span class="sxs-lookup"><span data-stu-id="514cd-103">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>

<span data-ttu-id="514cd-104">查詢數位視訊介面 (DVI) 連接器是否支援 DVI 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="514cd-104">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>



| <span data-ttu-id="514cd-105">需求</span><span class="sxs-lookup"><span data-stu-id="514cd-105">Requirement</span></span> | <span data-ttu-id="514cd-106">值</span><span class="sxs-lookup"><span data-stu-id="514cd-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="514cd-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="514cd-107">Request GUID</span></span> | <span data-ttu-id="514cd-108">OPM \_ 取得 \_ DVI \_ 特性</span><span class="sxs-lookup"><span data-stu-id="514cd-108">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>                                              |
| <span data-ttu-id="514cd-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="514cd-109">Input data</span></span>   | <span data-ttu-id="514cd-110">無</span><span class="sxs-lookup"><span data-stu-id="514cd-110">None</span></span>                                                                        |
| <span data-ttu-id="514cd-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="514cd-111">Return data</span></span>  | <span data-ttu-id="514cd-112">[**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構</span><span class="sxs-lookup"><span data-stu-id="514cd-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="514cd-113">備註</span><span class="sxs-lookup"><span data-stu-id="514cd-113">Remarks</span></span>

<span data-ttu-id="514cd-114">如果此查詢成功， [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員就會包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="514cd-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains one of the following values.</span></span>



| <span data-ttu-id="514cd-115">值</span><span class="sxs-lookup"><span data-stu-id="514cd-115">Value</span></span>                                     | <span data-ttu-id="514cd-116">描述</span><span class="sxs-lookup"><span data-stu-id="514cd-116">Description</span></span>               |
|-------------------------------------------|---------------------------|
| <span data-ttu-id="514cd-117">OPM \_ DVI \_ 特性 \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="514cd-117">OPM\_DVI\_CHARACTERISTIC\_1\_0</span></span>            | <span data-ttu-id="514cd-118">DVI 1.0 版。</span><span class="sxs-lookup"><span data-stu-id="514cd-118">DVI version 1.0.</span></span>          |
| <span data-ttu-id="514cd-119">OPM \_ DVI \_ 特性 \_ 1 \_ 1 \_ 或 \_ 更新版本</span><span class="sxs-lookup"><span data-stu-id="514cd-119">OPM\_DVI\_CHARACTERISTIC\_1\_1\_OR\_ABOVE</span></span> | <span data-ttu-id="514cd-120">DVI 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="514cd-120">DVI version 1.1 or later.</span></span> |



 

<span data-ttu-id="514cd-121">只有當實體連接器類型是 OPM 連接器類型的 DVI 時，才支援此查詢 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="514cd-121">This query is supported only when the physical connector type is OPM\_CONNECTOR\_TYPE\_DVI.</span></span> <span data-ttu-id="514cd-122">若要取得連接器類型，請傳送 [**OPM \_ get \_ connector \_ 型**](opm-get-connector-type.md) 別查詢。</span><span class="sxs-lookup"><span data-stu-id="514cd-122">To get the connector type, send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) query.</span></span>

## <a name="requirements"></a><span data-ttu-id="514cd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="514cd-123">Requirements</span></span>



| <span data-ttu-id="514cd-124">需求</span><span class="sxs-lookup"><span data-stu-id="514cd-124">Requirement</span></span> | <span data-ttu-id="514cd-125">值</span><span class="sxs-lookup"><span data-stu-id="514cd-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="514cd-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="514cd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="514cd-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="514cd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="514cd-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="514cd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="514cd-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="514cd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="514cd-130">標頭</span><span class="sxs-lookup"><span data-stu-id="514cd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="514cd-131"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="514cd-131"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="514cd-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="514cd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514cd-133">**IOPMVideoOutput：： GetInformation**</span><span class="sxs-lookup"><span data-stu-id="514cd-133">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="514cd-134">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="514cd-134">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




