---
description: 下列常數會指定一組有效的 Windows 映像取得 (WIA) 掃描器專案屬性。
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: '掃描器 WIA 專案屬性常數 (Wiadef. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 3202a4ae6bec7808d2d71fe890f248e6b4d3c397
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624764"
---
# <a name="scanner-wia-item-property-constants"></a>掃描器 WIA 專案屬性常數

下列常數會指定一組有效的 Windows 映像取得 (WIA) 掃描器專案屬性。

前置詞 "WIA \_ ip \_ " 表示掃描器裝置的專案屬性，而且是 C/c + + 中使用的命名慣例。 針對腳本用途，這些常數會使用前置詞 "ScannerPicture"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。 來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。



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
<td ><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
<br/> 開啟或關閉自動反扭曲。<br/> 僅限 WIA_CATEGORY_FEEDER 的選擇性。<br/> Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> 下表包含對此屬性有效的常數。 
<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_AUTO_DESKEW_ON</td>
<td>開啟自動反扭曲。</td>
</tr>
<tr class="even">
<td>WIA_AUTO_DESKEW_OFF</td>
<td>關閉自動反扭曲。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </dl></td>
<td ><p>掃描器內可用的影像亮度值。</p>
<p>包含裝置目前的硬體亮度設定。 應用程式會將此屬性設定為硬體的亮度值。 迷你驅動程式會建立並維護此屬性。</p>
<p>值的對應範圍介於-1000 到1000之間，其中1000對應到最大亮度、0對應于標準亮度，而-1000 對應至最小亮度。</p>
<p>類別中所有專案的必要專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。 選擇性，但建議用於支援預覽的 WIA_CATEGORY_FINISHED_FILE 專案。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </dl></td>
<td ><p>包含裝置目前的硬體對比設定。 應用程式會將此屬性設定為硬體的對比值。 迷你驅動程式會建立並維護此屬性。</p>
<p>值的對應範圍介於-1000 到1000之間，其中-1000 對應至最小對比度、0對應至正常對比，而1000對應到最大對比度。</p>
<p>類別中所有專案的必要專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。 選擇性，但建議用於支援預覽的 WIA_CATEGORY_FINISHED_FILE 專案。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </dl></td>
<td ><p>包含目前的意圖設定。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。 WIA_CATEGORY_FINISHED_FILE 或 WIA_CATEGORY_FOLDER 專案不支援此功能。</p>
<p>類型： <strong>VT_I4</strong> 存取：讀取/寫入、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></p>
<p>驅動程式會根據應用程式的預期用途，使用這些專案來設定專案屬性。 例如，這可能包括最高品質、最小大小等等。</p>
<p>驅動程式會選擇位深度（以英寸為單位），而其所決定的其他設定則適用于所選意圖。 應用程式會由應用程式讀取目前的設定，以判斷哪些屬性已變更。 應用程式會設定此屬性，以自動設定特定取得意圖的 WIA 屬性。 所有掃描器都需要這個屬性。</p>
<p>應用程式會設定此屬性，以自動設定特定取得意圖的 WIA 屬性</p>
<div class="alert">
<blockquote>
[!Note]<br />
旗標可以與位 <strong>or</strong> 運算子結合，但影像不能同時為灰階和 color。
</blockquote>
</div>
<div>
 
</div>
<p>所有掃描器都需要這個屬性。</p>
<p>下表包含影像類型旗標及其定義。 這些旗標用來設定要使用的影像類型：色彩、灰階等等。</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>預定的影像類型旗標</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_NONE</td>
<td>預設值。 未指定意圖。</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_COLOR</td>
<td>應用程式打算將裝置準備好進行色彩掃描。</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_GRAYSCALE</td>
<td>應用程式打算將裝置準備好進行灰階掃描。</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_TEXT</td>
<td>應用程式打算準備裝置來掃描文字。</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_MASK</td>
<td>所有影像類型旗標的遮罩。</td>
</tr>
</tbody>
</table>

<p> </p>
<p>下表包含品質和大小旗標及其定義。 這些旗標是用來設定預期的品質等級。</p>

