---
title: IMsRdpClientAdvancedSettings5 介面
description: 管理 advanced client 設定。 衍生自 IMsRdpClientAdvancedSettings4 介面。
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966502"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a>IMsRdpClientAdvancedSettings5 介面

管理 advanced client 設定。 衍生自 [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) 介面。

若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。 然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings5** 傳遞給 **QueryInterface**。

## <a name="members"></a>成員

**IMsRdpClientAdvancedSettings5** 介面繼承自 [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)。 **IMsRdpClientAdvancedSettings5** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientAdvancedSettings5** 介面具有這些屬性。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">屬性</th>
<th style="text-align: left;">存取類型</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">音訊重新導向模式。 <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a>屬性具有下列可能的值。<br/>
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (已啟用音訊重新導向，而重新導向的選項會 &quot; 帶至此電腦 &quot; 。 這是預設模式。 ) <br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (已啟用音訊重新導向，且 [遠端電腦] 選項為 [ &quot; 離開] &quot; 。 &quot; &quot; 只有在遠端連線到執行 Windows Vista 的主機電腦時，才支援 [離開遠端電腦] 選項。 如果連接到執行 Windows Server 2008 的主機電腦，則 [ &quot; 遠端電腦離開] 選項 &quot; 會變更為 [ &quot; 不播放] &quot; 。 ) <br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (已啟用音訊重新導向，且 &quot; 不播放模式 &quot; 。 ) <br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定每圖元32位的虛擬快取檔案大小 (bpp) 點陣圖。 最大值為 48 mb (MB) 。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否應該在連接列上顯示 [釘選] 按鈕。 依預設，此值為 <strong>TRUE</strong>。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否應啟用或停用公用模式。 Public 模式預設會設定為 <strong>FALSE</strong>。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否應啟用或停用剪貼簿重新導向。 根據預設，剪貼簿重新導向模式會設定為 <strong>TRUE</strong> (已啟用) 。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否應啟用或停用重新導向的裝置。 根據預設，重新導向的裝置模式會設定為 <strong>FALSE</strong>。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否應啟用或停用服務重新導向裝置的點。 依預設，[服務重新導向裝置的時間點] 模式會設定為 [ <strong>FALSE</strong>]。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

