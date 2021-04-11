---
description: COPP 查詢參考
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: COPP 查詢參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025793"
---
# <a name="copp-query-reference"></a><span data-ttu-id="ccf0e-103">COPP 查詢參考</span><span class="sxs-lookup"><span data-stu-id="ccf0e-103">COPP Query Reference</span></span>

<span data-ttu-id="ccf0e-104">本節說明經認證的輸出保護通訊協定所支援的狀態查詢 (COPP) 。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-104">This section describes the status queries that are supported by Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="ccf0e-105">針對每個查詢，會列出用來定義查詢的 GUID，以及輸入資料和傳回資料。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-105">For each query, the GUID that defines the query is listed, along with the input data and return data.</span></span>



| <span data-ttu-id="ccf0e-106">查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-106">Query</span></span>                   | <span data-ttu-id="ccf0e-107">GUID</span><span class="sxs-lookup"><span data-stu-id="ccf0e-107">GUID</span></span>                                     |
|-------------------------|------------------------------------------|
| <span data-ttu-id="ccf0e-108">匯流排資料</span><span class="sxs-lookup"><span data-stu-id="ccf0e-108">Bus Data</span></span>                | <span data-ttu-id="ccf0e-109">**DXVA \_ COPPQueryBusData**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-109">**DXVA\_COPPQueryBusData**</span></span>               |
| <span data-ttu-id="ccf0e-110">連接器類型</span><span class="sxs-lookup"><span data-stu-id="ccf0e-110">Connector Type</span></span>          | <span data-ttu-id="ccf0e-111">**DXVA \_ COPPQueryConnectorType**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-111">**DXVA\_COPPQueryConnectorType**</span></span>         |
| <span data-ttu-id="ccf0e-112">顯示資料</span><span class="sxs-lookup"><span data-stu-id="ccf0e-112">Display Data</span></span>            | <span data-ttu-id="ccf0e-113">**DXVA \_ COPPQueryDisplayData**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-113">**DXVA\_COPPQueryDisplayData**</span></span>           |
| <span data-ttu-id="ccf0e-114">HDCP 金鑰資料</span><span class="sxs-lookup"><span data-stu-id="ccf0e-114">HDCP Key Data</span></span>           | <span data-ttu-id="ccf0e-115">**DXVA \_ COPPQueryHDCPKeyData**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-115">**DXVA\_COPPQueryHDCPKeyData**</span></span>           |
| <span data-ttu-id="ccf0e-116">全域保護等級</span><span class="sxs-lookup"><span data-stu-id="ccf0e-116">Global Protection Level</span></span> | <span data-ttu-id="ccf0e-117">**DXVA \_ COPPQueryGlobalProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-117">**DXVA\_COPPQueryGlobalProtectionLevel**</span></span> |
| <span data-ttu-id="ccf0e-118">本機保護層級</span><span class="sxs-lookup"><span data-stu-id="ccf0e-118">Local Protection Level</span></span>  | <span data-ttu-id="ccf0e-119">**DXVA \_ COPPQueryLocalProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-119">**DXVA\_COPPQueryLocalProtectionLevel**</span></span>  |
| <span data-ttu-id="ccf0e-120">保護類型</span><span class="sxs-lookup"><span data-stu-id="ccf0e-120">Protection Type</span></span>         | <span data-ttu-id="ccf0e-121">**DXVA \_ COPPQueryProtectionType**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-121">**DXVA\_COPPQueryProtectionType**</span></span>        |
| <span data-ttu-id="ccf0e-122">Signaling</span><span class="sxs-lookup"><span data-stu-id="ccf0e-122">Signaling</span></span>               | <span data-ttu-id="ccf0e-123">**DXVA \_ COPPQuerySignaling**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-123">**DXVA\_COPPQuerySignaling**</span></span>             |



 

<span data-ttu-id="ccf0e-124">匯流排資料查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-124">Bus Data Query</span></span>

<span data-ttu-id="ccf0e-125">傳回圖形介面卡所使用的 i/o 匯流排型別。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-125">Returns the type of I/O bus used by the graphics adapter.</span></span>