<table>
<thead>
<tr class="header">
<th>預定的影像大小/品質旗標</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_MINIMIZE_SIZE</td>
<td>應用程式會準備裝置來掃描產生的影像，以進行小型掃描。</td>
</tr>
<tr class="even">
<td>WIA_INTENT_MAXIMIZE_QUALITY</td>
<td>應用程式打算準備裝置來掃描高品質的影像。</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_SIZE_MASK</td>
<td>此旗標是所有大小/品質旗標的遮罩。</td>
</tr>
<tr class="even">
<td>WIA_INTENT_BEST_PREVIEW</td>
<td>應用程式打算準備裝置以掃描預覽。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含 x 方向的圖元數，從 WIA_IPS_XPOS 到要 deskewed 之影像最上方角落的 x 座標。 因此，它會結合 WIA_IPS_DESKEW_Y，其中扭曲影像的兩個頂角位於 WIA_IPS_XPOS、WIA_IPS_YPOS、WIA_IPS_XEXTENT 和 WIA_IPS_YEXTENT 所定義的周框中。 如果支援 deskewing，則會由掃描器驅動程式來執行它的屬性。</p>
<p>WIA_IPS_DESKEW_X 的有效值必須介於0到 (WIA_IPS_XEXTENT-1) 之間。 0值表示不應該執行扭曲。</p>
<p>針對 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER 和 WIA_CATEGORY_FILM 類別目錄的專案，這個屬性是選擇性的。而且無法 WIA_CATEGORY_FINISHED_FILE 或 WIA_CATEGORY_FOLDER 專案使用。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含 y 方向的圖元數，從 WIA_IPS_YPOS 到要 deskewed 之影像最左邊角落的 y 座標。 因此，它會結合 WIA_IPS_DESKEW_X，其中扭曲影像的兩個頂角位於 WIA_IPS_XPOS、WIA_IPS_YPOS、WIA_IPS_XEXTENT 和 WIA_IPS_YEXTENT 所定義的周框中。 如果支援 deskewing，則會由掃描器驅動程式來執行這個屬性。</p>
<p>WIA_IPS_DESKEW_Y 的有效值必須介於0到 (WIA_IPS_YEXTENT-1) 之間。 0值表示不應該執行扭曲。</p>
<p>針對 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER 和 WIA_CATEGORY_FILM 類別目錄的專案，這個屬性是選擇性的。而且無法 WIA_CATEGORY_FINISHED_FILE 或 WIA_CATEGORY_FOLDER 專案使用。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含目前的掃描器取得來源和模式。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會讀取此屬性，以判斷掃描器的目前取得來源，或撰寫此屬性來設定掃描器的來源和模式。 此外，應用程式也會使用此屬性來啟用和停用雙面列印程式功能。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>下表包含對此屬性有效的常數。 </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>雙工</td>
<td>使用雙面列印器作業掃描。 使用針對送紙器專案所設定的一般設定來掃描兩個檔側 (WIA_CATEGORY_FEEDER) 。 無法同時設定雙工和 ADVANCE_DUPLEX。</td>
</tr>
<tr class="even">
<td>ADVANCED_DUPLEX</td>
<td>使用為每個子送紙器專案設定的個別設定進行掃描 (WIA_CATEGORY_FEEDER_FRONT 和 WIA_CATEGORY_FEEDER_BACK) 。 無法同時設定雙工和 ADVANCE_DUPLEX。</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>先掃描檔的前方。 當設定了雙工或 ADVANCED_DUPLEX 時，此值有效。</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>先掃描檔的背面。 當設定了雙工或 ADVANCED_DUPLEX 時，此值有效。</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>只掃描前方。</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>只掃描回來。 當設定了雙工或 ADVANCED_DUPLEX 時，此值有效。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>當有一個以上的檔案時，可指定特定電影掃描附件的規格。</p>
<p>當有多個膠捲掃描專案時，WIA_CATEGORY_FILM 專案需要這個屬性。 如果裝置只支援一個根掃描器膠捲專案，則此屬性是選擇性的。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>允許的值： BSTR 的格式應為 @ResourceBinary ， <ResourceID> 以允許當地語系化，因為此字串會透過膠捲掃描 UI 向使用者公開。</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>啟用目前電影掃描的設定。</p>
<p>WIA_CATEGORY_FILM 專案需要這個屬性。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表包含對此屬性有效的常數。 </p>
<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FILM_COLOR_SLIDE</td>
<td>掃描彩色投影片。</td>
</tr>
<tr class="even">
<td>WIA_FILM_COLOR_NEGATIVE</td>
<td>掃描是否有負面的色彩。</td>
</tr>
<tr class="odd">
<td>WIA_FILM_BW_NEGATIVE</td>
<td>掃描黑色和白色的負面。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><p>保留供未來使用，並不會在此時間執行。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定 WIA_CATEGORY_FOLDER 專案中儲存的專案數。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>開啟或關閉掃描器燈。</p>
<p>針對 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER 和 WIA_CATEGORY_FILM 專案為選擇性，並建議用於 WIA_CATEGORY_FILM。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表包含對此屬性有效的常數。 </p>
<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_LAMP_ON</td>
<td>開啟燈泡。</td>
</tr>
<tr class="even">
<td>WIA_LAMP_OFF</td>
<td>關閉燈。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>設定當掃描器未使用時，保持燈的最長時間。</p>
<p>針對 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER 和 WIA_CATEGORY_FILM 專案為選擇性，並建議用於 WIA_CATEGORY_FILM。</p>
<p>類型： <strong>VT_UI4</strong>、存取：讀取/寫入、有效的值： 0-0xFFF 秒</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定目前解析度的水準 (X) 軸中掃描的最大寬度（以英寸為限）。 這可能是工作表輸送或掃描床的寬度（根據專案類型）。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定目前解析度的垂直 (Y) 軸中掃描的最大高度（以英寸為限）。 這可能是工作表輸送或掃描床的高度（根據專案類型而定）。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定目前解析度的水準 (X) 軸掃描的最小寬度（以英寸為限）。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定目前解析度的垂直 (Y) 軸中掃描的最小高度（以英寸為限）。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </dl></td>
<td ><p>保留供未來使用，並不會在此時間執行。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>水準光學解析度。 最高支援的水準光學解析度（DPI）。 這個屬性是單一值。 這不是可由裝置產生的所有解決方案的清單。 相反地，這是裝置光纖的解析度。 迷你驅動程式會建立並維護此屬性。 所有專案都需要這個屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>垂直光學解析度。 支援的最高垂直光學解析度（DPI）。 這個屬性是單一值。 這不是裝置產生的所有解決方案的清單。 相反地，這是裝置光纖的解析度。 迷你驅動程式會建立並維護此屬性。 所有專案都需要這個屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </dl></td>
<td ><p>指定要掃描之檔的目前方向。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會設定此屬性，以定義要取得之頁面或影像的原始方向。 如需如何使用 WIA_IPS_ORIENTATION 的詳細資訊，請參閱 <strong>WIA_IPS_PAGE_SIZE</strong>。</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION 指的是要在掃描器床或輸送器上掃描的檔位置。 這是相對於掃描方向的檔方向。 WIA_IPS_ROTATION 指的是在影像傳送至應用程式之前，在掃描影像之後套用的旋轉。
</blockquote>
</div>
<div>
 
