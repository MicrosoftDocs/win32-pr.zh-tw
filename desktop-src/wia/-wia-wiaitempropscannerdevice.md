---
description: Windows 映像取得 (WIA) 硬體裝置具有儲存在 Windows 登錄中的屬性值。
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: '掃描器裝置屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971005"
---
# <a name="scanner-device-property-constants"></a>掃描器裝置屬性常數

Windows 映像取得 (WIA) 硬體裝置具有儲存在 Windows 登錄中的屬性值。 如需詳細資訊，請參閱 [**一般裝置屬性常數**](-wia-wiaitempropcommondevice.md)。 下列裝置屬性常數（與其相關聯的字串）是數位影像掃描器的特定常數。

前置詞 "WIA \_ DPS \_ " 表示掃描器裝置的裝置屬性，而且是 C/c + + 中使用的命名慣例。 針對腳本用途，這些常數會使用前置詞 "ScannerDevice"，而且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。 來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。



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
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
只有在 Windows Vista 和更新版本上才支援此屬性。
</blockquote>
<br/> 包含 web 服務掃描器裝置的唯一函數實例識別碼。 此識別碼代表 WIA 迷你驅動程式用來進行通訊的掃描器裝置上的 web 服務。 這項識別碼的表單不應進行任何假設。 WIA 迷你驅動程式會建立並維護此屬性。 <br/> WIA 應用程式可使用「函式探索 API」這項 WIA_DPS_DEVICE_ID 的值，來尋找目前 WIA 2.0 會話中使用的 web 服務掃描器裝置的函式實例物件。<br/> 類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td style="text-align: left;">保留，請勿使用。<br/> 類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;">保留，請勿使用。<br/> 類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td style="text-align: left;">包含掃描器的功能。 迷你驅動程式會建立並維護此屬性。 <br/> 應用程式會讀取此屬性，以判斷掃描器是否已安裝平板、檔輸送器或雙面列印器。 這個屬性也可用來進一步定義已安裝的功能。<br/> 類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> 下表說明僅適用于 Windows 7 的常數。<br/> 
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AUTO_SOURCE</td>
<td>掃描器已安裝自動檔處理常式。</td>
</tr>
</tbody>
</table>

<p> </p>
<p>下表說明僅適用于 Windows 7 和 Windows Vista 的常數。</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ADVANCED_DUP</td>
<td>裝置支援 advanced 雙工掃描設定。 使用 WIA_IPS_DUPLEX_SETTINGS 在使用基本和先進雙工設定之間切換。</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>掃描器可以偵測透明/膠捲介面卡何時可以進行掃描。</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>掃描器可以偵測到內部儲存體中有檔時。</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>掃描器配備了透明/膠捲掃描介面卡。</td>
</tr>
<tr class="odd">
<td>STOR</td>
<td>掃描器配備了內部影像儲存裝置。</td>
</tr>
</tbody>
</table>

<p> </p>
<p>下表描述的是 Windows XP 或更新版本中有效的常數。</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_FEED</td>
<td>掃描器可以偵測到送紙器中的檔。</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>掃描器可以偵測到平板玻璃上的檔。</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>掃描器只能透過掃描來偵測送紙器中的檔。</td>
</tr>
<tr class="even">
<td>多重</td>
<td>掃描器有雙面列印器。</td>
</tr>
<tr class="odd">
<td>飼料</td>
<td>掃描器已安裝自動檔處理常式。</td>
</tr>
<tr class="even">
<td>平</td>
<td>掃描器有平板玻璃。</td>
</tr>
</tbody>
</table>