-   <span data-ttu-id="ccf0e-126">**GUID**： DXVA \_ COPPQueryBusData</span><span class="sxs-lookup"><span data-stu-id="ccf0e-126">**GUID**: DXVA\_COPPQueryBusData</span></span>
-   <span data-ttu-id="ccf0e-127">**輸入資料**：無。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-127">**Input data**: None.</span></span>
-   <span data-ttu-id="ccf0e-128">傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-128">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="ccf0e-129">匯流排類型會以 **dwData** 成員的旗標形式傳回，作為 [**COPP \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) 列舉的旗標。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-129">The bus type is returned in the **dwData** member as a flag from the [**COPP\_BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) enumeration.</span></span>

<span data-ttu-id="ccf0e-130">連接器類型查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-130">Connector Type Query</span></span>

<span data-ttu-id="ccf0e-131">傳回實體接點型別。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-131">Returns the physical connector type.</span></span>

-   <span data-ttu-id="ccf0e-132">**GUID**： DXVA \_ COPPQueryConnectorType</span><span class="sxs-lookup"><span data-stu-id="ccf0e-132">**GUID**: DXVA\_COPPQueryConnectorType</span></span>
-   <span data-ttu-id="ccf0e-133">**輸入資料**：無。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-133">**Input data**: None.</span></span>
-   <span data-ttu-id="ccf0e-134">傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-134">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="ccf0e-135">連接器類型會以 **dwData** 成員中的旗標形式傳回，以做為 [**COPP \_ ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) 列舉的旗標。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-135">The connector type is returned in the **dwData** member as a flag from the [**COPP\_ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) enumeration.</span></span>

<span data-ttu-id="ccf0e-136">顯示資料查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-136">Display Data Query</span></span>

<span data-ttu-id="ccf0e-137">傳回透過連接器傳輸之視訊訊號的描述。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-137">Returns a description of the video signal that is being transmitted over the connector.</span></span>

<span data-ttu-id="ccf0e-138">透過連接器傳送的視訊訊號不一定會與桌面顯示模式具有相同的格式。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-138">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="ccf0e-139">例如，桌面顯示器模式可能是 85 Hz 的1024x768 圖元，而連接器可能是以720x480 圖元為單位傳輸視訊訊號的 S-video 連接器，60/1.01 Hz 交錯。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-139">For example, the desktop display mode might be 1024x768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720x480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="ccf0e-140">在此情況下，驅動程式會傳回 S-video 信號的解析度，而不是電腦解析度。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-140">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

-   <span data-ttu-id="ccf0e-141">**GUID**： DXVA \_ COPPQueryDisplayData</span><span class="sxs-lookup"><span data-stu-id="ccf0e-141">**GUID**: DXVA\_COPPQueryDisplayData</span></span>
-   <span data-ttu-id="ccf0e-142">**輸入資料**：無。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-142">**Input data**: None.</span></span>
-   <span data-ttu-id="ccf0e-143">傳回 **資料**：傳回 [**DXVA \_ COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata)結構。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-143">**Return data**: Returns a [**DXVA\_COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) structure.</span></span>

<span data-ttu-id="ccf0e-144">HDCP 索引鍵資料查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-144">HDCP Key Data Query</span></span>

<span data-ttu-id="ccf0e-145">傳回裝置的 HDCP 金鑰選取向量 (B-KSV) 。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-145">Returns the device's HDCP key selection vector (B-KSV).</span></span>

<span data-ttu-id="ccf0e-146">KSV 是提供給裝置製造商的識別碼，用於 HDCP 驗證和設定程式。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-146">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="ccf0e-147">應用程式應該針對已撤銷的 KSVs 清單來檢查此值。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-147">The application should check this value against the list of revoked KSVs.</span></span> <span data-ttu-id="ccf0e-148">取得 KSV 撤銷清單的機制超出 COPP 通訊協定的範圍。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-148">The mechanism for obtaining the KSV revocation list is outside the scope of the COPP protocol.</span></span> <span data-ttu-id="ccf0e-149">如需詳細資訊，請參閱 HDCP 規格。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-149">For more information, consult the HDCP specification.</span></span>

