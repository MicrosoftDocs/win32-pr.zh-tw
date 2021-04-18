---
title: 遠端桌面通訊協定提供者結構
description: 自訂遠端通訊協定 API 支援下列結構。
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964948"
---
# <a name="remote-desktop-protocol-provider-structures"></a><span data-ttu-id="4f33e-103">遠端桌面通訊協定提供者結構</span><span class="sxs-lookup"><span data-stu-id="4f33e-103">Remote Desktop Protocol Provider Structures</span></span>

<span data-ttu-id="4f33e-104">自訂遠端通訊協定 API 支援下列結構。</span><span class="sxs-lookup"><span data-stu-id="4f33e-104">The custom remote protocol API supports the following structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4f33e-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="4f33e-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4f33e-106">**TSMF \_ \_ \_ 中的支援資料**</span><span class="sxs-lookup"><span data-stu-id="4f33e-106">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> <dd>

<span data-ttu-id="4f33e-107">包含媒體格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-107">Contains information about media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-108">**TSMF \_ 支援 \_ 資料 \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="4f33e-108">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> <dd>

<span data-ttu-id="4f33e-109">包含媒體格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-109">Contains information about media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-110">**TSMF \_ 支援 \_ NODEDATA \_**</span><span class="sxs-lookup"><span data-stu-id="4f33e-110">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> <dd>

<span data-ttu-id="4f33e-111">在 TSMF 中使用，可 [**\_ 支援結構 \_ \_ 中的資料**](tsmf-support-data-in.md) ，以包含支援之媒體格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-111">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-112">**TSMF \_ 支援 \_ NODEDATA \_**</span><span class="sxs-lookup"><span data-stu-id="4f33e-112">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> <dd>

<span data-ttu-id="4f33e-113">在 TSMF 內使用可 [**\_ 支援 \_ 資料 \_ 輸出**](tsmf-support-data-out.md) 結構，以包含支援之媒體格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-113">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-114">**WRDS \_ 連接 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="4f33e-114">**WRDS\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

<span data-ttu-id="4f33e-115">包含遠端會話的連接設定資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-115">Contains connection setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-116">**WRDS \_ 連接 \_ 設定 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4f33e-116">**WRDS\_CONNECTION\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

<span data-ttu-id="4f33e-117">包含遠端會話的連接設定資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-117">Contains connection setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-118">**WRDS \_ 動態 \_ 時區 \_ \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="4f33e-118">**WRDS\_DYNAMIC\_TIME\_ZONE\_INFORMATION**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

<span data-ttu-id="4f33e-119">包含動態時區資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-119">Contains dynamic time zone information.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-120">**WRDS 接聽程式 \_ \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="4f33e-120">**WRDS\_LISTENER\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

<span data-ttu-id="4f33e-121">包含遠端會話的接聽程式設定資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-121">Contains listener setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-122">**WRDS 接聽程式 \_ \_ 設定 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4f33e-122">**WRDS\_LISTENER\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

<span data-ttu-id="4f33e-123">包含遠端會話的接聽程式設定。</span><span class="sxs-lookup"><span data-stu-id="4f33e-123">Contains listener settings for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-124">**WRDS \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="4f33e-124">**WRDS\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

<span data-ttu-id="4f33e-125">包含遠端會話的原則相關設定資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-125">Contains policy-related setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-126">**WRDS \_ 設定 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4f33e-126">**WRDS\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

<span data-ttu-id="4f33e-127">包含遠端會話的原則相關設定。</span><span class="sxs-lookup"><span data-stu-id="4f33e-127">Contains policy-related settings for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-128">**WTS 快取 \_ \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="4f33e-128">**WTS\_CACHE\_STATS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

<span data-ttu-id="4f33e-129">包含通訊協定快取統計資料。</span><span class="sxs-lookup"><span data-stu-id="4f33e-129">Contains protocol cache statistics.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-130">**WTS \_ 顯示 \_ IOCTL**</span><span class="sxs-lookup"><span data-stu-id="4f33e-130">**WTS\_DISPLAY\_IOCTL**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

<span data-ttu-id="4f33e-131">包含用戶端顯示的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-131">Contains information about the client display.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-132">**WTS \_ 用戶端 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="4f33e-132">**WTS\_CLIENT\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

<span data-ttu-id="4f33e-133">包含用戶端連接的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-133">Contains information about the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-134">**WTS \_ 授權 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="4f33e-134">**WTS\_LICENSE\_CAPABILITIES**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