<p> </p>
<p>下表說明僅適用于 Windows XP 的常數。 這些值在 Windows 7 和 Windows Vista 中已被取代，不應該使用。</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_DUP</td>
<td>掃描器可以偵測到使用者的雙工掃描要求。</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>掃描器可以分辨是否已安裝雙面列印程式。</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>掃描器可以分辨自動檔送紙器的安裝時間。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>包含目前的掃描器取得來源和模式。迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會讀取此屬性，以判斷掃描器的目前取得來源，或撰寫此屬性來設定掃描器的來源和模式。 此外，應用程式也會使用此屬性來啟用和停用雙面列印程式功能。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>下表包含以這個屬性為有效的十個常數。 </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>饋線</td>
<td>使用檔送紙器進行掃描。</td>
</tr>
<tr class="even">
<td>平板</td>
<td>使用平板的掃描。</td>
</tr>
<tr class="odd">
<td>雙工</td>
<td>使用雙面列印器作業掃描。</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>在掃描之後啟用下一份檔的自動饋送。</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>先掃描檔的前方。 當設定雙工時，此值有效。</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>先掃描檔的背面。 當設定雙工時，此值有效。</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>只掃描前方。 當設定雙工時，此值有效。</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>只掃描回來。 當設定雙工時，此值有效。</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>掃描檔的下一頁。</td>
</tr>
<tr class="even">
<td>PREFEED</td>
<td>啟用進紙前模式。 掃描時預先定位下一個檔。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td style="text-align: left;"><p>包含掃描器安裝的平板、檔輸送器或雙面列印器的目前狀態。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會讀取此屬性，以判斷掃描器裝置是否已準備好可供使用。 在取得影像之前，這是檢查紙紙是否在紙器中的理想方式。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表包含對此屬性有效的常數。星號 * 表示 Windows Vista 或更新版本中不支援此旗標。 <strong>V</strong>符號表示只有在 Windows Vista 和更新版本中才支援旗標。 </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEED_READY</td>
<td>平板可供使用。</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>掃描器在平板玻璃上有一份檔。</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>自動列印器已啟用且可供使用。</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>平坦的床朝上。</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>涵蓋的是檔路徑，並導致無法正常運作。</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>檔送紙器中的檔已卡住。</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>已安裝並準備好使用「透明度介面卡」。</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>內部儲存體裝置已準備就緒。</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>儲存體已滿，無法進行上傳作業。</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>發生多個摘要條件 (通常會有 PAPER_JAM) 。</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>發生錯誤，需要使用者在裝置上介入。</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>掃描器未就緒，因為發生燈泡問題。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td style="text-align: left;"><p>包含應用程式可用於建立有效 endorser 字串的所有有效字元。 Endorser 是安裝在掃描器上的印表機，可在每個掃描的頁面上 imprints 文字訊息。 迷你驅動程式應該針對這個屬性中的有效字元集驗證 <strong>WIA_DPS_ENDORSER_STRING</strong> 屬性的設定。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td style="text-align: left;"><p>包含要背書的字串 (換句話說，在迷你驅動程式掃描的每個頁面上列印) 。 應用程式會使用 <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> 屬性中所報告的有效字元集來設定這個屬性。 只有在這個屬性中設定了字串時，迷你驅動程式才會將檔背書。 空字串表示 endorser 功能已停用。</p>
<p>因為驅動程式必須負責解讀 endorser 字串，所以您的驅動程式可以在 <strong>WIA_DPS_ENDORSER_STRING</strong>中使用特殊字元。 不過，只有您的應用程式會瞭解這些字元。</p>
<p>Type： <strong>VT_BSTR</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>支援 <strong>WIA_DPS_ENDORSER_STRING</strong> 屬性的驅動程式必須支援下列權杖清單。 </p>
<table>
<thead>
<tr class="header">
<th>Token</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE $</td>
<td>格式為 YYYY/MM/DD 的日期。</td>
</tr>
<tr class="even">
<td>$DAY $</td>
<td>以 DD 形式的日。</td>
</tr>
<tr class="odd">
<td>$MONTH $</td>
<td>年份的月份，格式為 MM。</td>
</tr>
<tr class="even">
<td>$PAGE _COUNT $</td>
<td>傳送的頁面數目。</td>
</tr>
<tr class="odd">
<td>$TIME $</td>
<td>一天中的時間，格式為 HH： MM： SS。</td>
</tr>
<tr class="even">
<td>$YEAR $</td>
<td>YYYY 格式的年份。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;"><p>保留，請勿使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
只有在 Windows Vista 和更新版本上才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含 web 服務掃描器裝置的 SOAP 位址。 WIA 2.0 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含放置於平板之檔的註冊或水準對齊。 迷你驅動程式會建立並維護此屬性。</p>
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
<td>這份檔會保持整齊。</td>
</tr>
<tr class="even">
<td>中心</td>
<td>這份檔是中心的。</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>紙張靠右對齊。</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>另請參閱</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>指定在水準 (X) 軸掃描的最大寬度（以英寸為限），從平台掃描器的滾筒到目前的解析度。 這個屬性也適用于將工作表移至平台掃描器的影印以進行掃描的自動檔送紙程式。 具有玻璃的掃描器必須有這個屬性。 其他掃描器類型會改為執行 <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> 屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>指定從掌上 (X) 軸掃描的最大寬度（以英寸為限），以目前解析度的掌上型或紙紙掃描器進行掃描。 這個屬性也適用于自動檔的自動檔，不需要將工作表移至平台掃描器的滾筒就能進行掃描。 這是工作表、捲軸和手入掃描器的必要屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td style="text-align: left;"><p>包含使用目前的屬性設定掃描單一頁面的最長時間（以毫秒為單位）。 應用程式會讀取此屬性，以估計掃描頁面所需的時間。 這在判斷已停止回應之裝置的條件時很有説明。 迷你驅動程式會建立並維護此屬性。 所有掃描器都需要這個屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>包含掃描器檔送紙器可掃描之最小頁面的實體水準維度（以英寸為限）。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>另請參閱</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>包含掃描器檔送紙器可掃描之最小頁面的實體垂直尺寸（以英寸為限）。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>另請參閱</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 不支援這個屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>水準光學解析度。 最高支援的水準光學解析度（DPI）。 這個屬性是單一值。 這不是可由裝置產生的所有解決方案的清單。 相反地，這是裝置光纖的解析度。 迷你驅動程式會建立並維護此屬性。 所有掃描器都需要這個屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 不支援這個屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>垂直光學解析度。 支援的最高垂直光學解析度（DPI）。 這個屬性是單一值。 這不是裝置產生的所有解決方案的清單。 相反地，這是裝置光纖的解析度。 迷你驅動程式會建立並維護此屬性。 所有掃描器都需要這個屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td style="text-align: left;"><p>包含目前的方向設定。迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會設定 <strong>WIA_DPS_ORIENTATION</strong> 屬性，以定義要取得之頁面或影像的原始方向。 如需如何使用 WIA_DPS_ORIENTATION 的詳細資訊，請參閱 <strong>WIA_DPS_PAGE_SIZE</strong></p>
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
<td>景觀</td>
<td>相對於直向的順向計數器旋轉旋轉。90</td>
</tr>
<tr class="even">
<td>肖像</td>
<td>0度。</td>
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

