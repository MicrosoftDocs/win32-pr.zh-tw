---
description: 除了裝置資訊屬性，Windows 映像取得 (WIA) 裝置具有儲存在應用程式讀取和寫入登錄中的屬性值。
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: '一般裝置屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511593"
---
# <a name="common-device-property-constants"></a><span data-ttu-id="6ffc6-103">一般裝置屬性常數</span><span class="sxs-lookup"><span data-stu-id="6ffc6-103">Common Device Property Constants</span></span>

<span data-ttu-id="6ffc6-104">除了裝置資訊屬性，Windows 映像取得 (WIA) 裝置具有儲存在應用程式讀取和寫入登錄中的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-104">In addition to device information properties, Windows Image Acquisition (WIA) devices have property values stored in the registry that applications read and write.</span></span> <span data-ttu-id="6ffc6-105">它們會與 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件相關聯。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-105">They are associated with the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object or [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <span data-ttu-id="6ffc6-106">裝置屬性代表裝置資訊，例如連接狀態和裝置時間。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-106">Device properties represent device information such as connection status and device time.</span></span> <span data-ttu-id="6ffc6-107">每個裝置屬性都有相關聯的裝置屬性字串。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-107">Each device property has an associated device property string.</span></span>

<span data-ttu-id="6ffc6-108">此處所列的裝置屬性常數是大部分或所有 WIA 硬體裝置的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-108">The Device Property Constants listed here are common to most or all WIA hardware devices.</span></span>

<span data-ttu-id="6ffc6-109">前置詞 "WIA \_ DPA \_ " 表示所有裝置的裝置屬性，而且是 C/c + + 中使用的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-109">The prefix "WIA\_DPA\_" indicates a Device Property for All devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="6ffc6-110">針對腳本用途，這些常數會使用 "Device" 前置詞，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-110">For scripting purposes these constants use the prefix "Device" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="6ffc6-111">來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-111">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="6ffc6-112">常數/值</span><span class="sxs-lookup"><span data-stu-id="6ffc6-112">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="6ffc6-113">Description</span><span class="sxs-lookup"><span data-stu-id="6ffc6-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <span data-ttu-id="6ffc6-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="6ffc6-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6ffc6-115">裝置目前的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-115">The current connection status for the device.</span></span> <span data-ttu-id="6ffc6-116">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-116">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="6ffc6-117">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ffc6-117">Type: <strong>VT_I4</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="6ffc6-118">屬性可以有下列可能的值。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-118">The property can have the following possible values.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6ffc6-119">連接狀態</span><span class="sxs-lookup"><span data-stu-id="6ffc6-119">Connect Status</span></span></th>
<th><span data-ttu-id="6ffc6-120">定義</span><span class="sxs-lookup"><span data-stu-id="6ffc6-120">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ffc6-121">WIA_DEVICE_NOT_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="6ffc6-121">WIA_DEVICE_NOT_CONNECTED</span></span></td>
<td><span data-ttu-id="6ffc6-122">裝置未連接。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-122">Device is not connected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ffc6-123">WIA_DEVICE_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="6ffc6-123">WIA_DEVICE_CONNECTED</span></span></td>
<td><span data-ttu-id="6ffc6-124">裝置已連線且可運作。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-124">Device is connected and operational.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <span data-ttu-id="6ffc6-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span><span class="sxs-lookup"><span data-stu-id="6ffc6-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ffc6-126">目前儲存在裝置上的時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-126">The current clock time that is stored on the device.</span></span> <span data-ttu-id="6ffc6-127">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-127">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="6ffc6-128">類型： <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ffc6-128">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong>, Access: Read/Write or Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6ffc6-129">只有具有內部時鐘的裝置才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-129">This property is supported only by devices that have an internal clock.</span></span> <span data-ttu-id="6ffc6-130">如果可以設定裝置時鐘，則此屬性為 [讀取/寫入];否則，它是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-130">If the device clock can be set, this property is Read/Write; otherwise, it is Read-only.</span></span></p>
<p><span data-ttu-id="6ffc6-131">WIA 裝置會在 <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> 結構中報告時間。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-131">WIA devices report time in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <span data-ttu-id="6ffc6-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="6ffc6-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ffc6-133">裝置固件版本。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-133">The device firmware version.</span></span> <span data-ttu-id="6ffc6-134">此值必須是字串值，例如 &quot; 1.0.4 &quot; 或 &quot; 1.0 abc &quot; 。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-134">This value must be a string value, such as &quot;1.0.4&quot; or &quot;1.0abc&quot;.</span></span> <span data-ttu-id="6ffc6-135">迷你驅動程式會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-135">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="6ffc6-136">如果 WIA 迷你驅動程式未提供版本資源，則 WIA 服務會提供值 &quot; 0.0.0.0 &quot; 作為預設值。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-136">If the WIA minidriver does not supply a version resource, the WIA service supplies the value &quot;0.0.0.0&quot; as a default.</span></span> <span data-ttu-id="6ffc6-137">應用程式會讀取這個屬性，以判斷 WIA 迷你驅動程式 DLL 的版本。</span><span class="sxs-lookup"><span data-stu-id="6ffc6-137">An application reads this property to determine the version of the WIA minidriver DLL.</span></span></p>
<p><span data-ttu-id="6ffc6-138">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ffc6-138">Type: <strong>VT_BSTR</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="6ffc6-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ffc6-139">Requirements</span></span>



| <span data-ttu-id="6ffc6-140">需求</span><span class="sxs-lookup"><span data-stu-id="6ffc6-140">Requirement</span></span> | <span data-ttu-id="6ffc6-141">值</span><span class="sxs-lookup"><span data-stu-id="6ffc6-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ffc6-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ffc6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6ffc6-143">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ffc6-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6ffc6-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ffc6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6ffc6-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ffc6-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6ffc6-146">標頭</span><span class="sxs-lookup"><span data-stu-id="6ffc6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ffc6-147"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ffc6-147"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
