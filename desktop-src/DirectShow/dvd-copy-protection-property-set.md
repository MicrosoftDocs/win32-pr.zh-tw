---
description: DVD 禁止複製屬性集提供從硬體或軟體 decrypters 禁止複製資訊的驗證。 使用這個屬性集，以防止未經授權的 DVD 影片複製。
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: DVD 複製保護屬性集 (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909476"
---
# <a name="dvd-copy-protection-property-set"></a>DVD 禁止複製屬性集

DVD 禁止複製屬性集提供從硬體或軟體 decrypters 禁止複製資訊的驗證。 使用這個屬性集，以防止未經授權的 DVD 影片複製。

Microsoft 提供的軟體可協助加密配置所需的驗證程式，因此可讓 DVD-ROM 光碟機以 DVD decrypter 來驗證和傳輸金鑰。 Microsoft 目前沒有計劃寄送 DVD decrypter，而是提供作業系統程式碼，作為代理程式來啟用硬體或軟體 decrypters 的驗證。

DVD 導覽器會初始化並控制金鑰交換程式。 DVD 迷你驅動程式只需要執行下列屬性。 其他元件則會處理其餘部分。

每個 DVD 輸入串流都會接收禁止複製屬性。 即使相同硬體控制所有 DVD 串流，也是如此。

下列資訊提供在呼叫 [**IKsPropertySet**](ikspropertyset.md) 方法時，要用於此屬性集的必要常數和資料類型。 它會提供 **GUID** (*GuidPropSet*) 、屬性識別碼 (*dwPropID*) 和屬性資料類型的值， (*pPropData*) 參數。



| 標籤 | 值 |
|-------------------|---------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ CopyProt |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性識別碼</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></td>
<td>查詢影片輸出是否為標準定義、類比元件影片。</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_COPY_MACROVISION</td>
<td>這是僅限設定的屬性。 這個屬性會在接收 pin 的輸出結尾設定 NTSC 編碼器的類比禁止複製層級。 使用 <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>。</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_CHLG_KEY</td>
<td>這個屬性支援 get 和 set 作業。 Get 作業會要求解碼器提供其匯流排挑戰金鑰。 設定作業會提供具有來自 DVD 光碟機之匯流排挑戰金鑰的解碼器。 在這個屬性中傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>類型的結構。</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DEC_KEY2</td>
<td>這是僅供取得的屬性。 這個屬性會要求將解碼器的匯流排金鑰2傳輸到 DVD 光碟機。 傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>類型的結構。</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_DISC_KEY</td>
<td>僅限設定的屬性。 這會提供光碟機碼。 索引鍵是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>類型的結構。</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DVD_KEY1</td>
<td>這是僅限設定的屬性。 這個屬性會將 DVD 磁片磁碟機匯流排金鑰1提供給解碼器。 傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>類型的結構。</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_REGION</td>
<td>區域程式碼會要求使用此解碼器的區域定義，如 DVD 協會所定義。 此區域定義為 <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> 結構。</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_SET_COPY_STATE</td>
<td>Get 和 set 都支援此屬性。 首先會呼叫 Get，以判斷是否需要驗證。 設定的屬性會指出篩選所輸入的禁止複製協調階段。 傳遞的資料將會是 <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>類型的結構。</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</td>
<td>如果這個屬性為 <strong>TRUE</strong>，則在協商光碟機碼之前，DVD 導覽器不會傳送 <strong>AM_UseNewCSSKey</strong> 範例。 請參閱 <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>。<br/> 唯讀。 屬性資料是 <strong>布林</strong> 值。<br/>
<blockquote>
[!Note]<br />
適用于 Windows 7。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_TITLE_KEY</td>
<td>這是僅限設定的屬性。 這會從目前內容提供標題索引鍵。 索引鍵是 <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>類型的結構。</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 