<p> </p>
<p><strong>另請參閱</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td style="text-align: left;"><p>當沒有足夠的影像資料來填滿要求的緩衝區時，用來填補的色彩。 這個屬性是針對填補緩衝區的掃描器所執行。 所有掃描器的這個屬性是選擇性的。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>色彩資訊的格式為 <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>。</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 不支援這個屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>包含目前所選頁面的高度（以英寸為限）。 迷你驅動程式會建立並維護 <strong>WIA_DPS_PAGE_HEIGHT</strong> 屬性。 應用程式會讀取此屬性，以判斷所掃描之頁面的實體維度。 如果範圍設定與已知的頁面大小不同，這個屬性會報告頁面的高度，其 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM (這是 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性) 的值。 <strong>WIA_DPS_PAGE_HEIGHT</strong> 必須與 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>同步，以報告要掃描之頁面的高度（以圖元為單位）。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 不支援這個屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>包含目前已選取要掃描的頁面大小。 若要選取要掃描的頁面維度，應用程式會設定此屬性。 迷你驅動程式會建立並維護此屬性。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表有三個對此屬性有效的常數。 </p>
<table>
<thead>
<tr class="header">
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_A4</td>
<td>8267 X 11692 (縱向方向) </td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>由 <strong>WIA_DPS_PAGE_HEIGHT</strong> 的值和 <strong>WIA_DPS_PAGE_WIDTH</strong> 屬性定義</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (縱向方向) </td>
</tr>
</tbody>
</table>

