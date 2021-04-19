---
description: 下表中的旗標指定輸出保護管理員 (OPM) 的輸出保護機制。
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: 'OPM 保護類型旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977803"
---
# <a name="opm-protection-type-flags"></a><span data-ttu-id="d9826-103">OPM 保護類型旗標</span><span class="sxs-lookup"><span data-stu-id="d9826-103">OPM Protection Type Flags</span></span>

<span data-ttu-id="d9826-104">下表中的旗標指定輸出保護管理員 (OPM) 的輸出保護機制。</span><span class="sxs-lookup"><span data-stu-id="d9826-104">The flags in the following table specify output protection mechanisms for Output Protection Manager (OPM).</span></span>



| <span data-ttu-id="d9826-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="d9826-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d9826-106">Description</span><span class="sxs-lookup"><span data-stu-id="d9826-106">Description</span></span>                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <span data-ttu-id="d9826-107"><dt>**OPM \_保護 \_ 類型 \_ 其他**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="d9826-107"><dt>**OPM\_PROTECTION\_TYPE\_OTHER**</dt> <dt>0x80000000</dt></span></span> </dl>                                                | <span data-ttu-id="d9826-108">未知的保護機制。</span><span class="sxs-lookup"><span data-stu-id="d9826-108">Unknown protection mechanism.</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <span data-ttu-id="d9826-109"><dt>**OPM \_保護 \_ 類型 \_ NONE**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d9826-109"><dt>**OPM\_PROTECTION\_TYPE\_NONE**</dt> <dt>0x00000000</dt></span></span> </dl>                                                   | <span data-ttu-id="d9826-110">沒有防護機制。</span><span class="sxs-lookup"><span data-stu-id="d9826-110">No protection mechanisms.</span></span><br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <span data-ttu-id="d9826-111"><dt>**OPM \_保護 \_ 類型 \_ COPP \_ 相容的 \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d9826-111"><dt>**OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="d9826-112">High-Bandwidth 數位內容保護 (HDCP) 。</span><span class="sxs-lookup"><span data-stu-id="d9826-112">High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="d9826-113">當模擬經認證的輸出保護通訊協定 (COPP) 時，會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="d9826-113">This flag is used when emulating Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="d9826-114">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d9826-114">For more information, see Remarks.</span></span> <span data-ttu-id="d9826-115">OPM 語義不支援此旗標。</span><span class="sxs-lookup"><span data-stu-id="d9826-115">This flag is not supported for OPM semantics.</span></span><br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <span data-ttu-id="d9826-116"><dt>**OPM \_保護 \_ 類型 \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d9826-116"><dt>**OPM\_PROTECTION\_TYPE\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                                                      | <span data-ttu-id="d9826-117">類比禁止複製 (ACP) 。</span><span class="sxs-lookup"><span data-stu-id="d9826-117">Analog Copy Protection (ACP).</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <span data-ttu-id="d9826-118"><dt>**OPM \_保護 \_ 類型 \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="d9826-118"><dt>**OPM\_PROTECTION\_TYPE\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>                                                | <span data-ttu-id="d9826-119">複製世代管理系統—類比 (CGMS-A) 。</span><span class="sxs-lookup"><span data-stu-id="d9826-119">Copy Generation Management System—Analog (CGMS-A).</span></span><br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <span data-ttu-id="d9826-120"><dt>**OPM \_保護 \_ 類型 \_ HDCP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="d9826-120"><dt>**OPM\_PROTECTION\_TYPE\_HDCP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                   | <span data-ttu-id="d9826-121">觀看.</span><span class="sxs-lookup"><span data-stu-id="d9826-121">HDCP.</span></span> <span data-ttu-id="d9826-122">當 OPM 物件具有 OPM 語義時，會使用這個旗標。</span><span class="sxs-lookup"><span data-stu-id="d9826-122">This flag is used when the OPM object has OPM semantics.</span></span> <span data-ttu-id="d9826-123">COPP 語義不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="d9826-123">It is not supported for COPP semantics.</span></span><br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <span data-ttu-id="d9826-124"><dt>**OPM \_保護 \_ 類型 \_ DPCP**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="d9826-124"><dt>**OPM\_PROTECTION\_TYPE\_DPCP**</dt> <dt>0x00000010</dt></span></span> </dl>                                                   | <span data-ttu-id="d9826-125">DisplayPort 內容保護 (DPCP) 。</span><span class="sxs-lookup"><span data-stu-id="d9826-125">DisplayPort Content Protection (DPCP).</span></span><br/>                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="d9826-126">備註</span><span class="sxs-lookup"><span data-stu-id="d9826-126">Remarks</span></span>

<span data-ttu-id="d9826-127">下列 OPM 命令和狀態要求會使用這些旗標。</span><span class="sxs-lookup"><span data-stu-id="d9826-127">These flags are used in the following OPM commands and status requests.</span></span>

-   [<span data-ttu-id="d9826-128">OPM \_ SET \_ 保護 \_ 等級</span><span class="sxs-lookup"><span data-stu-id="d9826-128">OPM\_SET\_PROTECTION\_LEVEL</span></span>](opm-set-protection-level.md)
-   [<span data-ttu-id="d9826-129">OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級</span><span class="sxs-lookup"><span data-stu-id="d9826-129">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-virtual-protection-level.md)
-   [<span data-ttu-id="d9826-130">OPM \_ 取得 \_ 實際的 \_ 保護 \_ 層級</span><span class="sxs-lookup"><span data-stu-id="d9826-130">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-actual-protection-level.md)

### <a name="hdcp"></a><span data-ttu-id="d9826-131">觀看</span><span class="sxs-lookup"><span data-stu-id="d9826-131">HDCP</span></span>

