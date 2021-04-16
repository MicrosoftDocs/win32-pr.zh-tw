---
description: 下表中的旗標會指定輸出保護管理員 (OPM) 會話的狀態。
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: 'OPM 狀態旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512576"
---
# <a name="opm-status-flags"></a><span data-ttu-id="f2b53-103">OPM 狀態旗標</span><span class="sxs-lookup"><span data-stu-id="f2b53-103">OPM Status Flags</span></span>

<span data-ttu-id="f2b53-104">下表中的旗標會指定輸出保護管理員 (OPM) 會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="f2b53-104">The flags in the following table specify the status of an Output Protection Manager (OPM) session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f2b53-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="f2b53-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f2b53-106">Description</span><span class="sxs-lookup"><span data-stu-id="f2b53-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <span data-ttu-id="f2b53-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span><span class="sxs-lookup"><span data-stu-id="f2b53-107"><dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f2b53-108">一般狀態。</span><span class="sxs-lookup"><span data-stu-id="f2b53-108">Normal status.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <span data-ttu-id="f2b53-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span><span class="sxs-lookup"><span data-stu-id="f2b53-109"><dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f2b53-110">連接的完整性已遭入侵。</span><span class="sxs-lookup"><span data-stu-id="f2b53-110">The integrity of the connection has been compromised.</span></span> <span data-ttu-id="f2b53-111">導致驅動程式設定此旗標的事件範例包括：</span><span class="sxs-lookup"><span data-stu-id="f2b53-111">Examples of events that cause the driver to set this flag include:</span></span><br/>
<ul>
<li><span data-ttu-id="f2b53-112">驅動程式無法再強制執行目前的保護層級。</span><span class="sxs-lookup"><span data-stu-id="f2b53-112">The driver can no longer enforce the current protection level.</span></span></li>
<li><span data-ttu-id="f2b53-113">驅動程式偵測到內部完整性錯誤。</span><span class="sxs-lookup"><span data-stu-id="f2b53-113">The driver detected an internal integrity error.</span></span></li>
<li><span data-ttu-id="f2b53-114">電腦與顯示裝置之間的連接器已插上。</span><span class="sxs-lookup"><span data-stu-id="f2b53-114">The connector between the computer and the display device was unplugged.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <span data-ttu-id="f2b53-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span><span class="sxs-lookup"><span data-stu-id="f2b53-115"><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f2b53-116">連接設定已變更。</span><span class="sxs-lookup"><span data-stu-id="f2b53-116">The connection configuration has changed.</span></span> <span data-ttu-id="f2b53-117">例如，使用者已變更桌面顯示模式。</span><span class="sxs-lookup"><span data-stu-id="f2b53-117">For example, the user has changed the desktop display mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <span data-ttu-id="f2b53-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span><span class="sxs-lookup"><span data-stu-id="f2b53-118"><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f2b53-119">圖形介面卡或驅動程式已遭篡改。</span><span class="sxs-lookup"><span data-stu-id="f2b53-119">The graphics adapter or the driver has been tampered with.</span></span><br/> <span data-ttu-id="f2b53-120"><em>COPP 模擬模式</em>不會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="f2b53-120">This flag is not used in <em>COPP emulation mode</em>.</span></span> <span data-ttu-id="f2b53-121">相反地，如果偵測到篡改，影片輸出會設定 OPM_STATUS_LINK_LOST 旗標。</span><span class="sxs-lookup"><span data-stu-id="f2b53-121">Instead, the video output will set the OPM_STATUS_LINK_LOST flag if it detects tampering.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <span data-ttu-id="f2b53-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span><span class="sxs-lookup"><span data-stu-id="f2b53-122"><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="f2b53-123">已撤銷的 High-Bandwidth 數位內容保護 (HDCP) 裝置會附加至影片輸出。</span><span class="sxs-lookup"><span data-stu-id="f2b53-123">A revoked High-Bandwidth Digital Content Protection (HDCP) device is attached to the video output.</span></span><br/> <span data-ttu-id="f2b53-124">您可以從 <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> 或 <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> 查詢傳回此狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="f2b53-124">This status flag can be returned from an <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> or <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> query.</span></span> <br/> <span data-ttu-id="f2b53-125">撤銷的裝置可能會直接附加至影片輸出，或間接透過 HDCP 中繼器。</span><span class="sxs-lookup"><span data-stu-id="f2b53-125">The revoked device might be attached directly to the video output, or indirectly through an HDCP repeater.</span></span> <span data-ttu-id="f2b53-126">必須要有影片輸出，才能在 HDCP 啟用時偵測這種情況，但不能使用其他方式。</span><span class="sxs-lookup"><span data-stu-id="f2b53-126">A video output is required to detect this condition while HDCP is enabled, but not otherwise.</span></span><br/> <span data-ttu-id="f2b53-127"><em>COPP 模擬模式</em>不會使用此旗標，因為影片輸出不會偵測到處于該模式的已撤銷裝置。</span><span class="sxs-lookup"><span data-stu-id="f2b53-127">This flag is not used in <em>COPP emulation mode</em>, because the video output does not detect revoked devices in that mode.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="f2b53-128">備註</span><span class="sxs-lookup"><span data-stu-id="f2b53-128">Remarks</span></span>

<span data-ttu-id="f2b53-129">其中一些常數相當於 **COPP \_ StatusFlags** 列舉中的值，這些值是在認證的輸出保護通訊協定 (COPP) 中使用。</span><span class="sxs-lookup"><span data-stu-id="f2b53-129">Some of these constants are equivalent to values from the **COPP\_StatusFlags** enumeration used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b53-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2b53-130">Requirements</span></span>



| <span data-ttu-id="f2b53-131">需求</span><span class="sxs-lookup"><span data-stu-id="f2b53-131">Requirement</span></span> | <span data-ttu-id="f2b53-132">值</span><span class="sxs-lookup"><span data-stu-id="f2b53-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b53-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2b53-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f2b53-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2b53-134">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f2b53-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2b53-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f2b53-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2b53-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f2b53-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f2b53-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2b53-138"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2b53-138"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2b53-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2b53-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b53-140">OPM 列舉</span><span class="sxs-lookup"><span data-stu-id="f2b53-140">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