</div>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表包含四個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>肖像</td>
<td>0度。</td>
</tr>
<tr class="even">
<td>景觀</td>
<td>相對於直向的順向計數器旋轉旋轉。90</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>相對於直向的順向計數器旋轉旋轉。180</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>相對於直向的順向計數器旋轉旋轉。270</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含目前已設定要掃描的頁面大小。 應用程式會設定此屬性，以選取要掃描的頁面維度。 迷你驅動程式會建立並維護此屬性。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>如需可搭配這個屬性使用的常數，請參閱 <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2.0 頁面大小常數</strong></a>。 請注意這些非固定大小，特別是： </p>
<table>
<thead>
<tr class="header">
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_CUSTOM</td>
<td>由 <strong>WIA_IPS_PAGE_HEIGHT</strong> 的值和 <strong>WIA_IPS_PAGE_WIDTH</strong> 屬性定義。</td>
</tr>
<tr class="even">
<td>WIA_PAGE_AUTO</td>
<td>裝置會自動決定頁面大小。</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_CUSTOM_BASE</td>
<td>應用程式和設備磁碟機已經知道其維度的自訂頁面大小。</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>WIA_IPS_ORIENTATION</strong>屬性的值會決定目前選取之頁面的方向。 <strong>WIA_IPS_PAGE_WIDTH</strong>和<strong>WIA_IPS_PAGE_HEIGHT</strong>屬性會報告頁面的尺寸（以英寸為限）。 這些屬性必須與 <strong>WIA_IPS_XEXTENT</strong> 和 <strong>WIA_IPS_YEXTENT</strong>一致，其中包含頁面的尺寸（以圖元為單位）。</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_PROP_LIST 類型的有效值取決於 <strong>WIA_IPS_ORIENTATION</strong> 屬性的有效設定。 例如，如果裝置無法使用 WIA_PAGE_A4 設定來掃描橫向導向的檔，當<strong>WIA_IPS_ORIENTATION</strong>設定為 [橫向] 時，WIA_PAGE_A4 不是<strong>WIA_IPS_PAGE_SIZE</strong>屬性的有效值。
</blockquote>
</div>
<div>
 
