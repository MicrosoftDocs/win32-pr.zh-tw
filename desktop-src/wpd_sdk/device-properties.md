---
description: Windows可攜式裝置支援下列裝置屬性。
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
ms.openlocfilehash: 5490323e60d353fade6dfb7f517533ecb5fa26ca9e78ae221b9ff584d8c13a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430976"
---
# <a name="device-properties-portabledeviceh"></a>裝置屬性 (PortableDevice .h) 

Windows可攜式裝置支援下列裝置屬性。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>VarType</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></td>
<td><strong>VT_DATE</strong></td>
<td>裝置上目前的日期和時間。</td>
</tr>
<tr class="even">
<td><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>裝置的固件版本。</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR |VT_UI1</strong></td>
<td>唯一16位元組的識別碼，此識別碼在裝置支援的多個傳輸之間是共通的。 如果單一裝置支援多個傳輸，這個屬性可能會用來將各種傳輸 WPD 驅動程式與該裝置產生關聯。</td>
</tr>
<tr class="even">
<td><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>人們看得懂的裝置製造商名稱。</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>裝置型號。</td>
</tr>
<tr class="even">
<td><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR |VT_UI1</strong></td>
<td>唯一的16位元組識別碼，用來區別不同的裝置型號。</td>
</tr>
<tr class="odd">
<td><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></td>
<td><strong>VT_UI8</strong></td>
<td>值，指定裝置的 EUI-64 網路識別碼;這個屬性用於頻外網路作業。如果裝置有 MAC-48 實體網路位址 (一般的 IPv4 網路) ，則在 EUI-64 位址中會將 MAC-48 位址編碼為以 FF-FF 分隔的兩個 MAC-48 位址。 EUI-64 值會以 &quot; 網路 &quot; 或位元組由 &quot; 大到 &quot; 小的順序儲存，其中的 eui-64 位址 01-02-03-ff-ff-04-05-06 會放置在 VT_UI8 中，讓十進位值為72624942021346566。 支援名義驗證或安全驗證的任何裝置都需要此屬性。 建議您在僅支援零驗證的裝置上使用此屬性。 此值可供主機用來自動建立裝置的存取權，而不需要使用者介入。<br/></td>
</tr>
<tr class="even">
<td><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></td>
<td><strong>VT_UI4</strong></td>
<td>從0到100的值，指定裝置電池的電源等級，0為無，100則完全收費。</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></td>
<td>VT_UI4</td>
<td>指定裝置電源來源的 <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> 列舉。</td>
</tr>
<tr class="even">
<td><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>正在使用的裝置通訊協定。</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>裝置的序號。</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></td>
<td><strong>VT_UNKNOWN</strong></td>
<td>值，指定從裝置傳回的支援格式是否採用慣用順序。 此清單中的第一個格式最適合裝置，而最後一個則是最不慣用的格式。應用程式可以使用此屬性來判斷是否以慣用順序列出裝置支援的格式。<br/></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>布林值，指定從裝置傳回的支援格式是否採用慣用順序;亦即，第一個傳回的格式最慣用，而最後一個傳回的格式則是最不慣用的。</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>指定裝置是否支援非取用物件的布林值。 這些是裝置僅用來儲存、不以任何方式播放或使用的物件。</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>人們看得懂的裝置 <em>同步夥伴</em>描述。 此裝置、應用程式或伺服器會與裝置通訊，以維護兩個夥伴之間的一般狀態或檔案群組。 範例包括電子郵件程式和音樂媒體櫃。</td>
</tr>
<tr class="even">
<td><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>值，表示使用者在裝置上所設定的易記名稱。</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></td>
<td><strong>VT_UI4</strong></td>
<td>裝置支援的傳輸，例如 USB、IP 或藍牙。 有效的值為 <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> 列舉型別。</td>
</tr>
<tr class="even">
<td><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>指定裝置類型的值。應用程式只會使用這個屬性來表示用途。 裝置的功能性特性是透過功能物件決定。未提供裝置圖示的裝置（例如，裝置物件的 <strong>WPD_RESOURCE_ICON</strong> ）將會在 WPD 命名空間中以一般圖示表示。 此圖示將視指定的裝置類型而定，例如，如果裝置類型為行動電話，則會使用一般電話圖示。 第一次安裝裝置時，WPD 類別安裝程式會查詢此屬性值，並將其儲存在裝置登錄中的 PORTABLE_DEVICE_TYPE 值下，作為 REG_DWORD。<br/> 這個參數的可能值是來自 PortableDevice 中定義的 <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> 列舉。 值為：<br/> <dl> <strong>WPD_DEVICE_TYPE_GENERIC</strong><br />
<strong>WPD_DEVICE_TYPE_CAMERA</strong><br />
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong><br />
<strong>WPD_DEVICE_TYPE_PHONE</strong><br />
<strong>WPD_DEVICE_TYPE_VIDEO</strong><br />
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong><br />
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>如果此屬性存在且設定為 <strong>TRUE</strong>，則裝置可搭配 Device Stage 使用。 這適用于無法使用 <strong>裝置 Metadata Service</strong>儲存中繼資料的裝置，但會在 Microsoft 伺服器上提供中繼資料。</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WPD 屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




