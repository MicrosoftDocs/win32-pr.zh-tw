---
description: 下表列出封包屬性結構所使用的封包屬性 Guid \_ 。
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: PacketProperty Guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb7db9f2d5e05000bdccd5a09b2b799f38aa1bb692fea110ea153a57912cfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449368"
---
# <a name="packetproperty-guids"></a>PacketProperty Guid

下表列出封 [**包 \_ 屬性**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) 結構所使用的封包屬性 guid。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GUID_ALTITUDE_ORIENTATION<br/></td>
<td>畫筆軸和平板電腦表面之間的角度。 當畫筆平行至介面時，此值為0，當畫筆垂直至表面時，則為90。 當畫筆反轉時，值為負數。<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>透過完整的圓形範圍，在 Z 軸上順時針旋轉游標。<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>當辨識器以 box 模式操作時，用來取得筆跡辨識替代方塊的 GUID。<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>壓力相關按鈕的壓力。<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>PacketProperty 物件的 GUID，表示與 tablet 介面垂直的鋼筆提示壓力。 畫筆秘訣的壓力愈大，繪製的筆墨越多。<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>包含下列一或多個旗標值：<br/>
<ul>
<li>游標觸及繪圖介面 (Value = 1) 。</li>
<li>資料指標反轉。 例如，畫筆的橡皮擦末端指向介面 (值 = 2) 。</li>
<li>未使用 (值 = 4) 。</li>
<li>已按下 [圓筒] 按鈕 (值 = 8) 。</li>
</ul></td>
</tr>
<tr class="odd">
<td>GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br/></td>
<td>封包的裝置連絡人識別碼。<br/></td>
</tr>
<tr class="even">
<td>GUID_SERIAL_NUMBER<br/></td>
<td>識別封包。 這是您用來從封包佇列取出封包的相同值。<br/></td>
</tr>
<tr class="odd">
<td>GUID_TANGENT_PRESSURE<br/></td>
<td>PacketProperty 物件的 GUID，這個物件表示沿著 tablet 介面平面之畫筆提示的壓力。<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>產生封包的時間。<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>以順時針旋轉其本身軸的游標。<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>Tablet 座標空間中的 x 座標。 依預設，每個封包都包含這個屬性。 平板電腦的原點 (0、0) 是左上角。<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>若為畫筆游標，x 傾斜方向是 y、z 平面和畫筆和 y 軸平面之間的角度。 當畫筆垂直至繪圖介面時，此值為0，而當畫筆位於垂直右方時為正數。<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>Tablet 座標空間中的 y 座標。 依預設，每個封包都包含這個屬性。 平板電腦的原點 (0、0) 是左上角。<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>若為畫筆游標，y 傾斜方向是 x、z 平面和畫筆和 X 軸平面之間的角度。 當畫筆垂直至繪圖介面時，此值為0，當畫筆向上或遠離使用者時，此值為正數。<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>Tablet 介面中畫筆提示的 z 座標或距離。 <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a>列舉型別會決定這個屬性的度量單位。 <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> TangentPressure 欄位代表 tablet 表面平面的壓力;NormalPressure 欄位代表與 tablet 表面平面垂直的壓力。

 

 

 




