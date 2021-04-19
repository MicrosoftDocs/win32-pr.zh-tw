---
description: Windows 可攜式裝置支援下列裝置屬性。
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: '裝置屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 696d5fefd65d194f9bb451b0095ed87b90f8a22c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978746"
---
# <a name="device-properties-portabledeviceh"></a><span data-ttu-id="cf442-103">裝置屬性 (PortableDevice .h) </span><span class="sxs-lookup"><span data-stu-id="cf442-103">Device Properties (PortableDevice.h)</span></span>

<span data-ttu-id="cf442-104">Windows 可攜式裝置支援下列裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="cf442-104">Windows Portable Devices supports the following device properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf442-105">屬性</span><span class="sxs-lookup"><span data-stu-id="cf442-105">Property</span></span></th>
<th><span data-ttu-id="cf442-106">VarType</span><span class="sxs-lookup"><span data-stu-id="cf442-106">VarType</span></span></th>
<th><span data-ttu-id="cf442-107">Description</span><span class="sxs-lookup"><span data-stu-id="cf442-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf442-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span></span></td>
<td><span data-ttu-id="cf442-109"><strong>VT_DATE</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-109"><strong>VT_DATE</strong></span></span></td>
<td><span data-ttu-id="cf442-110">裝置上目前的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="cf442-110">The current date and time on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span></span></td>
<td><span data-ttu-id="cf442-112"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-112"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="cf442-113">裝置的固件版本。</span><span class="sxs-lookup"><span data-stu-id="cf442-113">The device's firmware version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="cf442-115"><strong>VT_VECTOR |VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-115"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="cf442-116">唯一16位元組的識別碼，此識別碼在裝置支援的多個傳輸之間是共通的。</span><span class="sxs-lookup"><span data-stu-id="cf442-116">A unique 16-byte identifier that is common across multiple transports supported by the device.</span></span> <span data-ttu-id="cf442-117">如果單一裝置支援多個傳輸，這個屬性可能會用來將各種傳輸 WPD 驅動程式與該裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="cf442-117">If a single device supports multiple transports, this property may be used to associate the various transport WPD drivers with that device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span></span></td>
<td><span data-ttu-id="cf442-119"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-119"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="cf442-120">人們看得懂的裝置製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="cf442-120">A human-readable device manufacturer name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span></span></td>
<td><span data-ttu-id="cf442-122"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-122"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="cf442-123">裝置型號。</span><span class="sxs-lookup"><span data-stu-id="cf442-123">The device model.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="cf442-125"><strong>VT_VECTOR |VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-125"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="cf442-126">唯一的16位元組識別碼，用來區別不同的裝置型號。</span><span class="sxs-lookup"><span data-stu-id="cf442-126">A unique 16-byte identifier used to differentiate among different models of a device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span></span></td>
<td><span data-ttu-id="cf442-128"><strong>VT_UI8</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-128"><strong>VT_UI8</strong></span></span></td>
<td><span data-ttu-id="cf442-129">值，指定裝置的 EUI-64 網路識別碼;這個屬性用於頻外網路作業。如果裝置有 MAC-48 實體網路位址 (一般的 IPv4 網路) ，則在 EUI-64 位址中會將 MAC-48 位址編碼為以 FF-FF 分隔的兩個 MAC-48 位址。</span><span class="sxs-lookup"><span data-stu-id="cf442-129">A value that specifies the EUI-64 network identifier of the device; this property is used for out-of-band network operations.If the device has MAC-48 physical network addresses (typical of IPv4 networks), the MAC-48 address is encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span> <span data-ttu-id="cf442-130">EUI-64 值會以 &quot; 網路 &quot; 或位元組由 &quot; 大到 &quot; 小的順序儲存，其中的 eui-64 位址 01-02-03-ff-ff-04-05-06 會放置在 VT_UI8 中，讓十進位值為72624942021346566。</span><span class="sxs-lookup"><span data-stu-id="cf442-130">The EUI-64 value is stored in &quot;network&quot; or &quot;big-endian&quot; order, where an EUI-64 address of 01-02-03-FF-FF-04-05-06 would be placed in the VT_UI8 such that the decimal value is 72624942021346566.</span></span> <span data-ttu-id="cf442-131">支援名義驗證或安全驗證的任何裝置都需要此屬性。</span><span class="sxs-lookup"><span data-stu-id="cf442-131">This property is required on any device that supports Nominal or Secure Authentication.</span></span> <span data-ttu-id="cf442-132">建議您在僅支援零驗證的裝置上使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="cf442-132">This property is recommended on devices that support only Zero Authentication.</span></span> <span data-ttu-id="cf442-133">此值可供主機用來自動建立裝置的存取權，而不需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="cf442-133">The value can be used by the host to automatically establish access to the device without user intervention.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span></span></td>
<td><span data-ttu-id="cf442-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="cf442-136">從0到100的值，指定裝置電池的電源等級，0為無，100則完全收費。</span><span class="sxs-lookup"><span data-stu-id="cf442-136">A value from 0 to 100 that specifies the power level of the device's battery, with 0 being none, and 100 being fully charged.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span></span></td>
<td><span data-ttu-id="cf442-138">VT_UI4</span><span class="sxs-lookup"><span data-stu-id="cf442-138">VT_UI4</span></span></td>
<td><span data-ttu-id="cf442-139">指定裝置電源來源的 <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> 列舉。</span><span class="sxs-lookup"><span data-stu-id="cf442-139">A <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> enumeration that specifies the power source of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span></span></td>
<td><span data-ttu-id="cf442-141"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-141"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="cf442-142">正在使用的裝置通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cf442-142">The device protocol that is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span></span></td>
<td><span data-ttu-id="cf442-144"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-144"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="cf442-145">裝置的序號。</span><span class="sxs-lookup"><span data-stu-id="cf442-145">The device's serial number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span></span></td>
<td><span data-ttu-id="cf442-147"><strong>VT_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-147"><strong>VT_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="cf442-148">值，指定從裝置傳回的支援格式是否採用慣用順序。</span><span class="sxs-lookup"><span data-stu-id="cf442-148">A value that specifies whether the supported formats returned from the device are in a preferred order.</span></span> <span data-ttu-id="cf442-149">此清單中的第一個格式最適合裝置，而最後一個則是最不慣用的格式。應用程式可以使用此屬性來判斷是否以慣用順序列出裝置支援的格式。</span><span class="sxs-lookup"><span data-stu-id="cf442-149">The first format in the list is most preferred by the device, while the last is the least preferred.Applications may use this property to determine whether a device's supported formats are listed in a preferred order.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span></span></td>
<td><span data-ttu-id="cf442-151"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-151"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="cf442-152">布林值，指定從裝置傳回的支援格式是否採用慣用順序;亦即，第一個傳回的格式最慣用，而最後一個傳回的格式則是最不慣用的。</span><span class="sxs-lookup"><span data-stu-id="cf442-152">A Boolean value that specifies whether the supported formats returned from the device are in a preferred order; that is, the first returned format is most preferred while the last returned format is least preferred.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span></span></td>
<td><span data-ttu-id="cf442-154"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-154"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="cf442-155">指定裝置是否支援非取用物件的布林值。</span><span class="sxs-lookup"><span data-stu-id="cf442-155">A Boolean value that specifies whether the device supports non-consumable objects.</span></span> <span data-ttu-id="cf442-156">這些是裝置僅用來儲存、不以任何方式播放或使用的物件。</span><span class="sxs-lookup"><span data-stu-id="cf442-156">These are objects that the device is only meant to store, not play or use in any way.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span></span></td>
<td><span data-ttu-id="cf442-158"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-158"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="cf442-159">人們看得懂的裝置 <em>同步夥伴</em>描述。</span><span class="sxs-lookup"><span data-stu-id="cf442-159">A human-readable description of a device's <em>synchronization partner</em>.</span></span> <span data-ttu-id="cf442-160">此裝置、應用程式或伺服器會與裝置通訊，以維護兩個夥伴之間的一般狀態或檔案群組。</span><span class="sxs-lookup"><span data-stu-id="cf442-160">This is a device, application, or server that the device communicates with to maintain a common state or group of files between both partners.</span></span> <span data-ttu-id="cf442-161">範例包括電子郵件程式和音樂媒體櫃。</span><span class="sxs-lookup"><span data-stu-id="cf442-161">Examples include e-mail programs and music libraries.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span></span></td>
<td><span data-ttu-id="cf442-163"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-163"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="cf442-164">值，表示使用者在裝置上所設定的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="cf442-164">A value that represents the friendly name set by the user on the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span></span></td>
<td><span data-ttu-id="cf442-166"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-166"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="cf442-167">裝置支援的傳輸，例如 USB、IP 或藍牙。</span><span class="sxs-lookup"><span data-stu-id="cf442-167">the transport supported by the device, such as USB, IP, or Bluetooth.</span></span> <span data-ttu-id="cf442-168">有效的值為 <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> 列舉型別。</span><span class="sxs-lookup"><span data-stu-id="cf442-168">Valid values are of the <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> enumeration type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf442-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span></span></td>
<td><span data-ttu-id="cf442-170"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-170"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="cf442-171">指定裝置類型的值。應用程式只會使用這個屬性來表示用途。</span><span class="sxs-lookup"><span data-stu-id="cf442-171">A value that specifies the device type; applications use this property for representation purposes only.</span></span> <span data-ttu-id="cf442-172">裝置的功能性特性是透過功能物件決定。未提供裝置圖示的裝置（例如，裝置物件的 <strong>WPD_RESOURCE_ICON</strong> ）將會在 WPD 命名空間中以一般圖示表示。</span><span class="sxs-lookup"><span data-stu-id="cf442-172">Functional characteristics of the device are decided through functional objects.Devices that do not supply a device icon, for example, a <strong>WPD_RESOURCE_ICON</strong> for the device object, will be represented in the WPD Namespace with a generic icon.</span></span> <span data-ttu-id="cf442-173">此圖示將視指定的裝置類型而定，例如，如果裝置類型為行動電話，則會使用一般電話圖示。</span><span class="sxs-lookup"><span data-stu-id="cf442-173">This icon will depend on the specified device type, for example, if the device type is a mobile phone, the generic phone icon is used.</span></span> <span data-ttu-id="cf442-174">第一次安裝裝置時，WPD 類別安裝程式會查詢此屬性值，並將其儲存在裝置登錄中的 PORTABLE_DEVICE_TYPE 值下，作為 REG_DWORD。</span><span class="sxs-lookup"><span data-stu-id="cf442-174">On first install of the device, the WPD Class Installer will query this property value and store it in the device registry under the PORTABLE_DEVICE_TYPE value as a REG_DWORD.</span></span><br/> <span data-ttu-id="cf442-175">這個參數的可能值是來自 PortableDevice 中定義的 <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> 列舉。</span><span class="sxs-lookup"><span data-stu-id="cf442-175">This parameter's possible values are from the <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="cf442-176">值為：</span><span class="sxs-lookup"><span data-stu-id="cf442-176">Values are:</span></span><br/> <dl> <span data-ttu-id="cf442-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span></span><br /><span data-ttu-id="cf442-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span></span><br /><span data-ttu-id="cf442-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span></span><br /><span data-ttu-id="cf442-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span></span><br /><span data-ttu-id="cf442-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span></span><br /><span data-ttu-id="cf442-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span></span><br /><span data-ttu-id="cf442-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf442-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span></span></td>
<td><span data-ttu-id="cf442-185"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="cf442-185"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="cf442-186">如果此屬性存在且設定為 <strong>TRUE</strong>，則裝置可搭配 Device Stage 使用。</span><span class="sxs-lookup"><span data-stu-id="cf442-186">If this property exists and is set to <strong>TRUE</strong>, the device can be used with Device Stage .</span></span> <span data-ttu-id="cf442-187">這適用于無法使用 <strong>裝置 Metadata Service</strong>儲存中繼資料的裝置，但會在 Microsoft 伺服器上提供中繼資料。</span><span class="sxs-lookup"><span data-stu-id="cf442-187">This is meant for devices that cannot store metadata using the <strong>Device Metadata Service</strong>, but will provide metadata on the Microsoft servers.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="cf442-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf442-188">Requirements</span></span>



| <span data-ttu-id="cf442-189">需求</span><span class="sxs-lookup"><span data-stu-id="cf442-189">Requirement</span></span> | <span data-ttu-id="cf442-190">值</span><span class="sxs-lookup"><span data-stu-id="cf442-190">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf442-191">標頭</span><span class="sxs-lookup"><span data-stu-id="cf442-191">Header</span></span><br/> | <dl> <span data-ttu-id="cf442-192"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf442-192"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf442-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf442-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf442-194">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="cf442-194">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




