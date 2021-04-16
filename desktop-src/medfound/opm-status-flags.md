---
description: 下表中的旗標會指定輸出保護管理員 (OPM) 會話的狀態。
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: 'OPM 狀態旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512576"
---
# <a name="opm-status-flags"></a>OPM 狀態旗標

下表中的旗標會指定輸出保護管理員 (OPM) 會話的狀態。



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
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </dl></td>
<td style="text-align: left;">一般狀態。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </dl></td>
<td style="text-align: left;">連接的完整性已遭入侵。 導致驅動程式設定此旗標的事件範例包括：<br/>
<ul>
<li>驅動程式無法再強制執行目前的保護層級。</li>
<li>驅動程式偵測到內部完整性錯誤。</li>
<li>電腦與顯示裝置之間的連接器已插上。</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </dl></td>
<td style="text-align: left;">連接設定已變更。 例如，使用者已變更桌面顯示模式。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </dl></td>
<td style="text-align: left;">圖形介面卡或驅動程式已遭篡改。<br/> <em>COPP 模擬模式</em>不會使用此旗標。 相反地，如果偵測到篡改，影片輸出會設定 OPM_STATUS_LINK_LOST 旗標。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </dl></td>
<td style="text-align: left;">已撤銷的 High-Bandwidth 數位內容保護 (HDCP) 裝置會附加至影片輸出。<br/> 您可以從 <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> 或 <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> 查詢傳回此狀態旗標。 <br/> 撤銷的裝置可能會直接附加至影片輸出，或間接透過 HDCP 中繼器。 必須要有影片輸出，才能在 HDCP 啟用時偵測這種情況，但不能使用其他方式。<br/> <em>COPP 模擬模式</em>不會使用此旗標，因為影片輸出不會偵測到處于該模式的已撤銷裝置。<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>備註

其中一些常數相當於 **COPP \_ StatusFlags** 列舉中的值，這些值是在認證的輸出保護通訊協定 (COPP) 中使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 列舉](opm-enumerations.md)
</dt> </dl>

 

 