</div>
<p>如果應用程式將 <strong>WIA_IPS_PAGE_SIZE</strong> 設定為上表中的三個以外的任何值，則迷你驅動程式應該將 <strong>WIA_IPS_PAGE_WIDTH</strong> 的值和 <strong>WIA_IPS_PAGE_HEIGHT</strong> 調整為頁面的尺寸（以英寸為萬分之一）。 它也應該調整 <strong>WIA_IPS_XEXTENT</strong> 的值，並 <strong>WIA_IPS_YEXTENT</strong> 為頁面的尺寸（以圖元為單位）。</p>
<p>如果範圍設定 (<strong>WIA_IPS_XEXTENT</strong> 或 <strong>WIA_IPS_YEXTENT</strong>) 變更為不符合目前 [頁面大小] 設定的值，則迷你驅動程式應該將 [ <strong>WIA_IPS_PAGE_SIZE</strong> ] 屬性的值變更為 [WIA_PAGE_CUSTOM]。 迷你驅動程式也應該根據新的範圍設定來修改 <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> 或 <strong>WIA_IPS_PAGE_HEIGHT</strong> 。</p>
<p>如果 <strong>WIA_IPS_ORIENTATION</strong> 設定為 [橫向]，則會相對於其一般值來交換範圍設定。 例如，如果應用程式將 <strong>WIA_IPS_PAGE_SIZE</strong> 設定為 WIA_PAGE_A4，迷你驅動程式會將 <strong>WIA_IPS_PAGE_WIDTH</strong> 設定為11692，並將 <strong>WIA_IPS_PAGE_HEIGHT</strong> 設定為8267。  (迷你驅動程式也應據以調整 <strong>WIA_IPS_XEXTENT</strong> 和 <strong>WIA_IPS_YEXTENT</strong> 。 ) </p>
<div class="alert">
<blockquote>
[!Note]<br />
如果 <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> 設為 WIA_PAGE_CUSTOM，則不會使用方向設定來決定要掃描之頁面的範圍維度。
</blockquote>
</div>
<div>
 