<span data-ttu-id="4f33e-135">包含用戶端授權功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-135">Contains information about the licensing capabilities of the client.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-136">**WTS \_ 原則 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="4f33e-136">**WTS\_POLICY\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

<span data-ttu-id="4f33e-137">包含由遠端桌面服務服務傳遞至通訊協定的原則資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-137">Contains policy information that is passed by the Remote Desktop Services service to the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-138">**WTS \_ 屬性 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="4f33e-138">**WTS\_PROPERTY\_VALUE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

<span data-ttu-id="4f33e-139">包含要從通訊協定取得之屬性值的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-139">Contains information about a property value to retrieve from the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-140">**WTS \_ 通訊協定快取 \_**</span><span class="sxs-lookup"><span data-stu-id="4f33e-140">**WTS\_PROTOCOL\_CACHE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

<span data-ttu-id="4f33e-141">包含快取讀取和快取點擊的數目。</span><span class="sxs-lookup"><span data-stu-id="4f33e-141">Contains the number of cache reads and cache hits.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-142">**WTS \_ 通訊協定 \_ 計數器**</span><span class="sxs-lookup"><span data-stu-id="4f33e-142">**WTS\_PROTOCOL\_COUNTERS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

<span data-ttu-id="4f33e-143">包含通訊協定效能計數器。</span><span class="sxs-lookup"><span data-stu-id="4f33e-143">Contains protocol performance counters.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-144">**WTS \_ 通訊協定 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="4f33e-144">**WTS\_PROTOCOL\_STATUS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

<span data-ttu-id="4f33e-145">包含通訊協定狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-145">Contains information about the status of the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-146">**WTS \_ 服務 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="4f33e-146">**WTS\_SERVICE\_STATE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

<span data-ttu-id="4f33e-147">包含遠端桌面服務服務狀態變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-147">Contains information about changes in the state of the Remote Desktop Services service.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-148">**WTS \_ 會話 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="4f33e-148">**WTS\_SESSION\_ID**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

<span data-ttu-id="4f33e-149">包含可唯一識別會話的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="4f33e-149">Contains a **GUID** that uniquely identifies a session.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-150">**WTS \_ SMALL \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="4f33e-150">**WTS\_SMALL\_RECT**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

<span data-ttu-id="4f33e-151">包含用戶端視窗座標。</span><span class="sxs-lookup"><span data-stu-id="4f33e-151">Contains client window coordinates.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-152">**WTS \_ SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="4f33e-152">**WTS\_SOCKADDR**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

<span data-ttu-id="4f33e-153">包含通訊端位址。</span><span class="sxs-lookup"><span data-stu-id="4f33e-153">Contains a socket address.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-154">**WTS \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="4f33e-154">**WTS\_SYSTEMTIME**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

<span data-ttu-id="4f33e-155">指定標準時間和日光節約時間之間轉換的日期和時間資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-155">Specifies date and time information for transitions between standard time and daylight saving time.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-156">**WTS \_ 時區 \_ \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="4f33e-156">**WTS\_TIME\_ZONE\_INFORMATION**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

<span data-ttu-id="4f33e-157">包含用戶端時區資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-157">Contains client time zone information.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-158">**WTS \_ 使用者 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="4f33e-158">**WTS\_USER\_CREDENTIAL**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

<span data-ttu-id="4f33e-159">包含使用者的認證資訊。</span><span class="sxs-lookup"><span data-stu-id="4f33e-159">Contains credential information for a user.</span></span>

</dd> <dt>

[<span data-ttu-id="4f33e-160">**WTS \_ 使用者 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="4f33e-160">**WTS\_USER\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

<span data-ttu-id="4f33e-161">包含選取的用戶端屬性值。</span><span class="sxs-lookup"><span data-stu-id="4f33e-161">Contains select client property values.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="4f33e-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f33e-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f33e-163">遠端桌面通訊協定提供者參考</span><span class="sxs-lookup"><span data-stu-id="4f33e-163">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="4f33e-164">遠端桌面通訊協定提供者列舉</span><span class="sxs-lookup"><span data-stu-id="4f33e-164">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="4f33e-165">遠端桌面通訊協定提供者介面</span><span class="sxs-lookup"><span data-stu-id="4f33e-165">Remote Desktop Protocol Provider Interfaces</span></span>](custom-remote-protocol-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4f33e-166">遠端桌面通訊協定提供者聯集</span><span class="sxs-lookup"><span data-stu-id="4f33e-166">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