<span data-ttu-id="ccf0e-150">此查詢也會判斷連線的 HDCP 裝置是監視器還是 HDCP 中繼器。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-150">This query also determines whether the connected HDCP device is a monitor or an HDCP repeater.</span></span> <span data-ttu-id="ccf0e-151">如果 HDCP 裝置為 HDCP 中繼器，應用程式不應該播放受保護的內容，因為 COPP 不支援這些功能。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-151">The application should not play protected content if the HDCP device is an HDCP repeater, because these are not supported by COPP.</span></span>

-   <span data-ttu-id="ccf0e-152">**GUID**： DXVA \_ COPPQueryHDCPKeyData</span><span class="sxs-lookup"><span data-stu-id="ccf0e-152">**GUID**: DXVA\_COPPQueryHDCPKeyData</span></span>
-   <span data-ttu-id="ccf0e-153">**輸入資料**：無。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-153">**Input data**: None.</span></span>
-   <span data-ttu-id="ccf0e-154">傳回 **資料**：傳回 [**DXVA \_ COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata)結構。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-154">**Return data**: Returns a [**DXVA\_COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) structure.</span></span>

<span data-ttu-id="ccf0e-155">全域保護等級查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-155">Global Protection Level Query</span></span>

<span data-ttu-id="ccf0e-156">傳回所指定保護機制的全域保護層級。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-156">Returns the global protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="ccf0e-157">全域保護層級是目前正在連接器上套用的保護層級，而不管圖形驅動程式如何指示套用保護。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-157">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="ccf0e-158">例如，應用程式可以藉由呼叫 **ChangeDisplaySettingsEx** 函數來設定 ACP 保護層級。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-158">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="ccf0e-159">在這種情況下，全域保護層級會反映這項設定，即使不是透過 COPP 來要求也是一樣。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-159">In that case, the global protection level would reflect this setting, even though it was not requested through COPP.</span></span>