<p> </p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>屬性的值會決定目前選取之頁面的方向。 <strong>WIA_DPS_PAGE_WIDTH</strong>和<strong>WIA_DPS_PAGE_HEIGHT</strong>屬性會報告頁面的尺寸（以英寸為限）。 請注意，這些屬性必須與 <strong>WIA_IPS_XEXTENT</strong> 和 <strong>WIA_IPS_YEXTENT</strong>一致，其中包含頁面的尺寸（以圖元為單位）。 WIA_PROP_LIST 類型的有效值應取決於 <strong>WIA_IPS_ORIENTATION</strong> 屬性的有效設定。 如果裝置無法使用 WIA_PAGE_A4 設定來掃描橫向導向的檔，當<strong>WIA_IPS_ORIENTATION</strong>設為 LANSCAPE 時，WIA_PAGE_A4 不應該出現在<strong>WIA_DPS_PAGE_SIZE</strong>屬性的有效值清單中。</p>
<p>如果應用程式將 <strong>WIA_DPS_PAGE_SIZE</strong> 設定為 WIA_PAGE_CUSTOM 以外的任何值，則迷你驅動程式應該調整 <strong>WIA_DPS_PAGE_WIDTH</strong> 的值，並 <strong>WIA_DPS_PAGE_HEIGHT</strong> 為頁面的尺寸（以英寸為萬分之一）。 它也應該調整 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> 的值，並 <strong>WIA_IPS_YEXTENT</strong> 為頁面的尺寸（以圖元為單位）。</p>
<p>如果範圍設定 (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> 或 <strong>WIA_IPS_YEXTENT</strong>) 變更為不符合目前頁面大小設定的值，則迷你驅動程式應該將 [ <strong>WIA_DPS_PAGE_SIZE</strong> ] 屬性的值變更為 [WIA_PAGE_CUSTOM]。 迷你驅動程式也應該根據新的範圍設定來修改 <strong>WIA_DPS_PAGE_WIDTH</strong> 或 <strong>WIA_DPS_PAGE_HEIGHT</strong> 。</p>
<p>如果 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> 設定為 LANSCAPE，則會翻轉範圍設定 &quot; 。 &quot; 例如，如果應用程式將 <strong>WIA_DPS_PAGE_SIZE</strong> 設定為 WIA_PAGE_A4，迷你驅動程式應該將 <strong>WIA_DPS_PAGE_WIDTH</strong> 設定為11692，並將 <strong>WIA_DPS_PAGE_HEIGHT</strong> 設定為8267。  (迷你驅動程式也應該設定 <strong>WIA_IPS_XEXTENT</strong> ，並據此 <strong>WIA_IPS_YEXTENT</strong> 。 ) 請注意，如果 <strong>WIA_DPS_PAGE_SIZE</strong> 設定為 WIA_PAGE_CUSTOM，則方向設定不會用來判斷要掃描之頁面的範圍維度。</p>
<p>迷你驅動程式負責確保 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> 屬性與目前的選取區域一致。 如果應用程式將 <strong>WIA_IPS_ORIENTATION</strong> 的值變更為目前選取之頁面大小不正確值，則迷你驅動程式應該將 <strong>WIA_DPS_PAGE_SIZE</strong> 的值變更為新的方向值所支援的頁面大小。</p>
<p>如果應用程式將 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM，則目前的選取範圍不會受到影響。 WIA 迷你驅動程式應該會從目前的 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> 設定開始，取得目前的影像版面配置，並 <strong>WIA_IPS_YPOS</strong> 屬性。 如果頁面大小設定產生掃描器外的選取區域，則迷你驅動程式必須自動調整 <strong>WIA_IPS_XPOS</strong> 的值，並 <strong>WIA_IPS_YPOS</strong> 屬性設定為有效的設定。 如果 <strong>WIA_DPS_PAGE_SIZE</strong> 和 <strong>WIA_IPS_ORIENTATION</strong> 屬性同時設定，且在組合套用時無效，則迷你驅動程式應該會在 <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv：:d rvvalidateitemproperties</a>中傳回錯誤，以使應用程式的設定失敗。 .</p>
<p>下列四個範例顯示不同 <strong>WIA_DPS_PAGE_SIZE</strong> 案例。</p>
<ol>
<li>驅動程式會報告設定。</li>
<li>應用程式會將 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_LETTER。</li>
<li>應用程式會將 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> 屬性設定為 LANSCAPE。</li>
<li>應用程式會將 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> 屬性變更為較小的值。</li>
</ol>
<p><strong>範例1：迷你驅動程式報告設定</strong></p>
<p>在下列範例中，迷你驅動程式會在應用程式設定任何 WIA 屬性之前，設定自訂選取區域。 在此情況下，選取區域代表整個平板。</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
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
<p><strong>範例2：應用程式將</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>屬性設定為 WIA_PAGE_LETTER</strong></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
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
<p><strong>範例3：應用程式將</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>屬性設定為 LANSCAPE</strong></p>
<p>實體床必須能夠取得原本處於橫向方向的頁面。</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<p><strong>範例4：應用程式</strong>將 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>屬性變更為較小的值</strong></p>
<p>在下列範例中，應用程式會將 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> 屬性變更為1000。 迷你驅動程式應該假設 <strong>WIA_IPS_XEXTENT</strong> 中包含的新值不再適用于 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性，因此應該將 <strong>WIA_DPS_PAGE_SIZE</strong> 變更為 WIA_PAGE_CUSTOM。 迷你驅動程式也必須調整 <strong>WIA_DPS_PAGE_WIDTH</strong>。</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 不支援這個屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>包含目前所選取頁面的寬度（以英寸為限）。 應用程式會讀取此屬性，以判斷所掃描之頁面的實體維度。 如果範圍設定與已知的頁面大小不同，這個屬性會報告頁面的寬度，其 <strong>WIA_DPS_PAGE_SIZE</strong> 屬性設定為 WIA_PAGE_CUSTOM。 <strong>WIA_DPS_PAGE_WIDTH</strong> 必須與 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>的值同步，這會報告要掃描頁面的寬度（以圖元為單位）。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 不支援這個屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>包含要從自動檔送紙器取得的目前頁面數目。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_I4</strong>;存取：讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (零到檔送紙器可以容納的最大頁面數目) </p>
<p>應用程式會讀取此屬性，以判斷檔送紙器的頁面容量。 應用程式也會將此屬性設定為要掃描的頁面數目。</p>
<div class="alert">
<blockquote>
[!Note]<br />
如果已啟用雙工模式 (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> 設定為 [送紙器] |雙工 ) ， <strong>WIA_DPS_PAGES</strong> 仍等於要掃描的頁面數目。
</blockquote>
</div>
<div>
 
