---
description: 除非在其描述中另有說明，否則所有 IWiaItem、IWiaItem2 和 IWiaDrvItem 介面介面都必須支援下列裝置屬性常數。
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: '常見的 WIA 專案屬性常數 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967142"
---
# <a name="common-wia-item-property-constants"></a>常見的 WIA 專案屬性常數

除非在其描述中另有說明，否則所有 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)、 [**IWiaItem2**](-wia-iwiaitem2.md) 和 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 介面都必須支援下列裝置屬性常數。

前置詞 "WIA \_ IPA \_ " 表示所有裝置的專案屬性，而且是 C/c + + 中使用的命名慣例。 在撰寫腳本時，這些常數會使用前置詞「圖片」，且是 [WiaItemPropertyId](-wia-wiaitempropertyid.md) 列舉型別的一部分。 來自該腳本列舉的對應成員名稱，會出現在下列清單中 C/c + + 常數名稱旁邊的括弧中。



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
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </dl></td>
<td style="text-align: left;">此旗標會控制專案的存取權，以及是否刪除專案。<br/> 所有 WIA 2.0 專案的必要專案。<br/> 類型： <strong>VT_I4</strong>;[讀取/寫入] 或 [唯讀]，視專案的存取權限變更的能力而定;有效的值： WIA_PROP_FLAG<br/> 下表有五個對此屬性有效的旗標。<br/> 
<table>
<thead>
<tr class="header">
<th>存取權限</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ITEM_READ</td>
<td>專案具有唯讀存取權。</td>
</tr>
<tr class="even">
<td>WIA_ITEM_WRITE</td>
<td>專案具有僅限寫入的存取權。</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_CAN_BE_DELETED</td>
<td>專案具有僅限刪除的存取權。</td>
</tr>
<tr class="even">
<td>WIA_ITEM_RD</td>
<td>WIA_ITEM_READ |WIA_ITEM_CAN_BE_DELETED</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_RWD</td>
<td>WIA_ITEM_READ |WIA_ITEM_WRITE |WIA_ITEM_CAN_BE_DELETED</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </dl></td>
<td style="text-align: left;"><p>這個屬性是保留供日後使用，且目前不會執行。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>包含影像每個通道的位數。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有 WIA 2.0 取得啟用或預存映射專案的必要專案。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>包含資料傳輸期間使用的緩衝區大小（以位元組為單位）。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式可以讀取此屬性，以判斷用於資料傳輸的驅動程式指定緩衝區大小。 WIA 服務也會在資料傳輸期間，讀取此屬性以配置迷你驅動程式的記憶體</p>
<p>所有已啟用轉換的 WIA 2.0 專案都是選擇性的。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
<strong>WIA_IPA_BUFFER_SIZE</strong>屬性包含的是應用程式在任何指定時間可以要求的最小資料量。 緩衝區大小愈大，裝置的要求就會愈大。 這可能使裝置看起來很慢且沒有回應，可能會降低整體系統效能，並且可能耗用過多的資源。 緩衝區大小太小可能會要求許多較小的要求，使資料傳輸的效能變慢。 請考慮您裝置的一般資料要求大小，並根據這些要求的大小來平衡要求數目，以選擇合理的緩衝區大小。
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </dl></td>
<td style="text-align: left;"><p>包含影像的一個掃描行中的位元組數目。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有 WIA 2.0 專案都是選擇性的。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </dl></td>
<td style="text-align: left;"><p>包含影像每圖元的通道數目。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有 WIA 2.0 取得啟用或預存映射專案的必要專案。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </dl></td>
<td style="text-align: left;"><p>這個屬性是保留供日後使用，且目前不會執行。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </dl></td>
<td style="text-align: left;"><p>包含目前使用的壓縮類型。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會讀取這個屬性，以判斷影像壓縮類型，或設定這個屬性來設定壓縮設定。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表包含對此屬性有效的常數。 <strong>V</strong>符號表示只有在 Windows Vista 和更新版本中才支援常數。  (只能透過 <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> 介面使用。 ) </p>

