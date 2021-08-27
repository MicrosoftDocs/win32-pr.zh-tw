---
description: Windows影像取得 (WIA) 硬體裝置具有儲存在 Windows 登錄中的屬性值。 如需詳細資訊，請參閱一般裝置屬性常數。
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: '攝影機裝置屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f33e7f2dfd17e535e47026aee173feccb7c69584
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624194"
---
# <a name="camera-device-property-constants"></a>攝影機裝置屬性常數

Windows影像取得 (WIA) 硬體裝置具有儲存在 Windows 登錄中的屬性值。 如需詳細資訊，請參閱 [**一般裝置屬性常數**](-wia-wiaitempropcommondevice.md)。

下列裝置屬性常數（與其相關聯的字串）是數位相機專用的。 前置詞 "WIA \_ DPC \_ " 表示相機的裝置屬性，而且是 C/c + + 中使用的命名慣例。 針對腳本用途，這些常數會使用前置詞 "CameraDevice"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。 來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。

> [!Note]  
> WIA 不支援 Windows Vista 或更新版本中的相機。 針對這些版本的 Windows，請使用 Windows 驅動程式開發工具組 (DDK) 中所述的 Windows 可攜式裝置 (WPD) API，從攝影機取得映射。

 



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >常數/值</th>
<th >描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </dl></td>
<td >相機拍攝的圖片數目。 迷你驅動程式會建立並維護此屬性。<br/> 類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </dl></td>
<td >給定目前的屬性設定，可取得的圖片數目。 如果這些設定變更，而變更影響相機裝置產生的影像大小，則 WIA 迷你驅動程式應該會更新剩餘的圖片數目。 迷你驅動程式會建立並維護此屬性。<br/> 類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </dl></td>
<td >指出相機目前的曝光模式。 應用程式會變更這個屬性，以控制攝影機裝置的曝光模式。<br/> Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> 下表包含七個對此屬性有效的常數。<br/> 
<table>
<thead>
<tr class="header">
<th>曝光模式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMODE_MANUAL</td>
<td>快門速度和光圈是由使用者設定。</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>攝影機會自動設定快門速度和光圈。</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>光圈是由使用者設定，而相機會自動設定快門速度。</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>快門速度是由使用者設定，而相機會自動設定光圈。</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>攝影機會自動設定快門速度和光圈，並針對仍有主題的優化。</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>攝影機會自動設定快門速度和光圈，並針對包含快速運動的場景進行優化。</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>攝影機會自動設定快門速度和光圈，並針對直向攝影進行優化。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </dl></td>
<td ><p>允許調整數位相機自動曝光控制的設定點。 例如，設定為零不會變更原廠設定的自動曝光層級。 單位會在以 &quot; &quot; 1000 因數調整的停止，以允許小數停止值。 2000的設定會對應到兩個 (停止更多的曝光四倍的感應器) 的能源，產生較亮的影像。 若設定為-1000，則會對應至一個低度的 (，感應器的一半能源) 產生較暗的影像。 設定值是在影像曝光的加法系統中 (頂點) 單位。 這個屬性可以表示為清單或值範圍。 只有當裝置將 <strong>WIA_DPC_EXPOSURE_MODE</strong> 屬性設定為 EXPOSUREMODE_MANUAL 時，才會使用此屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 或 WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </dl></td>
<td ><p>對應于依10000調整的快門速度（以秒為單位）。 通常，只有當 <strong>WIA_DPC_EXPOSURE_MODE</strong> 屬性設定為 EXPOSUREMODE_MANUAL 或 EXPOSUREMODE_SHUTTER_PRIORITY 時，裝置才會使用這個屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 或 WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </dl></td>
<td ><p>對應至鏡頭的光圈，以 f-停止數位的單位來調整100。 這個屬性的設定通常只有當 <strong>WIA_DPC_EXPOSURE_MODE</strong> 屬性設定為 EXPOSUREMODE_MANUAL 或 EXPOSUREMODE_APERTURE_PRIORITY 時才有效。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </dl></td>
<td ><p>定義相機裝置的目前閃爍模式設定。 設備磁碟機會列舉這個屬性支援的值。 應用程式會寫入此屬性，以設定相機裝置的閃爍模式。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表包含六個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>Flash 模式</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLASHMODE_AUTO</td>
<td>攝影機裝置決定適當的閃爍設定。</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>無論目前的光源條件為何，相機裝置都會設定為 flash。</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>攝影機裝置設定為 <em>不</em> 會針對拍攝的任何圖片進行閃爍。</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>攝影機裝置會使用紅眼減少來決定適當的閃光燈設定，不論目前的光源條件為何。</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>無論目前的光源條件為何，相機裝置都會設定為使用紅眼降低和閃爍。</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>攝影機裝置設定為與外部 flash 單位進行同步處理。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </dl></td>
<td ><p>定義相機裝置的目前焦點模式設定。 設備磁碟機會列舉這個屬性支援的值。 應用程式會寫入這個屬性，以設定相機裝置的焦點模式。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表有三個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>焦點模式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMODE_MANUAL</td>
<td>攝影機裝置已設定為允許使用者以手動方式進行焦點。</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>攝影機裝置設定為自動焦點。</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>攝影機裝置已設定為使用短範圍宏設定自動焦點。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td ><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td ><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </dl></td>
<td ><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </dl></td>
<td ><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </dl></td>
<td ><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </dl></td>
<td ><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </dl></td>
<td ><p>定義相機裝置目前的電源來源。 應用程式會讀取此屬性，以決定相機使用的電源來源。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表有兩個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>電源模式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>POWERMODE_LINE</td>
<td>攝影機裝置正在電源卡上運作。</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>攝影機裝置以電池電力運作。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </dl></td>
<td ><p>用來操作相機裝置的電池電力百分比。 此值應該是從0到100的整數。 應用程式會讀取此屬性，以決定相機裝置的剩餘電池壽命。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </dl></td>
<td ><p>要用於新捕獲影像的縮圖影像寬度（以圖元為單位）。 應用程式會讀取此值，以取得在其使用者介面中顯示縮圖的估計大小。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入 (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) 或唯讀 (WIA_PROP_NONE) ，有效的值： WIA_PROP_LIST 或 WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </dl></td>
<td ><p>要用於新捕獲影像的縮圖影像寬度（以圖元為單位）。 應用程式會讀取此值，以取得在其使用者介面中顯示縮圖的估計大小。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入 (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) 或唯讀 (WIA_PROP_NONE) ，有效的值： WIA_PROP_LIST 或 WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </dl></td>
<td ><p>用於新捕獲影像的寬度（以圖元為單位）。 這個屬性的有效值清單會與 <strong>WIA_DPC_PICT_HEIGHT</strong> 屬性的有效值清單有一對一的對應關係。 如果個別的寬度和高度具有線性可設定並彼此垂直，則可能會以範圍表示。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </dl></td>
<td ><p>用於新捕獲影像的高度（以圖元為單位）。 這個屬性的有效值清單與 <strong>WIA_DPC_PICT_WIDTH</strong> 屬性的有效值清單會有一對一的對應關係。 如果個別的寬度和高度具有線性可設定並彼此垂直，則可能會以範圍表示。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td ><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </dl></td>
<td ><p>預計在廣泛的場景內容上看到影像品質更接近線性，並且包含範圍或整數清單。 使用較小的整數來表示較低的品質 (也就是最大的壓縮) ，而較大的整數則用來表示較高的品質 (也就是最小的壓縮) 。 裝置上的任何可用設定都是相對於該裝置，因此是裝置特定的設定。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td ><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </dl></td>
<td ><p>以毫秒為單位的時間，這是在時間間隔捕獲作業中的影像捕捉之間的時間。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>、WIA_PROP_LIST 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </dl></td>
<td ><p>裝置在時間間隔期間嘗試捕捉的影像數目。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>、WIA_PROP_LIST 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </dl></td>
<td ><p>在高載操作期間，映射捕捉之間的時間（以毫秒為單位）。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>、WIA_PROP_LIST 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </dl></td>
<td ><p>裝置在高載作業期間嘗試捕獲的影像數目。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>、WIA_PROP_LIST 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </dl></td>
<td ><p>指定相機的特殊影像取得模式。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表有三個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>效果模式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EFFECTMODE_STANDARD</td>
<td>使用相機的標準模式來捕捉映射。</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>捕捉灰階影像。</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>捕獲棕褐色的影像。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </dl></td>
<td ><p>數位相機取得之影像的有效縮放比例，以10倍的比例進行縮放。 10的值對應于缺少數位縮放 (1X) ，也就是相機所捕捉的標準場景大小。 值為20時，會對應至2X 縮放，其中一季的標準場景大小是由相機所捕捉。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </dl></td>
<td ><p>所捕捉影像的已察覺清晰度。 這個屬性可以使用值清單或值範圍。 最小值代表最少的清晰度，而最大值代表最大清晰度。 通常範圍中間的值代表一般或預設的清晰度。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </dl></td>
<td ><p>已捕捉的映射已察覺對比。 這個屬性可以包含值清單或值範圍。 最小支援的值代表最小的對比，而最大值代表最高的對比。 一般來說，範圍中間的值代表一般或預設的對比。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </dl></td>
<td ><p>設定影像捕捉模式。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表有三個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>擷取模式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAPTUREMODE_NORMAL</td>
<td>攝影機的標準模式。</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>依照 <strong>WIA_DPC_BURST_NUMBER</strong> 和 <strong>WIA_DPC_BURST_INTERVAL</strong> 屬性的值所定義，快速連續地捕捉一個以上的影像。</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>依照 <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> 和 <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> 屬性的定義，連續捕捉一個以上的影像。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </dl></td>
<td ><p>值，表示應該在捕獲觸發程式與實際初始資料捕獲之間插入的時間延遲（以毫秒為單位）。 這個屬性不能用來描述單一初始初始的框架之間的時間、多重捕獲（例如高載或時間間隔），其具有個別的間隔屬性 <strong>WIA_DPC_BURST_INTERVAL</strong> 和 <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>。 在這些情況下，它仍會作為系列中第一個映射的初始延遲，與框架之間的時間無關。 如果沒有 precapture 延遲，此屬性應該設定為零。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </dl></td>
<td ><p>允許模擬數位相機上的電影速度設定。 這些設定會對應到 (ASA/等) 的 ISO 指派。 通常，裝置支援離散列舉值，但可能會持續控制某個範圍的值。 0xFFFF 的值對應到自動 ISO 設定。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </dl></td>
<td ><p>指定相機用來自動調整曝光設定的模式。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