</div>
<p>如果已啟用雙工，則會自動包含兩頁的紙張，即使頁面的後端是空白的。</p>
<p>將 <strong>WIA_DPS_PAGES</strong> 設定為1，會導致掃描器處理頁面的其中一個邊。 如果掃描器在雙工模式下無法僅掃描頁面的一端，則應該將 WIA_PROPERTY_INFO 結構的 Inc 成員 <strong>WIA_DPS_PAGES</strong> 有效值變更為2。 此值會通知應用程式，它必須以兩個的倍數要求頁面。 值為零表示要掃描目前載入檔送紙器中的 <em>所有</em> 頁面。</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td style="text-align: left;"><p>指定要掃描的工作表背面的影印色彩。 對於具有玻璃的掃描器，這個屬性是選擇性的。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>色彩資訊的格式為 <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>。</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 不支援這個屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>指出裝置的預覽模式。 應用程式會設定此屬性，以將裝置置於預覽模式。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表有兩個對此屬性有效的常數。 </p>
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
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td style="text-align: left;"><p>包含值，指出掃描器在將頁面傳送至應用程式之前，是否會在掃描器緩衝區中快取頁面。</p>
<p>值為0會停用事先掃描，而且不會事先掃描任何頁面。 在經過緩衝處理的掃描專案上進行一般資料傳輸，會抓取緩衝的頁面。 在提前掃描工作期間，無法變更 WIA 屬性。 這是選用屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值：從零到檔送紙器可以容納的最大頁面數目的 <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 。</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows 7 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>指出輸入來源 (平板、自動檔送紙器或 fil 掃描介面卡) 進行掃描，或要從中傳送資料的儲存位置。</p>
<p>掃描事件會通知應用程式使用者已啟動掃描，但該事件未提供代表輸入來源之 WIA 專案的名稱。 應用程式的事件處理常式可以查詢根專案的 WIA_DPS_SCAN_AVAILABLE_ITEM 屬性，以取得輸入來源專案的名稱。</p>
<p>類型： <strong>VT_I4</strong>、存取：讀取/寫入、有效的值：從零到檔送紙器可以容納的最大頁面數目的 <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 。</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含 Web 服務掃描器裝置的服務識別碼。 WIA 2.0 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>。
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
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 不支援這個屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>指出專案是否需要向使用者顯示預覽控制項。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表有兩個對此屬性有效的常數。 </p>
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
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
只有 Windows Vista 和更新版本才支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>由 WIA 服務用來通知迷你驅動程式有關使用者帳戶名稱 (包括目前 WIA 應用程式執行所在會話的可用) 的網路功能變數名稱。</p>
<p>這是由 WIA 服務管理的根專案屬性。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。
</blockquote>
</div>
<div>
 