</div>
<p>迷你驅動程式負責確保 <strong>WIA_IPS_ORIENTATION</strong> 屬性與目前的選取區域一致。 如果應用程式將 <strong>WIA_IPS_ORIENTATION</strong> 的值變更為目前選取之頁面大小不正確值，則迷你驅動程式應該將 <strong>WIA_IPS_PAGE_SIZE</strong> 的值變更為新的方向值所支援的頁面大小。</p>
<p>如果應用程式將 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM，則目前的選取範圍不會受到影響。 WIA 迷你驅動程式應該會從目前的 <strong>WIA_IPS_XPOS</strong> 設定開始，取得目前的影像版面配置，並 <strong>WIA_IPS_YPOS</strong> 屬性。 如果 [頁面大小] 設定產生的選取區域位於掃描器的床之外，則迷你驅動程式必須自動調整 <strong>WIA_IPS_XPOS</strong> 的值，並 <strong>WIA_IPS_YPOS</strong> 屬性設定為有效的設定。 如果 <strong>WIA_IPS_PAGE_SIZE</strong> 和 <strong>WIA_IPS_ORIENTATION</strong> 屬性同時設定，且在組合套用時無效，則迷你驅動程式應該會在 <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv：:d rvvalidateitemproperties</a>中傳回錯誤，以使應用程式的設定失敗。</p>
<p>下列四個範例顯示不同 <strong>WIA_IPS_PAGE_SIZE</strong> 案例。</p>
<ol>
<li>驅動程式會報告設定。</li>
<li>應用程式會將 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_LETTER。</li>
<li>應用程式會將 <strong>WIA_IPS_ORIENTATION</strong> 屬性設定為橫向。</li>
<li>應用程式會將 <strong>WIA_IPS_XEXTENT</strong> 屬性變更為較小的值。</li>
</ol>
<p><strong>範例1：迷你驅動程式報告設定</strong></p>
<p>在下列範例中，迷你驅動程式會在應用程式設定任何 WIA 屬性之前，設定自訂選取區域。 在此情況下，選取區域代表整個平板。</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>範例2：應用程式將</strong> <strong>WIA_IPS_PAGE_SIZE</strong>  <strong>屬性設定為 WIA_PAGE_LETTER</strong></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>範例3：應用程式將</strong> <strong>WIA_IPS_ORIENTATION</strong>  <strong>屬性設定為橫向</strong></p>
<p>實體床必須能夠取得原本處於橫向方向的頁面。</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>範例4：應用程式</strong>將 <strong>WIA_IPS_XEXTENT</strong> <strong>屬性變更為較小的值</strong></p>
<p>在下列範例中，應用程式會將 <strong>WIA_IPS_XEXTENT</strong> 屬性變更為1000。 迷你驅動程式應該假設 <strong>WIA_IPS_XEXTENT</strong> 中包含的新值不再適用于 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性，因此應該將 <strong>WIA_IPS_PAGE_SIZE</strong> 變更為 WIA_PAGE_CUSTOM。 迷你驅動程式也必須調整 <strong>WIA_IPS_PAGE_WIDTH</strong>。</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含目前所選頁面的高度（以英寸為限）。 迷你驅動程式會建立並維護 <strong>WIA_IPS_PAGE_HEIGHT</strong> 屬性。 應用程式會讀取此屬性，以判斷所掃描之頁面的實體維度。 如果範圍設定與已知的頁面大小不同，這個屬性會報告頁面的高度，其 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM (這是 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性) 的值。 <strong>WIA_IPS_PAGE_HEIGHT</strong> 必須與 <strong>WIA_IPS_XEXTENT</strong>同步，以報告要掃描之頁面的高度（以圖元為單位）。</p>
<p>WIA_CATEGORY_FEEDER 專案需要這個屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含目前所選取頁面的寬度（以英寸為限）。 應用程式會讀取此屬性，以判斷所掃描之頁面的實體維度。 如果範圍設定與已知的頁面大小不同，這個屬性會報告頁面的寬度，其 <strong>WIA_IPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM。 <strong>WIA_IPS_PAGE_WIDTH</strong> 必須與 <strong>WIA_IPS_XEXTENT</strong>的值同步，這會報告要掃描頁面的寬度（以圖元為單位）。 迷你驅動程式會建立並維護此屬性。</p>
<p>WIA_CATEGORY_FEEDER 專案需要這個屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含要從自動檔送紙器取得的目前頁面數目。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_I4</strong>;存取：讀取/寫入;有效值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 此值為零，表示掃描器可掃描的最大頁數。 如果掃描器可以連續掃描，則此值為 ALL_PAGES (= 0) 。</p>
<p>應用程式會讀取此屬性，以判斷檔送紙器的頁面容量。 應用程式也會將此屬性設定為要掃描的頁面數目。</p>
<div class="alert">
<blockquote>
[!Note]<br />
如果已啟用雙工模式 (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> 設定為 [送紙器] |雙工 |ADVANCED_DUPLEX) ， <strong>WIA_IPS_PAGES</strong> 仍等於要掃描的頁面數目。
</blockquote>
</div>
<div>
 
