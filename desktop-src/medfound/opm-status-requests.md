---
description: OPM 狀態要求
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: OPM 狀態要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691635"
---
# <a name="opm-status-requests"></a><span data-ttu-id="8c8a6-103">OPM 狀態要求</span><span class="sxs-lookup"><span data-stu-id="8c8a6-103">OPM Status Requests</span></span>

<span data-ttu-id="8c8a6-104">本節列出 [輸出保護管理員](output-protection-manager.md) (OPM) 可用的狀態要求。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="8c8a6-105">若要傳送 OPM 狀態要求，請呼叫 [**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="8c8a6-106">針對每個要求，會列出下列資訊。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-106">For each request, the following information is listed.</span></span>



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8a6-107">要求 GUID</span><span class="sxs-lookup"><span data-stu-id="8c8a6-107">Request GUID</span></span> | <span data-ttu-id="8c8a6-108">識別要求。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-108">Identifies the request.</span></span> <span data-ttu-id="8c8a6-109">將 [**OPM \_ GET \_ INFO \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)結構的 **guidSetting** 成員設定為等於此值。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-109">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="8c8a6-110">輸入資料</span><span class="sxs-lookup"><span data-stu-id="8c8a6-110">Input data</span></span>   | <span data-ttu-id="8c8a6-111">指定如何解讀 [**OPM \_ 取得 \_ 資訊 \_ 參數**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)結構中的 **abParameters** 陣列。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-111">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="8c8a6-112">輸出資料</span><span class="sxs-lookup"><span data-stu-id="8c8a6-112">Output data</span></span>  | <span data-ttu-id="8c8a6-113">指定如何在 [**OPM 所 \_ 要求的 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)結構中解讀 **abRequestedInformation** 陣列。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-113">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="8c8a6-114">系統會定義下列狀態要求：</span><span class="sxs-lookup"><span data-stu-id="8c8a6-114">The following status requests are defined:</span></span>



| <span data-ttu-id="8c8a6-115">狀態要求</span><span class="sxs-lookup"><span data-stu-id="8c8a6-115">Status request</span></span>                                                                                      | <span data-ttu-id="8c8a6-116">Description</span><span class="sxs-lookup"><span data-stu-id="8c8a6-116">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c8a6-117">**OPM \_ 取得 \_ ACP \_ 和 \_ CGMSA \_ 信號**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-117">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="8c8a6-118">傳回關於影片輸出的下列資訊：</span><span class="sxs-lookup"><span data-stu-id="8c8a6-118">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="8c8a6-119">**OPM \_ 取得 \_ 實際 \_ 輸出 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-119">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="8c8a6-120">傳回透過連接器傳輸之視訊訊號的描述。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-120">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="8c8a6-121">**OPM \_ 取得 \_ 實際的 \_ 保護 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-121">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="8c8a6-122">傳回所指定保護機制的全域保護層級。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-122">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="8c8a6-123">**OPM \_ 取得 \_ 介面卡 \_ 匯流排 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-123">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="8c8a6-124">傳回影片輸出所使用的 i/o 匯流排型別。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-124">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="8c8a6-125">**OPM \_ 取得 \_ 編解碼器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-125">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="8c8a6-126">取得硬體編解碼器的業績值。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-126">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="8c8a6-127">**OPM \_ 取得 \_ 已連線的 \_ HDCP \_ 裝置 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-127">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="8c8a6-128">取得連接至影片輸出 High-Bandwidth 數位內容保護 (HDCP) 裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-128">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="8c8a6-129">會傳回下列資訊：</span><span class="sxs-lookup"><span data-stu-id="8c8a6-129">The following information is returned:</span></span> |
| [<span data-ttu-id="8c8a6-130">**OPM \_ 取得 \_ 連接器 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-130">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="8c8a6-131">傳回影片輸出的實體接點類型。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-131">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="8c8a6-132">**OPM \_ 取得 \_ 目前的 \_ HDCP \_ SRM \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-132">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="8c8a6-133">傳回目前影片輸出所使用 (SRM) 的系統 renewability 訊息版本號碼。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-133">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="8c8a6-134">**OPM \_ 取得 \_ DVI \_ 特性**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-134">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="8c8a6-135">查詢數位視訊介面 (DVI) 連接器是否支援 DVI 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-135">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="8c8a6-136">**OPM \_ 取得 \_ 輸出 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-136">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="8c8a6-137">傳回與此影片輸出相關聯之監視的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-137">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="8c8a6-138">**OPM \_ 取得 \_ 支援的 \_ 保護 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-138">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="8c8a6-139">傳回連接器所支援的保護機制清單。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-139">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="8c8a6-140">**OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="8c8a6-140">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="8c8a6-141">傳回所指定保護機制的虛擬保護層級。</span><span class="sxs-lookup"><span data-stu-id="8c8a6-141">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="8c8a6-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c8a6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c8a6-143">OPM 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="8c8a6-143">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="8c8a6-144">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="8c8a6-144">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