</div>
<p>包含放置於平板之檔的註冊或垂直對齊和邊緣偵測。 迷你驅動程式會建立並維護此屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表有三個對此屬性有效的常數。 </p>
<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TOP_JUSTIFIED</td>
<td>這份白皮書最重要。</td>
</tr>
<tr class="even">
<td>中心</td>
<td>這份檔是中心的。</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>這份白皮書靠下對齊。</td>
</tr>
</tbody>
</table>

<p> </p>
<p>另<strong>請參閱</strong>。</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>指定在垂直 (Y) 軸中掃描的最大高度（以英寸為限），從平台掃描器的滾筒到目前的解析度。 這個屬性也適用于自動檔送紙程式，可將工作表移至平台掃描器的影印以進行掃描。 具有玻璃的掃描器必須有這個屬性。 其他掃描器類型會改為執行 <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> 屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Windows Vista 和更新版本不支援此屬性。 使用 <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>。
</blockquote>
</div>
<div>
 
</div>
<p>指定在垂直 (Y) 軸的最大高度（以英寸為間隔），從掌上型或工作表饋送掃描器以目前的解析度掃描。 這個屬性也適用于自動檔的自動檔，不需要將工作表移至平台掃描器的滾筒就能進行掃描。 這是工作表饋送掃描器的必要屬性。 滾動饋送和掌上型掃描器不應執行此屬性。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 
