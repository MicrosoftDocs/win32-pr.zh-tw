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
# <a name="common-device-property-constants"></a>一般裝置屬性常數

除了裝置資訊屬性，Windows 映像取得 (WIA) 裝置具有儲存在應用程式讀取和寫入登錄中的屬性值。 它們會與 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 物件或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件相關聯。 裝置屬性代表裝置資訊，例如連接狀態和裝置時間。 每個裝置屬性都有相關聯的裝置屬性字串。

此處所列的裝置屬性常數是大部分或所有 WIA 硬體裝置的通用屬性。

前置詞 "WIA \_ DPA \_ " 表示所有裝置的裝置屬性，而且是 C/c + + 中使用的命名慣例。 針對腳本用途，這些常數會使用 "Device" 前置詞，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。 來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數/值</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </dl></td>
<td style="text-align: left;">裝置目前的連接狀態。 迷你驅動程式會建立並維護此屬性。<br/> 類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> 屬性可以有下列可能的值。<br/> 
<table>
<thead>
<tr class="header">
<th>連接狀態</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DEVICE_NOT_CONNECTED</td>
<td>裝置未連接。</td>
</tr>
<tr class="even">
<td>WIA_DEVICE_CONNECTED</td>
<td>裝置已連線且可運作。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </dl></td>
<td style="text-align: left;"><p>目前儲存在裝置上的時鐘時間。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>只有具有內部時鐘的裝置才支援此屬性。 如果可以設定裝置時鐘，則此屬性為 [讀取/寫入];否則，它是唯讀的。</p>
<p>WIA 裝置會在 <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> 結構中報告時間。</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </dl></td>
<td style="text-align: left;"><p>裝置固件版本。 此值必須是字串值，例如 &quot; 1.0.4 &quot; 或 &quot; 1.0 abc &quot; 。 迷你驅動程式會建立並維護此屬性。 如果 WIA 迷你驅動程式未提供版本資源，則 WIA 服務會提供值 &quot; 0.0.0.0 &quot; 作為預設值。 應用程式會讀取這個屬性，以判斷 WIA 迷你驅動程式 DLL 的版本。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 