<table>
<thead>
<tr class="header">
<th>[壓縮類型]</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_COMPRESSION_NONE</td>
<td>無壓縮。 如需詳細資訊，請參閱 <strong>備註</strong> 。</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>自動壓縮模式。 如需詳細資訊，請參閱 <strong>備註</strong> 。</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_BI_RLE4</td>
<td>RLE4 壓縮</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_BI_RLE8</td>
<td>RLE8 壓縮</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_G3</td>
<td>群組3壓縮</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_G4</td>
<td>群組4壓縮</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG</td>
<td>JPEG 壓縮。</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_JBIG<strong>V</strong></td>
<td>JBIG 壓縮。</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG2K<strong>V</strong></td>
<td>JPEG 2000 壓縮。</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_PNG<strong>V</strong></td>
<td>PNG 壓縮。</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p>當 WIA_COMPRESSION_NONE 這個屬性時，WIA_IPA_FORMAT 是 WiaImgFmt_PDFA 或 WiaImgFmt_XPS;然後 WIA_COMPRESSION_NONE 表示壓縮模式是未定義的，而且掃描器必須決定模式。</p>
<p>WIA_COMPRESSION_AUTO 是針對 WIA_IPA_COMPRESSION 屬性定義的新屬性值。 此值適用于所有可程式化的影像資料來源專案，包括平板和送紙器。 當 WIA 迷你驅動程式支援這個值時，WIA 應用程式用戶端可以設定 WIA_IPA_COMPRESSION，以便在裝置上啟用自動壓縮模式偵測。 WIA_COMPRESSION_AUTO 可以搭配使用，而且不會支援或啟用完整的自動色彩 (WIA_DATA_AUTO 和 WIA_DEPTH_AUTO) 。</p>
<p>WIA_COMPRESSION_AUTO 最適合用於支援多種資料類型和位深度的傳輸檔案格式，例如 WiaImgFmt_RAW。 如需傳輸檔案格式的詳細資訊，請參閱此表格中的 WIA_IPA_FORMAT。</p>
<p>它的 opitonal 是要讓 WIA 迷你驅動程式支援 WIA_COMPRESSION_AUTO。 當支援時，WIA 迷你驅動程式絕對不能將它設為 WIA_IPA_COMPRESSION 的預設值;只有 WIA 應用程式可以設定此值。</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </dl></td>
<td style="text-align: left;"><p>包含裝置目前的資料類型設定。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會讀取這個屬性，以判斷影像的資料類型。 應用程式會寫入這個屬性，以設定即將傳送之影像的目前資料類型。</p>
<p>所有 WIA 2.0 專案都需要這個屬性。 它必須針對所有啟用 WIA 2.0 的已啟用專案進行讀取/寫入，並唯讀取 WIA 2.0 儲存體專案。</p>
<p>類型： <strong>VT_I4</strong>;Windows Vista 前版作業系統的存取權：此屬性是唯讀的，適用于相機和讀取/寫入掃描器;Windows Vista 和更新版本的存取：此屬性是唯讀的，適用于 WIA_CATEGORY_FOLDER 和 WIA_CATEGORY_FINISHED_FILE 專案，以及所有其他 WIA 2.0 專案類別目錄的讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表具有六個在 <strong>WIA_IPA_FORMAT</strong> 未設定為 WiaImgFmt_RAW 時有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>資料類型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_AUTO</td>
<td>適用于所有可程式化的影像資料來源專案，包括平板和送紙器。 當 WIA 迷你驅動程式支援這個值時，WIA 應用程式用戶端可以設定 WIA_IPA_DATATYPE，以便在裝置上啟用自動色彩偵測。 設定 WIA_DATA_AUTO 時，WIA 迷你驅動程式必須將相同專案上的 WIA_IPA_DEPTH 更新為 WIA_DEPTH_AUTO (如果裝置支援自動色彩) ，則必須是支援的值。<br/> 這是選擇性的值，但 WIA_DEPTH_AUTO 支援 WIA_IPA_DEPTH 時則需要。<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>掃描資料是紅色、綠色、藍色 (RGB) 色彩。 使用下列 WIA 屬性來描述完整色彩格式： <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>與 WIA_DATA_COLOR 相同，不同之處在于資料是使用目前選取的遞色模式進行遞色。</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>與 WIA_DATA_COLOR 相同，不同之處在于掃描資料時使用臨界值。 <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a>值的色彩值會轉換成完整亮度;此值下的色彩會轉換為黑色。</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>掃描資料是使用目前選取的遞色模式進行遞色。</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>掃描資料代表濃度。 此調色板是固定且等距的灰色小數位數，並以 <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> 屬性指定深度。</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>閾值是黑色和白色資料的每個圖元一位。 <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a>的目前值資料會轉換成白色;此值下的資料會轉換為黑色。</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>WIA_IPA_DATATYPE</strong>屬性也用來描述當應用程式設定 WiaImgFmt_RAW 時要使用的原始資料傳輸類型。 驅動程式應該將 <strong>WIA_IPA_DATATYPE</strong> 屬性設定為允許的值清單，讓應用程式可從中挑選一個值。</p>
<p>如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。</p>
<p>檢查 <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> 屬性以判斷位深度。 這個屬性通常會包含相機的單一值。</p>
<p>下表列出<strong>WIA_IPA_FORMAT</strong>設定為 WiaImgFmt_RAW 時，對<strong>WIA_IPA_DATATYPE</strong>有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>資料類型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_GRAYSCALE</td>
<td>掃描資料代表濃度。 此調色板是固定且等距的灰色，以及 <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> 屬性指定的深度。 <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設定為1。</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>掃描資料位於 BGR (藍-綠-red) colorspace。 使用 followingWIAproperties 來描述完整的色彩格式： <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設為3。<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>掃描資料為青色-洋紅-黃色 (CMY) colorspace。 使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。 <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設為3。<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>掃描資料是以青色-洋紅-黃色-黑色 (CMYK) colorspace。 使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。 <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設定為4。<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>掃描資料是以紅色-綠色-藍色 (RGB) colorspace。 使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。 <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設為3。<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>掃描資料的亮度-藍色差異-紅色差異 (YUV) colorspace。 使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。 <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設為3。<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>掃描資料處於 [亮度-藍色差異-紅色差異-黑色] (YUVK) colorspace]。 使用與 WIA_DATA_RAW_BGR 中相同的 WIA 屬性來描述完整的色彩格式。 <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> 必須設定為4。<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </dl></td>
<td style="text-align: left;"><p>WIA_IPA_DEPTH 包含影像的位深度設定。 迷你驅動程式會建立並維護此屬性。應用程式會讀取這個屬性，以判斷影像的位深度設定。 此應用程式也可以將此值設定為所需的位深度。</p>
<p>如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。</p>
<p>所有 WIA 2.0 專案都需要這個屬性。 它必須針對所有啟用 WIA 2.0 的已啟用專案進行讀取/寫入，並唯讀取 WIA 2.0 儲存體專案。</p>
<p>類型： <strong>VT_I4</strong>;Windows Vista 前版作業系統的存取權：讀取/寫入;Windows Vista 和更新版本的存取：此屬性是唯讀的，適用于 WIA_CATEGORY_FOLDER 和 WIA_CATEGORY_FINISHED_FILE 專案，以及所有其他 WIA 2.0 專案類別目錄的讀取/寫入;有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO 定義為每圖元0位，而且是為 WIA_IPA_DEPTH 定義的新屬性值。 此值適用于所有可程式化的影像資料來源專案，包括平板和送紙器。 當 WIA 迷你驅動程式支援 WIA_DEPTH_AUTO 時，WIA 應用程式用戶端可以將 WIA_IPA_DEPTH 設定為此值，以在裝置上啟用自動色彩偵測。 當 WIA_DEPTH_AUTO 設定時，如果裝置支援自動色彩) ，則 WIA 迷你驅動程式必須將相同專案上的 WIA_IPA_DATATYPE 更新為 WIA_DATA_AUTO (必須是支援的值。</p>
<p>WIA_DEPTH_AUTO 是選擇性的值，但是當 WIA_IPA_DATATYPE 支援 WIA_DATA_AUTO 時，就會變成必要值。</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </dl></td>
<td style="text-align: left;"><p>包含特定檔案格式的副檔名。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有已啟用轉換的 WIA 2.0 專案都是選擇性的。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>驅動程式會更新這個屬性，以反映 <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> 屬性的目前值。</p>
<p>例如，如果 WiaImgFmt_JPEG <strong>WIA_IPA_FORMAT</strong> ，則 <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> 應該是 <strong>jpg</strong>。 如果 WiaImgFmt_BMP <strong>WIA_IPA_FORMAT</strong> ，則 WIA_IPA_FILENAME_EXTENSION 應該是 BMP。</p>
<div class="alert">
<blockquote>
[!Note]<br />
副檔名不包含點。
</blockquote>
</div>
<div>
 
</div>
<p>針對支援標準格式的驅動程式，建議使用此屬性，並針對執行自訂定義格式的驅動程式需要此屬性。 它會通知應用程式正確的副檔名，以便在私用格式化的檔案傳送期間使用。 例如，如果 a. Datum Corporation 建立了以新格式傳送檔案的 WIA 驅動程式，該公司就可以指定 adc 的延伸 &quot; &quot; 。 這可讓應用程式將該格式的資料傳輸至檔案，並建立檔案名（例如 <em>myfile.txt</em>），這對其他瞭解新擴充功能的人很有用。</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </dl></td>
<td style="text-align: left;"><p>包含要傳送的目前影像格式。</p>
<p>應用程式會讀取此屬性，以判斷其即將接收的影像格式。 應用程式會寫入這個屬性來設定格式。 這個屬性相依于 <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> 屬性。 迷你驅動程式會建立並維護此屬性。</p>
<p>如果裝置只能設定為單一值，請建立 <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> 類型，並在其中放置有效的值。</p>
<p>類型： <strong>CLSID</strong>，存取：讀取/寫入，有效值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表列出對此屬性有效的常數。 星號 * 表示 Windows Vista 中不支援常數。  (只能透過 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 介面使用。 ) 雙星號 * * 表示 windows Server 2003 或 windows Vista 中不支援該常數。 <strong>V</strong>符號表示只有在 Windows Vista 和更新版本中才支援常數。  (只能透過 <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> 介面使用。 ) </p>

<table>
<thead>
<tr class="header">
<th>格式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaAudFmt_AIFF</td>
<td>.AIFF 音訊格式</td>
</tr>
<tr class="even">
<td>WiaAudFmt_MP3</td>
<td>MP3 音訊格式</td>
</tr>
<tr class="odd">
<td>WiaAudFmt_WAV</td>
<td>WAV 音訊格式</td>
</tr>
<tr class="even">
<td>WiaAudFmt_WMA</td>
<td>WMA 音訊格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_ASF * *</td>
<td>ASF 影片格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI * *</td>
<td>AVI 影片格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>具有標頭檔的 Windows 點陣圖</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF *</td>
<td>相機影像檔案格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>DPOF 列印格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>擴充的 Windows 中繼檔</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXEC</td>
<td>執行檔</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EXIF</td>
<td>交換檔案格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_FLASHPIX</td>
<td>FlashPix 格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_GIF</td>
<td>GIF 影像格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_HTML</td>
<td>HTML 格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows 圖示檔案格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>聯合 Bi 層級影像專家群組 (JBIG) 格式。</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG</td>
<td>JPEG 壓縮格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG2K</td>
<td>JPEG 2000 壓縮格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG2KX</td>
<td>JPEG 2000 壓縮格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MEMORYBMP</td>
<td>沒有標頭檔的 Windows 點陣圖</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>PDF/A (ISO/CD 19005-1) 格式。</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG * *</td>
<td>MPEG 影片格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Eastman Kodak 檔案格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Apple 檔案格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>W3C PNG 格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>僅適用于資料傳輸的 Raw 格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_RAWRGB</td>
<td>Raw RGB 格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RTF</td>
<td>Rich Text 檔案格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_SCRIPT</td>
<td>指令碼檔案</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>TIF 檔案格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_TXT</td>
<td>文字檔</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_UNICODE16</td>
<td>UNICODE 16 位編碼</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows 中繼檔</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_XML</td>
<td>XML 檔</td>
</tr>
<tr class="even">
<td>WiaImgFmt_XPS<strong>V</strong></td>
<td>XPS 封裝格式</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
當這個屬性是 WiaImgFmt_PDFA 或 WiaImgFmt_XPS，而且 WIA_IPA_COMPRESSION 是 WIA_COMPRESSION_NONE 時，接著，第二個值表示壓縮模式是未定義的，而且掃描器必須決定模式。
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </dl></td>
<td style="text-align: left;"><p>包含專案名稱 (的完整專案名稱，以及) 的路徑資訊。 完整專案名稱與<a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a>服務公用程式函數的<em>bstrFullItemName</em>參數相同。 應用程式會讀取這個屬性，以判斷它目前正在使用的專案，以及該專案在專案樹狀結構中的位置。 每個專案都應該要有唯一的名稱。 應用程式通常會使用完整專案名稱來搜尋專案樹狀結構中的專案。 WIA 服務會建立並維護此屬性。</p>
<p>所有 WIA 2.0 專案的必要專案。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </dl></td>
<td style="text-align: left;"><p>這個屬性保留供日後使用，目前不會執行。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </dl></td>
<td style="text-align: left;"><p>包含正確解碼映射所需的 ICM 設定檔名稱。 應用程式會讀取此屬性，以判斷處理映射時所要使用的 ICM 設定檔。 WIA 服務會根據驅動程式安裝檔案中的 ICMProfiles 專案，建立及維護此屬性。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </dl></td>
<td style="text-align: left;"><p>只有在 Windows Vista 和更新版本中才支援。</p>
<p>WIA 2.0 專案會分組為類別，以定義如何處理或使用 <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> 。 例如，如果專案代表送紙器，則應用程式應該會預期它包含所需的檔送紙器屬性，並如同檔輸送器般運作。 如果專案代表已完成的檔案，則 WIA 2.0 應用程式應該以這種方式處理，並假設資料是靜態的，而且位於裝置上。  (每個專案的規則都會在其個別規格檔中定義。 ) </p>
<p>所有 WIA 2.0 專案的必要專案。</p>
<p>類型： <strong>VT_CLSID</strong>、存取：唯讀、有效的值： <a href="-wia-wia2-itemcategoryguids.md"><strong>專案分類 guid</strong></a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </dl></td>
<td style="text-align: left;"><p>包含 WIA 專案的描述性旗標。 專案旗標與<a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a>服務公用程式函式的<em>lObjectFlags</em>參數中的旗標相同。 WIA 服務會建立並維護此屬性。</p>
<p>應用程式會讀取這個屬性，以判斷專案的描述性旗標值。</p>
<p>類型： <strong>VT_I4</strong> 存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表包含對此屬性有效的旗標。 星號 * 表示 Windows Vista 或更新版本中不支援此旗標。  (只能透過 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 介面使用。 ) 雙星號 * * 表示 windows Server 2003 或 windows Vista 或更新版本不支援此旗標。 <strong>V</strong>符號表示只有在 Windows Vista 和更新版本中才支援旗標。  (只能透過 <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> 介面使用。 ) </p>

<table>
<thead>
<tr class="header">
<th>旗標</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaItemTypeAnalyze*</td>
<td>此專案支援 <strong>IWiaItem：： AnalyzeItem</strong> 方法 () 的 Platform SDK 檔中所述。 此專案也支援自動產生子專案。 這項功能適用于區域偵測或分頁分解。</td>
</tr>
<tr class="even">
<td>WiaItemTypeAudio</td>
<td>此專案支援音訊。 此旗標只適用于也已設定 <strong>WiaItemTypeFile</strong> 旗標的專案。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeBurst*</td>
<td>僅適用于資料夾。 此旗標表示此資料夾中的影像是以連續時間順序拍攝。</td>
</tr>
<tr class="even">
<td>WiaItemTypeDeleted</td>
<td>此專案已標示為要刪除、此專案已被刪除、此專案不存在，或此專案的內容無效。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDocument<strong>V</strong></td>
<td>此專案是 <strong>WIA_IPA_FORMAT</strong> 屬性包含的其中一種檔案格式的檔檔。  (這些格式包括 nonimage 檔案的格式，例如 .txt、.htm 和 .doc 檔案。 ) </td>
</tr>
<tr class="even">
<td>WiaItemTypeDevice</td>
<td>此專案代表連線的裝置。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDisconnected</td>
<td>此專案代表已中斷連線的裝置。</td>
</tr>
<tr class="even">
<td>WiaItemTypeFile</td>
<td>專案支援檔案傳輸。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeFolder</td>
<td>專案是資料夾。</td>
</tr>
<tr class="even">
<td>WiaItemTypeFree</td>
<td>專案未初始化或已刪除。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeGenerated</td>
<td>此專案是由應用程式或驅動程式所產生。</td>
</tr>
<tr class="even">
<td>WiaItemTypeHasAttachments*</td>
<td>此專案支援附件，且目前包含附件。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeHPanorama*</td>
<td>此專案代表水準全景影像。 此旗標只適用于也已設定 <strong>WiaItemTypeFolder</strong> 旗標的專案。</td>
</tr>
<tr class="even">
<td>WiaItemTypeImage</td>
<td>專案是影像檔案。 此旗標只適用于也已設定 <strong>WiaItemTypeFile</strong> 旗標的專案。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeProgrammableDataSource<strong>V</strong></td>
<td>此專案是可程式化的資料來源，並遵循一組預先定義的設定規則，這些規則是以 <strong>WIA_IPA_ITEM_CATEGORY</strong>為基礎。</td>
</tr>
<tr class="even">
<td>WiaItemTypeRoot<strong>V</strong></td>
<td>此專案是根項目，也就是裝置支援的所有功能專案的父系。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeStorage</td>
<td>此旗標表示資料夾專案的額外儲存空間。 WIA 驅動程式會根據影像和資料夾來指定其專案。 沒有任何 WIA 屬性描述儲存專案的特性 (例如剩餘的儲存空間、寫入速度或媒體類型。 您可以新增可公開此資訊的廠商特定屬性。 這些屬性只能存取為了辨識這些屬性而撰寫的應用程式或延伸模組。</td>
</tr>
<tr class="even">
<td>WiaItemTypeTransfer</td>
<td>這個專案可以用來傳輸資料。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeTwainCapabilityPassThrough</td>
<td>這種類型表示 WIA 裝置能夠接收來自 TWAIN 相容性層的 TWAIN 功能資料。 如果設定此型別，則 TWAIN 相容性層所不了解的任何 TWAIN 功能都會傳遞至 theWIA 驅動程式。 這僅適用于根項目。</td>
</tr>
<tr class="even">
<td>WiaItemTypeVideo**</td>
<td>此專案支援串流處理影片。</td>
</tr>
<tr class="odd">
<td>WiaItemTypeVPanorama*</td>
<td>此專案代表垂直全景影像。 此旗標只適用于也已設定 <strong>WiaItemTypeFolder</strong> 旗標的專案。</td>
</tr>
</tbody>
</table>

<p> </p>
<p>根據專案的類別，這些旗標中有些旗標是必要或選擇性2.0 的，如下表所示。</p>

<table>
<thead>
<tr class="header">
<th>專案類別</th>
<th>必要</th>
<th>選用</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_ROOT</td>
<td>WiaItemTypeRoot WiaItemTypeFolder</td>
<td>WiaItemTypeDevice WiaItemTypeDisconnected</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FLATBED</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (如果支援多個掃描區域專案，此旗標只適用于 WIA_CATEGORY_FLATBED 根專案。 ) </td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (如果 WIA_CATEGORY_FEEDER_FRONT 和 WIA_CATEGORY_FEEDER_BACK 專案都存在，則此旗標只適用于 WIA_CATEGORY_FEEDER 根專案。 ) </td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (根) </td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</td>
<td>無</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (子系) </td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>無</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FOLDER</td>
<td>WiaItemTypeStorage WiaItemTypeFolder</td>
<td>WiaItemTypeDeleted</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td>WiaItemTypeFile WiaItemTypeTransfer</td>
<td>WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </dl></td>
<td style="text-align: left;"><p>包含專案名稱。 應用程式會讀取此屬性，以判斷其目前使用的專案。 每個專案都有唯一的名稱。 WIA 服務會建立並維護此屬性。</p>
<p>所有 WIA 2.0 專案的必要專案。</p>
<p>類型： <strong>VT_BSTR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </dl></td>
<td style="text-align: left;"><p>包含與專案相關聯之資料的目前大小（以位元組為單位）。 迷你驅動程式會建立並維護此屬性。</p>
<p>[包含] 是要傳輸的資料大小總計。 如果此值為零，則表示迷你驅動程式沒有資料確切大小的相關資訊。  (這常見於壓縮的資料。 ) 應用程式會讀取此值，以在發生之前判斷取得的大小。 WIA 服務會讀取此屬性，以協助配置記憶體以進行資料傳輸。 如需詳細資訊，請參閱將 <a href="https://msdn.microsoft.com/library/ms792198.aspx">資料傳送至 WIA 應用程式</a> 。如果屬性設為零，且 TYMED 設定為檔案傳輸，則 wia 服務不會配置任何記憶體給 wia 迷你驅動程式。</p>
<p>所有已啟用轉換的 WIA 2.0 專案都需要。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </dl></td>
<td style="text-align: left;"><p>包含最初捕獲映射的時間。 迷你驅動程式會建立並維護此屬性。 這個屬性應該以 SYSTEMTIME 結構的形式回報為八個 <strong>單字</strong> 值的向量 (如 Platform SDK 檔) 中所述。</p>
<p>所有 WIA 2.0 專案都是選擇性的。</p>
<p>類型： <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>存取：讀取/寫入或唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </dl></td>
<td style="text-align: left;"><p>只有在 Windows Vista 和更新版本中才支援。</p>
<p>指定 WIA_CATEGORY_FOLDER 專案中儲存的專案數。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>指定資料傳輸中使用的最小緩衝區大小。 如果資料傳輸是透過回呼機制來執行，屬性值可以小到64KB。 但是，如果傳送至檔案，屬性值就是一次傳輸一個資料頁面所需的位元組數目。 迷你驅動程式會建立並維護此 WIA 屬性。</p>
<p>所有已啟用轉換的 WIA 2.0 專案都是選擇性的。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </dl></td>
<td style="text-align: left;"><p>包含影像中所含的行數 (影像的垂直高度（以圖元為單位）) 。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有 WIA 2.0 專案都是選擇性的。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </dl></td>
<td style="text-align: left;"><p>包含影像中每一行的圖元數 (影像的寬度（以圖元為單位）) 。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有 WIA 2.0 專案都是選擇性的。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </dl></td>
<td style="text-align: left;"><p>Windows Vista 和更新版本不支援此屬性。</p>
<p>包含影像資料封裝選項。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會讀取這個屬性，以判斷影像封裝選項，或設定目前的影像封裝選項。</p>
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
<td>WIA_PACKED_PIXEL</td>
<td>影像資料採用壓縮的像素格式。</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>影像資料是平面格式。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </dl></td>
<td style="text-align: left;"><p>包含此迷你驅動程式所傳送影像的慣用格式。 迷你驅動程式會建立並維護此屬性。</p>
<p>所有已啟用轉換的 WIA 2.0 專案都需要。</p>
<p>類型： <strong>CLSID</strong>、Access：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </dl></td>
<td style="text-align: left;"><p>指定代表一組裝置屬性值的 CLSID。 如果設備磁碟機會執行這項功能，應用程式會使用這個屬性來判斷裝置是否支援一組值。</p>
<p>類型： <strong>CLSID</strong>、Access：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表具有12個對此屬性有效的常數。</p>

<table>
<thead>
<tr class="header">
<th>值</th>
<th>定義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>具有標頭檔的 MicrosoftWindows 點陣圖</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>擴充的 Windows 中繼檔</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXIF</td>
<td>交換檔案格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_FLASHPIX</td>
<td>FlashPix 格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_GIF</td>
<td>GIF 影像格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows 圖示檔案格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>JPEG 壓縮格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Eastman Kodak 檔案格式</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>W3C PNG 格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>沒有標頭檔的 Windows 點陣圖</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>TIF 檔案格式</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows 中繼檔</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>只有在 Windows Vista 和更新版本中才支援。</p>
<p>包含每個通道中的位數。 這個屬性應該回報為多個位元組值的向量（如同通道的數目），其中第一個位元組會對應到第一個通道中的位數，第二個位元組會對應到第二個通道中的位數，依此類推。 根據 WIA_IPA_CHANNELS_PER_PIXEL，每個頻道都必須有任意數量的專案。 當應用程式切換為 WiaImgFmt_RAW 時，驅動程式會設定該屬性。 針對已知的子類型，WIA_IPA_RAW_SUBTYPE 的表格中所列的專案數目如下。</p>
<p>類型： <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </dl></td>
<td style="text-align: left;"><p>這個屬性是保留供日後使用，且目前不會執行。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </dl></td>
<td style="text-align: left;"><p>指定是否要隱藏裝置上專案的一般屬性頁。</p>
<p>這個屬性可在 Windows XP 和更新版本上使用。</p>
<p>類型： <strong>VT_I4</strong>、存取：唯讀、有效的值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>下表包含對此屬性有效的常數。 星號 * 表示常數在 Windows Vista 和更新版本中是不正確。  (只能透過 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 介面使用。 ) </p>

<table>
<thead>
<tr class="header">
<th>常數</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL *</td>
<td>隱藏相機的一般專案屬性頁。</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>隱藏掃描器的一般專案屬性頁。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </dl></td>
<td style="text-align: left;"><p>此屬性包含傳送方法設定。 迷你驅動程式會建立並維護此屬性。</p>
<p>應用程式會讀取這個屬性，以判斷迷你驅動程式的資料傳輸方法。</p>
<p>所有已啟用轉換的 WIA 2.0 專案都需要。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>下表包含對此屬性有效的常數。 星號 * 表示在 Windows Vista 和更新版本中不正確常數。  (只能透過 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 介面使用。 ) </p>

<table>
<thead>
<tr class="header">
<th>類型中的來源</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK *</td>
<td>將影像傳送至記憶體（以群組區）。</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK *</td>
<td>將多個映射傳送至記憶體（以群組區為限）。</td>
</tr>
<tr class="odd">
<td>TYMED_FILE</td>
<td>將影像傳送至檔案。</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_FILE</td>
<td>將影像傳送至檔案。</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </dl></td>
<td style="text-align: left;"><p>只有在 Windows Vista 和更新版本中才支援。</p>
<p>指定要為專案上傳的位元組數目。</p>
<p>Type： <strong>VT_I4</strong>、Access： Read/Write、Valid 值： <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 