<table>
<thead>
<tr class="header">
<th>曝光計量模式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMETERING_AVERAGE</td>
<td>根據整個場景的平均值來設定曝光。</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>根據中央加權平均設定曝光。</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>設定以 multispot 模式為基礎的曝光。</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>根據中心點設定曝光。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </dl></td>
<td ><p>指定相機用來自動調整焦點的模式。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表有兩個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>焦點計量模式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMETERING_CENTERSPOT</td>
<td>根據中央位置調整焦點。</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>根據 multispot 模式調整焦點。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </dl></td>
<td ><p>數位相機的影像捕捉平面和焦點點之間的距離（以毫米為單位）。 0xFFFF 的值對應到大於655計量的設定。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </dl></td>
<td ><p>35mm 對等的焦長度。 這個屬性的值會對應到以毫米乘以100的焦距長度。 焦長度會決定光學縮放。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </dl></td>
<td ><p>以 null 終止的 Unicode 字串，表示分別套用至影像資料的紅色、綠色和藍色增益。 例如， &quot; 4:25:50 &quot; 代表紅色增益4、有25的綠色增益，以及50的藍色增益。</p>
<p>Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </dl></td>
<td ><p>指定數位相機加權色頻。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>以下是這個屬性的可能值清單。</p>

<table>
<thead>
<tr class="header">
<th>白色餘額</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>您可以使用 <strong>WIA_DPC_RGB_GAIN</strong> 屬性直接設定白色餘額。</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>相機會使用自動機制來設定白色餘額。</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>當使用者在將攝影機指向白色表面時按下 [捕捉] 按鈕時，相機會決定白色餘額設定。</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>攝影機會將白色餘額設定為適合用於日光節約條件的值。</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>攝影機會將白色餘額設定為適合搭配螢光燈來源使用的值。</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>攝影機會將白色餘額設定為適合搭配 tungsten 光源使用的值。</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>攝影機會將白色餘額設定為適合搭配電子 flash 使用的值。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </dl></td>
<td ><p>描述 URL。 此 proroperty 所描述的 URL，是從裝置取得影像或物件之後，可以將其上傳至，根據下列其中一個案例。</p>
<ul>
<li>WIA 應用程式會讀取此屬性，並允許使用者自動將影像上傳至 URL。</li>
<li>應用程式會將 URL 和其他裝置 (kiosk 等) 使用此屬性。</li>
</ul>
<p>Microsoft Windows 不會自行上傳影像。</p>
<p>Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </dl></td>
<td ><p>擁有者的名稱 ( 是裝置目前的使用者) 。 裝置會使用這個屬性，在其所捕捉的每個 EXIF 映射中填入演出者欄位。</p>
<p>Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </dl></td>
<td ><p>著作權通知。 裝置會使用這個屬性，在其所捕捉的每個 EXIF 映射中填入著作權欄位。</p>
<p>Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 