</div>
<p>如果已啟用雙工，則會自動包含兩頁的紙張，即使頁面的後端是空白的。</p>
<p>將 <strong>WIA_IPS_PAGES</strong> 設定為1，會導致掃描器處理頁面的一側。 如果掃描器無法在雙工模式下掃描頁面的一端，則建議您將 WIA_PROPERTY_INFO 結構之範圍成員的 Inc 成員 <strong>WIA_IPS_PAGES</strong> 值變更為2。 此值會通知應用程式，它必須以兩個的倍數要求頁面。 值為 ALL_PAGES (= 0) 表示要掃描目前載入檔送紙器中的 <em>所有</em> 頁面。</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </dl></td>
<td ><p>包含白色和黑色圖元的目前設定。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會讀取此值，以根據應用程式的執行) 來判斷白色或黑色 (的值。</p>
<p>所有已啟用或已儲存的專案都需要。也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。 WIA_CATEGORY_FOLDER 專案不支援此功能。</p>
<p>類型： <strong>VT_I4</strong>;存取：讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>。 如果裝置只能設定為單一值，請建立 WIA_PROP_LIST 類型，並在其中放置有效的值。</p>
<p>下表有兩個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PHOTO_WHITE_0</td>
<td>白色為0，黑色為1。</td>
</tr>
<tr class="even">
<td>WIA_PHOTO_WHITE_1</td>
<td>白色為1，黑色為0。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指出裝置的預覽模式。 應用程式會設定此屬性，以將裝置置於預覽模式。</p>
<p>WIA_CATEGORY_FLATBED 和 WIA_CATEGORY_FILM 專案都需要這個屬性，WIA_CATEGORY_FEEDER 專案的選擇性專案。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表包含對此屬性有效的常數。 </p>
<table>
<thead>
<tr class="header">
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FINAL_SCAN</td>
<td>應用程式將會執行最後的掃描。</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>應用程式將會執行預覽掃描。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定是否可以在影像預覽期間更新現有的預覽影像， (以回應 WIA_IPA_DATATYPE 的變更或 WIA_IPA_DEPTH 屬性) 。</p>
<p>對於支援預覽掃描的所有啟用的專案，這個屬性是選擇性的。也就是說，WIA_PREVIEW_SCAN 支援 WIA_IPS_PREVIEW。 這包括類型 WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM 的專案。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表包含對此屬性有效的常數。 </p>
<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ADVANCED_PREVIEW</td>
<td>您可以更新現有的映射。</td>
</tr>
<tr class="even">
<td>WIA_BASIC_PREVIEW</td>
<td>必須執行另一個預覽掃描，因為無法更新現有的映射。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </dl></td>
<td ><p>包含目前的旋轉設定（如果已執行）。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會設定此屬性，以通知驅動程式 (如果所有) 在驅動程式將映射傳回給應用程式之前，都要旋轉映射。</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION 指的是要在掃描器床或輸送器上掃描的檔位置。 這是相對於掃描方向的檔方向。 WIA_IPS_ROTATION 指的是在影像傳送至應用程式之前，在掃描影像之後套用的旋轉。
</blockquote>
</div>
<div>
 
</div>
<p>WIA 迷你驅動程式會負責輪替影像資料，然後再將其傳回給應用程式。 應用程式會負責檢查影像標頭，以查看新旋轉的值。</p>
<p>解決目前影像選取區域的旋轉效果 (（由 <strong>WIA_IPS_XPOS</strong>、 <strong>WIA_IPS_YPOS</strong>、 <strong>WIA_IPS_XEXTENT</strong> 和 <strong>WIA_IPS_YEXTENT</strong> 屬性) 所定義）有相當大的混淆。</p>
<p><em>選取區域</em> 指的是實體掃描器床上要從中取得影像的選取區域。 <strong>WIA_IPS_ROTATION</strong> 不會修改選取區域。 只有在驅動程式取得適當的選取區域之後，驅動程式才會根據 <strong>WIA_IPS_ROTATION</strong> 來套用逆時針旋轉。 <strong>WIA_IPS_ROTATION</strong> 會影響輸出影像的維度，因此這些維度必須反映在產生的影像資料標頭中。</p>
<p>所有已啟用的專案都是選擇性的;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>已定義下列旋轉常數。</p>

<table>
<thead>
<tr class="header">
<th>常數</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>肖像</td>
<td>驅動程式將不會旋轉映射。</td>
</tr>
<tr class="even">
<td>景觀</td>
<td>驅動程式會逆時針旋轉影像90度。</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>驅動程式會逆時針旋轉影像180度。</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>驅動程式會逆時針旋轉影像270度。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定應用程式是否應該使用驅動程式的分割篩選進行多重區域掃描。 如果 WIA_CATEGORY_FLATBED 和 WIA_CATEGORY_FILM 專案支援使用分割篩選來建立子專案，或是驅動程式本身為固定框架建立子專案，則必須為這些專案執行 WIA_IPS_SEGMENTATION。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表有兩個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_USE_SEGMENTATION_FILTER</td>
<td>應用程式應該使用分割篩選進行多重區域掃描。</td>
</tr>
<tr class="even">
<td>WIA_DONT_USE_SEGMENTATION_FILTER</td>
<td>驅動程式會針對多重區域掃描建立子專案本身。 如果掃描器針對此用途使用固定的框架，通常會發生這種情況。</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
驅動程式可能會隨附分割篩選，但仍有 WIA_IPS_SEGMENTATION 設定為其中一個專案的 WIA_DONT_USE_SEGMENTATION_FILTER (例如 WIA_CATEGORY_FILM 專案) 。 如果掃描器使用固定的框架進行膠片掃描，但無法從 WIA_CATEGORY_FLATBED 專案進行一般掃描，就可能會發生這種情況。
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含放置於平板之檔的註冊（或對齊和邊緣偵測）。 迷你驅動程式會建立並維護此屬性。 這個屬性會指出工作表如何水準定位於掌上型或紙匣掃描器的掃描標頭上。 屬性是用來預測檔放置於掃描標頭的哪個位置。</p>
<p>如果掃描器支援一個以上的掃描標頭，這個屬性會相對於最上層的掃描標頭。 這是工作表、捲軸和掌上型掃描器的必要屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表有三個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>工作表在掃描標頭的相對位置。</td>
</tr>
<tr class="even">
<td>中心</td>
<td>工作表會以掃描標頭為中心。</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>工作表位於掃描標頭的右邊。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指出專案是否需要向使用者顯示預覽控制項。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有已啟用傳輸的專案都是選擇性的。 這通常只是類別目錄的專案 WIA_ITEM_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FILM 和 WIA_CATEGORY_FINISHED_FILE。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表包含對此屬性有效的常數。 </p>
<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_SHOW_PREVIEW_CONTROL</td>
<td>顯示使用者的預覽控制項，因為此裝置可以執行預覽。</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>不要向使用者顯示預覽控制項，因為此裝置無法執行預覽。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定應用程式 (或篩選) 是否可以在目前專案下建立子專案。</p>
<p>所有已啟用傳輸專案類別的選擇性： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FILM 甚至 WIA_CATEGORY_FOLDER。  (如果儲存體不支援上傳新的專案，則此屬性應該是不支援或不支援的 <strong>FALSE</strong> 值。 ) </p>
<p>支援 WIA_IPS_SEGMENTATION 和 WIA_USE_SEGMENTATION_FILTER 的專案也必須支援 WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION，並將其設定為 <strong>TRUE</strong>。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <strong>TRUE</strong> 和 <strong>FALSE</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定當影像轉換為單色時，可判斷圖元是否會轉換成白色或黑色的灰階值。 超過閾值的圖元變成白色。 低於閾值的圖元變成白色。</p>
<p>支援 1 bpp 掃描且將 WIA_IPA_DATATYPE 屬性設定為 WIA_DATA_THRESHOLD 的取得專案，需要這個屬性。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定驅動程式是否能夠在單一傳送呼叫中傳送多個子專案。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>這個屬性的唯一可能值是 WIA_TRANSFER_CHILDREN_SINGLE_SCAN。 如果設定此旗標，則驅動程式能夠在單一傳送呼叫中傳輸多個子專案。 如果未設定旗標，則 WIA 服務會以遞迴方式逐一查看子專案，然後傳送每一個專案。</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指定要為專案上傳的位元組數目。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </dl></td>
<td ><p>在開始掃描工作之前，指定裝置所需的最大準備時間（以毫秒為單位）。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式可以讀取此屬性，以判斷此裝置的最大準備時間。 然後，它會顯示 &quot; [正在等待裝置準備 &quot; ] 對話方塊，讓使用者知道等待或暫停可能會在發生任何情況之前發生。</p>
<p>所有取得的已啟用專案都需要這個屬性;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </dl></td>
<td ><p>包含要取得之所選影像的目前寬度（以圖元為單位）。 應用程式會設定這個屬性，將選取區域的寬度標示為取得。 這個屬性必須與 <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> 屬性一致。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </dl></td>
<td ><p>包含所選影像左上角的 x 座標（以圖元為單位）。 應用程式會將這個屬性設定為標示選取區域的左上角。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。 WIA_CATEGORY_FOLDER 專案不支援此功能。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </dl></td>
<td ><p>包含裝置目前的水準解析度（以圖元為單位）。 應用程式會設定這個屬性來設定水準解析度。 迷你驅動程式會建立並維護此屬性。</p>
<p>如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。 這也是一個解決方式設定相依于另一個解決方法的情況。  (垂直解析度可能取決於水準解析度。 ) </p>
<p>所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。 WIA_CATEGORY_FOLDER 專案不支援此功能。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 或 WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>設定可套用至掃描器裝置或其驅動程式內掃描影像的水準縮放（以百分比表示）。</p>
<p>針對所有已啟用的專案，這個屬性是選擇性的;也就是說，WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM 類型的專案。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE。</p>
<p>值可以是1到最大 VT_I4 (0xFFFF) 。 例如，100表示無縮放比例，050表示相應減少為原始大小的50%，而200表示相應減少為原始大小的200%。</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </dl></td>
<td ><p>包含要取得之所選影像的目前高度（以圖元為單位）。 應用程式會將這個屬性設定為標示選取區域的高度。 這個屬性必須與 <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> 屬性的值一致。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </dl></td>
<td ><p>所選影像左上角的目前 y 座標（以圖元為單位）。 應用程式會將這個屬性設定為標示選取區域的左上角。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。 WIA_CATEGORY_FOLDER 專案不支援此功能。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </dl></td>
<td ><p>包含裝置目前的垂直解析度（以圖元為單位）。 應用程式會設定這個屬性來設定垂直解析度。 迷你驅動程式會建立並維護此屬性。</p>
<p>如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。 這也是一個解決方式設定相依于另一個解決方法的情況。  (水準解析度可能取決於垂直解析度。 ) </p>
<p>所有已啟用專案的必要專案;也就是說，類別中的專案： WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK、WIA_CATEGORY_FINISHED_FILE 和 WIA_CATEGORY_FILM。 WIA_CATEGORY_FOLDER 專案不支援此功能。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 或 WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>設定可套用至掃描器裝置或其驅動程式內掃描影像的垂直縮放比例（以百分比表示）。</p>
<p>針對所有已啟用的專案，這個屬性是選擇性的;也就是說，WIA_CATEGORY_FLATBED、WIA_CATEGORY_FEEDER、WIA_CATEGORY_FEEDER_FRONT、WIA_CATEGORY_FEEDER_BACK 和 WIA_CATEGORY_FILM 類型的專案。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 或 WIA_PROP_RANGE。</p>
<p>值可以是1到最大 VT_I4 (0xFFFF) 。 例如，100表示無縮放比例，050表示相應減少為原始大小的50%，而200表示相應減少為原始大小的200%。</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 