-   <span data-ttu-id="ccf0e-160">**GUID**： DXVA \_ COPPQueryGlobalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="ccf0e-160">**GUID**: DXVA\_COPPQueryGlobalProtectionLevel</span></span>
-   <span data-ttu-id="ccf0e-161">**輸入資料**：要查詢的保護機制，指定為32位整數。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-161">**Input data**: The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="ccf0e-162">請參閱 [COPP 保護類型旗標](copp-protection-type-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-162">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="ccf0e-163">傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-163">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="ccf0e-164">目前的保護層級會在 **dwData** 成員中傳回。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-164">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="ccf0e-165">此值的意義取決於所查詢的保護機制。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-165">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="ccf0e-166">針對每個保護機制， **dwData** 成員的值是來自不同列舉的旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-166">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="ccf0e-167">保護機制</span><span class="sxs-lookup"><span data-stu-id="ccf0e-167">Protection mechanism</span></span> | <span data-ttu-id="ccf0e-168">列舉型別</span><span class="sxs-lookup"><span data-stu-id="ccf0e-168">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="ccf0e-169">ACP</span><span class="sxs-lookup"><span data-stu-id="ccf0e-169">ACP</span></span>                  | [<span data-ttu-id="ccf0e-170">**COPP \_ ACP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-170">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="ccf0e-171">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="ccf0e-171">CGMS-A</span></span>               | [<span data-ttu-id="ccf0e-172">**COPP \_ CGMSA \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-172">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="ccf0e-173">觀看</span><span class="sxs-lookup"><span data-stu-id="ccf0e-173">HDCP</span></span>                 | [<span data-ttu-id="ccf0e-174">**COPP \_ HDCP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-174">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="ccf0e-175">本機保護等級查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-175">Local Protection Level Query</span></span>

<span data-ttu-id="ccf0e-176">傳回所指定保護機制的本機保護層級。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-176">Returns the local protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="ccf0e-177">本機保護層級是透過目前的 COPP 會話所要求的保護層級。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-177">The local protection level is the protection level that was requested through the current COPP session.</span></span> <span data-ttu-id="ccf0e-178">驅動程式可能會設定較高的保護層級。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-178">The driver might set a higher protection level.</span></span>

-   <span data-ttu-id="ccf0e-179">**GUID**： DXVA \_ COPPQueryLocalProtectionLevel</span><span class="sxs-lookup"><span data-stu-id="ccf0e-179">**GUID**: DXVA\_COPPQueryLocalProtectionLevel</span></span>
-   <span data-ttu-id="ccf0e-180">**輸入資料**：要查詢的保護機制，以32位整數來進行查詢。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-180">**Input data**: The protection mechanism to query, as a 32-bit integer.</span></span> <span data-ttu-id="ccf0e-181">請參閱 [COPP 保護類型旗標](copp-protection-type-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-181">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="ccf0e-182">傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-182">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="ccf0e-183">目前的保護層級會在 **dwData** 成員中傳回。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-183">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="ccf0e-184">此值的意義取決於所查詢的保護機制。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-184">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="ccf0e-185">針對每個保護機制， **dwData** 成員的值是來自不同列舉的旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-185">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="ccf0e-186">保護機制</span><span class="sxs-lookup"><span data-stu-id="ccf0e-186">Protection mechanism</span></span> | <span data-ttu-id="ccf0e-187">列舉型別</span><span class="sxs-lookup"><span data-stu-id="ccf0e-187">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="ccf0e-188">ACP</span><span class="sxs-lookup"><span data-stu-id="ccf0e-188">ACP</span></span>                  | [<span data-ttu-id="ccf0e-189">**COPP \_ ACP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-189">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="ccf0e-190">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="ccf0e-190">CGMS-A</span></span>               | [<span data-ttu-id="ccf0e-191">**COPP \_ CGMSA \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-191">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="ccf0e-192">觀看</span><span class="sxs-lookup"><span data-stu-id="ccf0e-192">HDCP</span></span>                 | [<span data-ttu-id="ccf0e-193">**COPP \_ HDCP \_ 保護 \_ 等級**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-193">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="ccf0e-194">保護類型查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-194">Protection Type Query</span></span>

<span data-ttu-id="ccf0e-195">傳回連接器可用的保護機制。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-195">Returns the protection mechanisms that are available for the connector.</span></span>

-   <span data-ttu-id="ccf0e-196">**GUID**： DXVA \_ COPPQueryProtectionType</span><span class="sxs-lookup"><span data-stu-id="ccf0e-196">**GUID**: DXVA\_COPPQueryProtectionType</span></span>
-   <span data-ttu-id="ccf0e-197">**輸入資料**：無。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-197">**Input data**: None.</span></span>
-   <span data-ttu-id="ccf0e-198">傳回 **資料**：傳回 [**DXVA \_ COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata)結構。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-198">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="ccf0e-199">保護機制會以零或多個旗標的組合傳回 **dwData** 成員。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-199">The protection mechanisms are returned in the **dwData** member as a combination of zero or more flags.</span></span> <span data-ttu-id="ccf0e-200">請參閱 [COPP 保護類型旗標](copp-protection-type-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-200">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span> <span data-ttu-id="ccf0e-201">如果有一個以上的保護機制可用，旗標就會與位 **or** 合併。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-201">If more than one protection mechanism is available, the flags are combined with a bitwise **OR**.</span></span>

<span data-ttu-id="ccf0e-202">發出信號查詢</span><span class="sxs-lookup"><span data-stu-id="ccf0e-202">Signaling Query</span></span>

<span data-ttu-id="ccf0e-203">傳回驅動程式支援的所有保護標準的清單、目前作用中的標準，以及目前的外觀比例或其他信號資料。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-203">Returns a list of all the protection standards that are supported by the driver, the standard that is currently active, and the current aspect ratio or other signaling data.</span></span>

-   <span data-ttu-id="ccf0e-204">**GUID**： DXVA \_ COPPQuerySignaling</span><span class="sxs-lookup"><span data-stu-id="ccf0e-204">**GUID**: DXVA\_COPPQuerySignaling</span></span>
-   <span data-ttu-id="ccf0e-205">**輸入資料**：無。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-205">**Input data**: None.</span></span>
-   <span data-ttu-id="ccf0e-206">傳回 **資料**：傳回 [**DXVA \_ COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata)結構。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-206">**Return data**: Returns a [**DXVA\_COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccf0e-207">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccf0e-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccf0e-208">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="ccf0e-208">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