<span data-ttu-id="d9826-132">下列兩個旗標為 HDCP 定義。</span><span class="sxs-lookup"><span data-stu-id="d9826-132">The following two flags are defined for HDCP.</span></span>



| <span data-ttu-id="d9826-133">值</span><span class="sxs-lookup"><span data-stu-id="d9826-133">Value</span></span>                                         | <span data-ttu-id="d9826-134">描述</span><span class="sxs-lookup"><span data-stu-id="d9826-134">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9826-135">OPM \_ 保護 \_ 類型 \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="d9826-135">OPM\_PROTECTION\_TYPE\_HDCP</span></span>                   | <span data-ttu-id="d9826-136">如果已使用 OPM 語義建立了 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 指標，請使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="d9826-136">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with OPM semantics.</span></span>                                                                        |
| <span data-ttu-id="d9826-137">OPM \_ 保護 \_ 類型 \_ COPP \_ 相容的 \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="d9826-137">OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP</span></span> | <span data-ttu-id="d9826-138">如果已使用 COPP 語義建立了 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 指標，請使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="d9826-138">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with COPP semantics.</span></span> <span data-ttu-id="d9826-139">此旗標對應于 \_ COPP 中的 COPP Set-protectiontype \_ HDCP 旗標。</span><span class="sxs-lookup"><span data-stu-id="d9826-139">This flag corresponds to the COPP\_ProtectionType\_HDCP flag in COPP.</span></span> |



 

<span data-ttu-id="d9826-140">這兩種模式 (OPM 語義和 COPP 語義) 支援適用于 HDCP 的下列作業：</span><span class="sxs-lookup"><span data-stu-id="d9826-140">Both modes (OPM semantics and COPP semantics) support the following operations for HDCP:</span></span>

-   <span data-ttu-id="d9826-141">使用 [OPM \_ SET \_ PROTECTION \_ LEVEL](opm-set-protection-level.md) 命令啟用或停用 HDCP。</span><span class="sxs-lookup"><span data-stu-id="d9826-141">Enable or disable HDCP by using the [OPM\_SET\_PROTECTION\_LEVEL](opm-set-protection-level.md) command.</span></span>
-   <span data-ttu-id="d9826-142">使用 [OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 等級](opm-get-virtual-protection-level.md) 或 [OPM \_ 取得 \_ 實際的 \_ 保護 \_ 等級](opm-get-actual-protection-level.md) 狀態要求，以查詢是否已啟用 HDCP。</span><span class="sxs-lookup"><span data-stu-id="d9826-142">Query whether HDCP is enabled by using the [OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL](opm-get-virtual-protection-level.md) or [OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL](opm-get-actual-protection-level.md) status request.</span></span>

<span data-ttu-id="d9826-143">OPM 語義也支援下列各項：</span><span class="sxs-lookup"><span data-stu-id="d9826-143">OPM semantics also support the following:</span></span>

-   <span data-ttu-id="d9826-144">HDCP 中繼器。</span><span class="sxs-lookup"><span data-stu-id="d9826-144">HDCP repeaters.</span></span> <span data-ttu-id="d9826-145">*Hdcp 中繼器* 是一種 hdcp 裝置，可以接收 hdcp 內容，也可以重新加密及傳輸相同的內容。</span><span class="sxs-lookup"><span data-stu-id="d9826-145">An *HDCP repeater* is an HDCP device that can receive HDCP content and also re-encrypt and transmit the same content.</span></span>
-   <span data-ttu-id="d9826-146">HDCP 撤銷。</span><span class="sxs-lookup"><span data-stu-id="d9826-146">HDCP revocation.</span></span> <span data-ttu-id="d9826-147">如果已撤銷的 HDCP 裝置已附加至 OPM video 輸出，則影片輸出不會傳輸影片。</span><span class="sxs-lookup"><span data-stu-id="d9826-147">If a revoked HDCP device is attached to the OPM video output, the video output will not transmit the video.</span></span> <span data-ttu-id="d9826-148">應用程式不需要剖析 HDCP 系統 renewability 訊息 (SRMs) 或判斷是否已撤銷輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="d9826-148">The application does not need to parse HDCP system renewability messages (SRMs) or determine whether the output device has been revoked.</span></span> <span data-ttu-id="d9826-149">如需詳細資訊，請參閱 [**OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) 命令。</span><span class="sxs-lookup"><span data-stu-id="d9826-149">For more information, see the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="d9826-150">使用 COPP 的語法時， [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 介面不支援 HDCP 中繼器。</span><span class="sxs-lookup"><span data-stu-id="d9826-150">When COPP semantics are used, the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface does not support HDCP repeaters.</span></span> <span data-ttu-id="d9826-151">此外，它也不會處理 HDCP 撤銷。</span><span class="sxs-lookup"><span data-stu-id="d9826-151">Also, it does not handle HDCP revocation.</span></span> <span data-ttu-id="d9826-152">相反地，應用程式必須剖析 SRM，以判斷是否已撤銷 HDCP 裝置。</span><span class="sxs-lookup"><span data-stu-id="d9826-152">Instead, the application must parse the SRM to determine whether an HDCP device has been revoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9826-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9826-153">Requirements</span></span>



| <span data-ttu-id="d9826-154">需求</span><span class="sxs-lookup"><span data-stu-id="d9826-154">Requirement</span></span> | <span data-ttu-id="d9826-155">值</span><span class="sxs-lookup"><span data-stu-id="d9826-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d9826-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9826-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d9826-157">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9826-157">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d9826-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9826-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d9826-159">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9826-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d9826-160">標頭</span><span class="sxs-lookup"><span data-stu-id="d9826-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9826-161"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d9826-161"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9826-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9826-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9826-163">OPM 列舉</span><span class="sxs-lookup"><span data-stu-id="d9826-163">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




