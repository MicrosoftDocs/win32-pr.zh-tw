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
# <a name="device-information-property-constants"></a>裝置資訊屬性常數

裝置資訊屬性是描述裝置設定和安裝的屬性。 這些屬性可透過 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 或 [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) 介面取得，也可以透過根項目取得。 裝置資訊屬性的前面會加上 "WIA \_ DIP \_ " (裝置資訊屬性) ，而且是由 Windows 映像取得 (WIA) 提供。 針對腳本用途，這些常數會使用前置詞 "DeviceInfo"，而且是 [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) 列舉型別的一部分。 來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。



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
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </dl></td>
<td style="text-align: left;">WIA 迷你驅動程式的裝置識別碼字串。 WIA 服務會建立並維護此屬性。<br/> 類型： VT_BSTR、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </dl></td>
<td style="text-align: left;">WIA 迷你驅動程式的廠商描述字串。 廠商描述是從 INF 檔案取得的。 應用程式會讀取此屬性，以取得裝置廠商的描述。 WIA 服務會建立並維護此屬性。<br/> 類型： VT_BSTR、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </dl></td>
<td style="text-align: left;">WIA 迷你驅動程式的裝置描述字串。 WIA 服務會建立並維護此屬性。 這個屬性所包含的裝置描述字串是從 INF 檔案取得的。 應用程式會讀取此屬性來取得裝置的描述。<br/> 類型： VT_BSTR、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </dl></td>
<td style="text-align: left;">裝置類型和裝置子類型。 WIA 服務會建立並維護此屬性。 使用 GET_STIDEVICE_TYPE 宏來取得裝置類型。 從 INF 檔案取得裝置類型和子類型。 應用程式會讀取此屬性，以判斷其是否使用掃描器、相機或影片裝置。<br/> 類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> 目前，裝置類型的定義如下。 星號 * 表示 Windows Vista 和更新版本不支援裝置類型。 雙星號 * * 表示 Windows Server 2003、Windows Vista 或更新版本不支援裝置類型。 <br/> 
<table>
<thead>
<tr class="header">
<th>類型</th>
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>StiDeviceTypeDefault</td>
<td>0x0000</td>
<td>預設裝置</td>
</tr>
<tr class="even">
<td>StiDeviceTypeScanner</td>
<td>0x0001</td>
<td>掃描器裝置 (查看 <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> 來判斷掃描器是平板或紙匣。 ) </td>
</tr>
<tr class="odd">
<td>StiDeviceTypeDigitalCamera*</td>
<td>0x0002</td>
<td>攝影機裝置</td>
</tr>
<tr class="even">
<td>StiDeviceTypeStreamingVideo**</td>
<td>0x0003</td>
<td>影片裝置</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </dl></td>
<td style="text-align: left;"><p>已安裝裝置的埠名稱，由操作裝置的核心模式驅動程式所指派。 WIA 服務會建立並維護此屬性。 應用程式會讀取此屬性，以決定埠名稱。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </dl></td>
<td style="text-align: left;"><p>裝置的名稱。 WIA 服務會建立並維護此屬性。 這個屬性所包含的裝置名稱是從 INF 檔案取得的。 應用程式會讀取此屬性來取得裝置的名稱。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </dl></td>
<td style="text-align: left;"><p>WIA 迷你驅動程式正在執行的伺服器名稱。 這是 Windows XP 和更新版本的選擇性屬性。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </dl></td>
<td style="text-align: left;"><p>遠端電腦上所安裝之 WIA 裝置的裝置識別碼。 WIA 服務會建立並維護此屬性。 它只會由 WIA 服務在內部使用。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </dl></td>
<td style="text-align: left;"><p>廠商提供的 CLSID，適用于使用 WIA 迷你驅動程式安裝的任何 UI 延伸 COM 物件。 WIA 服務會建立並維護此屬性。 這個屬性所包含的 UI CLSID 值是從 INF 檔案取得的。 如果未指定任何 UI CLSID，則 WIA 服務會提供預設值。 只有在顯示 UI 時，WIA 服務才會在內部使用此屬性。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </dl></td>
<td style="text-align: left;"><p>裝置使用的連線類型。 WIA 服務會建立並維護這個屬性，而且只有 WIA 服務可以變更它。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>屬性可以有下列可能的值。</p>

<table>
<thead>
<tr class="header">
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>一般 WDM 裝置</td>
</tr>
<tr class="even">
<td>2</td>
<td>SCSI 裝置</td>
</tr>
<tr class="odd">
<td>4</td>
<td>USB 裝置</td>
</tr>
<tr class="even">
<td>8</td>
<td>序列裝置</td>
</tr>
<tr class="odd">
<td>16</td>
<td>平行裝置</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </dl></td>
<td style="text-align: left;"><p>裝置目前的傳輸速率設定。 WIA 服務會建立並維護此屬性。 如果裝置未透過 &quot; &quot; 序列纜線連接，此值應該是空的。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </dl></td>
<td style="text-align: left;"><p>從 INF 檔案取得之裝置的一般 STI 功能。 WIA 服務會建立並維護此屬性。 應用程式會讀取此屬性，以判斷裝置的一般 STI 功能。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </dl></td>
<td style="text-align: left;"><p> (的數位，表示為安裝在系統上的目前 WIA 版本的字串) 。 應用程式會讀取此屬性，以判斷安裝在系統上的 WIA 版本。 WIA 服務會建立並維護此屬性。 這個屬性可在 Windows XP 及更新版本中使用。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </dl></td>
<td style="text-align: left;"><p>WIA 迷你驅動程式的目前 DLL 版本。 WIA 服務會建立並維護此屬性。 這個屬性可在 Windows XP 及更新版本中使用。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </dl></td>
<td style="text-align: left;"><p>裝置目前的 PnP 識別碼。 WIA 服務會建立並維護此屬性。 這個屬性可在 Windows Vista 和更新版本中使用。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </dl></td>
<td style="text-align: left;"><p>一般 STI 驅動程式版本。 WIA 服務會建立並維護此屬性。 應用程式會讀取這個屬性，以判斷一般 STI 驅動程式版本。 這個屬性可在 Windows Vista 和更新版本中使用。</p>
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



 

 




