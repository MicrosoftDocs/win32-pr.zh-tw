---
description: 裝置資訊屬性是描述裝置設定和安裝的屬性。
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: '裝置資訊屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 18c44bb310c2dcee5bb227e0885a71b58f5b362e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967143"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="c1275-103">裝置資訊屬性常數</span><span class="sxs-lookup"><span data-stu-id="c1275-103">Device Information Property Constants</span></span>

<span data-ttu-id="c1275-104">裝置資訊屬性是描述裝置設定和安裝的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="c1275-105">這些屬性可透過 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) 介面取得，也可以透過根項目取得。</span><span class="sxs-lookup"><span data-stu-id="c1275-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="c1275-106">裝置資訊屬性的前面會加上 "WIA \_ DIP \_ " (裝置資訊屬性) ，而且是由 Windows 映像取得 (WIA) 提供。</span><span class="sxs-lookup"><span data-stu-id="c1275-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="c1275-107">針對腳本用途，這些常數會使用前置詞 "DeviceInfo"，而且是 [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) 列舉型別的一部分。</span><span class="sxs-lookup"><span data-stu-id="c1275-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="c1275-108">來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。</span><span class="sxs-lookup"><span data-stu-id="c1275-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c1275-109">常數/值</span><span class="sxs-lookup"><span data-stu-id="c1275-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c1275-110">Description</span><span class="sxs-lookup"><span data-stu-id="c1275-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="c1275-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c1275-112">WIA 迷你驅動程式的裝置識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="c1275-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="c1275-113">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="c1275-114">類型： VT_BSTR、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="c1275-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c1275-116">WIA 迷你驅動程式的廠商描述字串。</span><span class="sxs-lookup"><span data-stu-id="c1275-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="c1275-117">廠商描述是從 INF 檔案取得的。</span><span class="sxs-lookup"><span data-stu-id="c1275-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="c1275-118">應用程式會讀取此屬性，以取得裝置廠商的描述。</span><span class="sxs-lookup"><span data-stu-id="c1275-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="c1275-119">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="c1275-120">類型： VT_BSTR、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="c1275-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c1275-122">WIA 迷你驅動程式的裝置描述字串。</span><span class="sxs-lookup"><span data-stu-id="c1275-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="c1275-123">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-124">這個屬性所包含的裝置描述字串是從 INF 檔案取得的。</span><span class="sxs-lookup"><span data-stu-id="c1275-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="c1275-125">應用程式會讀取此屬性來取得裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="c1275-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="c1275-126">類型： VT_BSTR、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="c1275-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c1275-128">裝置類型和裝置子類型。</span><span class="sxs-lookup"><span data-stu-id="c1275-128">The device type and device subtype.</span></span> <span data-ttu-id="c1275-129">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-130">使用 GET_STIDEVICE_TYPE 宏來取得裝置類型。</span><span class="sxs-lookup"><span data-stu-id="c1275-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="c1275-131">從 INF 檔案取得裝置類型和子類型。</span><span class="sxs-lookup"><span data-stu-id="c1275-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="c1275-132">應用程式會讀取此屬性，以判斷其是否使用掃描器、相機或影片裝置。</span><span class="sxs-lookup"><span data-stu-id="c1275-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="c1275-133">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="c1275-134">目前，裝置類型的定義如下。</span><span class="sxs-lookup"><span data-stu-id="c1275-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="c1275-135">星號 \* 表示 Windows Vista 和更新版本不支援裝置類型。</span><span class="sxs-lookup"><span data-stu-id="c1275-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="c1275-136">雙星號 \* \* 表示 Windows Server 2003、Windows Vista 或更新版本不支援裝置類型。</span><span class="sxs-lookup"><span data-stu-id="c1275-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c1275-137">類型</span><span class="sxs-lookup"><span data-stu-id="c1275-137">Type</span></span></th>
<th><span data-ttu-id="c1275-138">值</span><span class="sxs-lookup"><span data-stu-id="c1275-138">Value</span></span></th>
<th><span data-ttu-id="c1275-139">定義</span><span class="sxs-lookup"><span data-stu-id="c1275-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1275-140">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="c1275-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="c1275-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="c1275-141">0x0000</span></span></td>
<td><span data-ttu-id="c1275-142">預設裝置</span><span class="sxs-lookup"><span data-stu-id="c1275-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1275-143">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="c1275-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="c1275-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="c1275-144">0x0001</span></span></td>
<td><span data-ttu-id="c1275-145">掃描器裝置 (查看 <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> 來判斷掃描器是平板或紙匣。 ) </span><span class="sxs-lookup"><span data-stu-id="c1275-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1275-146">StiDeviceTypeDigitalCamera\*</span><span class="sxs-lookup"><span data-stu-id="c1275-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="c1275-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="c1275-147">0x0002</span></span></td>
<td><span data-ttu-id="c1275-148">攝影機裝置</span><span class="sxs-lookup"><span data-stu-id="c1275-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1275-149">StiDeviceTypeStreamingVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="c1275-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="c1275-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="c1275-150">0x0003</span></span></td>
<td><span data-ttu-id="c1275-151">影片裝置</span><span class="sxs-lookup"><span data-stu-id="c1275-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="c1275-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-153">已安裝裝置的埠名稱，由操作裝置的核心模式驅動程式所指派。</span><span class="sxs-lookup"><span data-stu-id="c1275-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="c1275-154">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-155">應用程式會讀取此屬性，以決定埠名稱。</span><span class="sxs-lookup"><span data-stu-id="c1275-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="c1275-156">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="c1275-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-158">裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1275-158">The name of the device.</span></span> <span data-ttu-id="c1275-159">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-160">這個屬性所包含的裝置名稱是從 INF 檔案取得的。</span><span class="sxs-lookup"><span data-stu-id="c1275-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="c1275-161">應用程式會讀取此屬性來取得裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1275-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="c1275-162">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="c1275-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-164">WIA 迷你驅動程式正在執行的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c1275-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="c1275-165">這是 Windows XP 和更新版本的選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="c1275-166">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="c1275-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-168">遠端電腦上所安裝之 WIA 裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1275-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="c1275-169">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-170">它只會由 WIA 服務在內部使用。</span><span class="sxs-lookup"><span data-stu-id="c1275-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="c1275-171">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="c1275-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-173">廠商提供的 CLSID，適用于使用 WIA 迷你驅動程式安裝的任何 UI 延伸 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="c1275-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="c1275-174">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-175">這個屬性所包含的 UI CLSID 值是從 INF 檔案取得的。</span><span class="sxs-lookup"><span data-stu-id="c1275-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="c1275-176">如果未指定任何 UI CLSID，則 WIA 服務會提供預設值。</span><span class="sxs-lookup"><span data-stu-id="c1275-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="c1275-177">只有在顯示 UI 時，WIA 服務才會在內部使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="c1275-178">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="c1275-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-180">裝置使用的連線類型。</span><span class="sxs-lookup"><span data-stu-id="c1275-180">The type of connection that the device is using.</span></span> <span data-ttu-id="c1275-181">WIA 服務會建立並維護這個屬性，而且只有 WIA 服務可以變更它。</span><span class="sxs-lookup"><span data-stu-id="c1275-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="c1275-182">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="c1275-183">屬性可以有下列可能的值。</span><span class="sxs-lookup"><span data-stu-id="c1275-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c1275-184">值</span><span class="sxs-lookup"><span data-stu-id="c1275-184">Value</span></span></th>
<th><span data-ttu-id="c1275-185">定義</span><span class="sxs-lookup"><span data-stu-id="c1275-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1275-186">1</span><span class="sxs-lookup"><span data-stu-id="c1275-186">1</span></span></td>
<td><span data-ttu-id="c1275-187">一般 WDM 裝置</span><span class="sxs-lookup"><span data-stu-id="c1275-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1275-188">2</span><span class="sxs-lookup"><span data-stu-id="c1275-188">2</span></span></td>
<td><span data-ttu-id="c1275-189">SCSI 裝置</span><span class="sxs-lookup"><span data-stu-id="c1275-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1275-190">4</span><span class="sxs-lookup"><span data-stu-id="c1275-190">4</span></span></td>
<td><span data-ttu-id="c1275-191">USB 裝置</span><span class="sxs-lookup"><span data-stu-id="c1275-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1275-192">8</span><span class="sxs-lookup"><span data-stu-id="c1275-192">8</span></span></td>
<td><span data-ttu-id="c1275-193">序列裝置</span><span class="sxs-lookup"><span data-stu-id="c1275-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1275-194">16</span><span class="sxs-lookup"><span data-stu-id="c1275-194">16</span></span></td>
<td><span data-ttu-id="c1275-195">平行裝置</span><span class="sxs-lookup"><span data-stu-id="c1275-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="c1275-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-197">裝置目前的傳輸速率設定。</span><span class="sxs-lookup"><span data-stu-id="c1275-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="c1275-198">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-199">如果裝置未透過 &quot; &quot; 序列纜線連接，此值應該是空的。</span><span class="sxs-lookup"><span data-stu-id="c1275-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="c1275-200">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="c1275-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-202">從 INF 檔案取得之裝置的一般 STI 功能。</span><span class="sxs-lookup"><span data-stu-id="c1275-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="c1275-203">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-204">應用程式會讀取此屬性，以判斷裝置的一般 STI 功能。</span><span class="sxs-lookup"><span data-stu-id="c1275-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="c1275-205">類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="c1275-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-207"> (的數位，表示為安裝在系統上的目前 WIA 版本的字串) 。</span><span class="sxs-lookup"><span data-stu-id="c1275-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="c1275-208">應用程式會讀取此屬性，以判斷安裝在系統上的 WIA 版本。</span><span class="sxs-lookup"><span data-stu-id="c1275-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="c1275-209">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-210">這個屬性可在 Windows XP 及更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="c1275-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="c1275-211">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="c1275-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-213">WIA 迷你驅動程式的目前 DLL 版本。</span><span class="sxs-lookup"><span data-stu-id="c1275-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="c1275-214">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-215">這個屬性可在 Windows XP 及更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="c1275-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="c1275-216">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="c1275-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-218">裝置目前的 PnP 識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1275-218">The current PnP id for the device.</span></span> <span data-ttu-id="c1275-219">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-220">這個屬性可在 Windows Vista 和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="c1275-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="c1275-221">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="c1275-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="c1275-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="c1275-223">一般 STI 驅動程式版本。</span><span class="sxs-lookup"><span data-stu-id="c1275-223">The generic STI driver version.</span></span> <span data-ttu-id="c1275-224">WIA 服務會建立並維護此屬性。</span><span class="sxs-lookup"><span data-stu-id="c1275-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="c1275-225">應用程式會讀取這個屬性，以判斷一般 STI 驅動程式版本。</span><span class="sxs-lookup"><span data-stu-id="c1275-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="c1275-226">這個屬性可在 Windows Vista 和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="c1275-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="c1275-227">類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="c1275-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c1275-228">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1275-228">Requirements</span></span>



| <span data-ttu-id="c1275-229">需求</span><span class="sxs-lookup"><span data-stu-id="c1275-229">Requirement</span></span> | <span data-ttu-id="c1275-230">值</span><span class="sxs-lookup"><span data-stu-id="c1275-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c1275-231">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1275-231">Minimum supported client</span></span><br/> | <span data-ttu-id="c1275-232">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1275-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c1275-233">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1275-233">Minimum supported server</span></span><br/> | <span data-ttu-id="c1275-234">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1275-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c1275-235">標頭</span><span class="sxs-lookup"><span data-stu-id="c1275-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1275-236"><dt>Wiadef。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1275-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




