---
title: 'WINBIO_BIOMETRIC_SUBTYPE 常數 (Winbio \_ 類型 .h) '
description: 提供生物特徵辨識測量的相關資訊。
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e6dc285e1a19fab8e0363391fbd81429e931cd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630837"
---
# <a name="winbio_biometric_subtype-constants"></a>WINBIO \_ 生物特徵辨識 \_ 子類型常數

**WINBIO \_所有 Windows 生物特徵辨識架構都會使用生物特徵 \_ 子類型** 常數，以提供生物特徵辨識測量的其他相關資訊。 當不需要任何子類型或需要任何子型別時，可以使用下列常數。



| 常數/值                                                                                                                                                                                                                                                            | 描述                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_子類型 \_ 沒有 \_ 資訊**</dt> <dt>0x00</dt> </dl> | 沒有子類型資訊。<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_子類型 \_ 任何**</dt> <dt>0xff</dt> </dl>                                   | 任何子型別。<br/>            |



## <a name="remarks"></a>備註

若要尋找特定生物特徵辨識類型的可用生物特徵辨識子類型，請使用下表：



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><strong>WINBIO_BIOMETRIC_TYPE</strong> 值</th>
<th>主題 (s) 尋找 <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> 值</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE 常數</strong></a>
<blockquote>
[!Note]<br />
這些值僅適用于 Windows 10 和更新版本。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_FINGERPRINT</strong></td>
<td>下列其中一個主題：
<ul>
<li><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT 常數</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG 常數</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ 常數</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE 常數</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS 常數</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS 指紋常數</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm 常數</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS 常數</strong></a>
<blockquote>
[!Note]<br />
這些值僅適用于 Windows 10 和更新版本。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE 常數</strong></a>
<blockquote>
[!Note]<br />
這些值僅適用于 Windows 10 和更新版本。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

如需詳細資訊，請參閱 [用戶端應用程式常數](client-application-constants.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



 

 





