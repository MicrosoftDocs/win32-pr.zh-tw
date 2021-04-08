---
description: 下列常數形成一組有效的 Windows 映像取得 (WIA) 硬體裝置命令。
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: 'WIA 裝置命令 (Wiadef .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848065"
---
# <a name="wia-device-commands"></a>WIA 裝置命令

下列常數形成一組有效的 Windows 映像取得 (WIA) 硬體裝置命令。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">常數</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </dl></td>
<td style="text-align: left;">使裝置的迷你驅動程式與硬體裝置同步處理快取的專案。 如果裝置支援 <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem：： AnalyzeItem</strong></a> 方法，發出此命令會導致迷你驅動程式捨棄分析結果，並將專案重設為其初始狀態。 所有驅動程式都必須支援此命令。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </dl></td>
<td style="text-align: left;">導致 WIA 裝置取得映射。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </dl></td>
<td style="text-align: left;">告知裝置刪除所有可從代表裝置之 <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> 物件的樹狀結構中刪除的專案。 藉由設定專案的屬性，即可防止刪除專案。 如需詳細資訊，請參閱 <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage：： SetPropertyStream</strong></a> 和 <a href="-wia-property-attributes.md">屬性屬性</a>。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">用於檔掃描器。 使掃描器在其檔處理常式中載入下一個頁面。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">用於檔掃描器。 告知裝置卸載其檔處理常式中所有剩餘的頁面。 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <dt><strong>WIA_CMD_START_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">用於具有頁面送紙器的檔掃描器。 告知裝置啟動送紙器馬達。 從 Windows 8 開始，可以使用這項功能。<br/>
<blockquote>
[!Note]<br />
當<a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a>屬性不受支援，或設定為 WIA_FEEDER_CONTROL_AUTO 時，WIA 迷你驅動程式必須拒絕這個命令，並傳回<strong>WIA_ERROR_INVALID_COMMAND</strong> 。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">用於具有頁面送紙器的檔掃描器。 告知裝置停止送紙器馬達。 從 Windows 8 開始，可以使用這項功能。<br/>
<blockquote>
[!Note]<br />
當<strong>WIA_IPS_FEEDER_CONTROL</strong>屬性不受支援，或設定為 WIA_FEEDER_CONTROL_AUTO 時，WIA 迷你驅動程式必須拒絕這個命令，並傳回<strong>WIA_ERROR_INVALID_COMMAND</strong> 。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">用於具有頁面送紙器的檔掃描器。 告知裝置暫停送紙器馬達。 從 Windows 8 開始，可以使用這項功能。<br/>
<blockquote>
[!Note]<br />
當<strong>WIA_IPS_FEEDER_CONTROL</strong>屬性不受支援，或設定為 WIA_FEEDER_CONTROL_AUTO 時，WIA 迷你驅動程式必須拒絕這個命令，並傳回<strong>WIA_ERROR_INVALID_COMMAND</strong> 。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wiadef。h</dt> </dl> |



 

 
