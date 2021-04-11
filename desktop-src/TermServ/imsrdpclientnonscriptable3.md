---
title: IMsRdpClientNonScriptable3 介面
description: 提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 IMsRdpClientNonScriptable2 介面。
ms.assetid: 40cfcd8e-5dd7-497d-8c57-da1f542136b8
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable3 介面遠端桌面服務
- IMsRdpClientNonScriptable3 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c456393ee00c06bcd16135a7fbc73b0f1686259f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934581"
---
# <a name="imsrdpclientnonscriptable3-interface"></a>IMsRdpClientNonScriptable3 介面

提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) 介面。 這個介面的方法只能透過 vtable 存取;它們無法用於可編寫腳本的用戶端。

## <a name="members"></a>成員

**IMsRdpClientNonScriptable3** 介面繼承自 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)。 **IMsRdpClientNonScriptable3** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientNonScriptable3** 介面具有這些屬性。



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
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">要為連接列顯示的文字字串。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br/></td>
<td style="text-align: left;">唯讀<br/></td>
<td style="text-align: left;">可用於重新導向的 PnP 裝置集合。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br/></td>
<td style="text-align: left;">唯讀<br/></td>
<td style="text-align: left;">可用於重新導向的磁片磁碟機集合。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否啟用此連接的 CredSSP。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定此連接是否支援 NegotiateSecurityLayer 設定。<br/>
<blockquote>
[!Note]<br />
當 <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> 已啟用並存在於用戶端上，或當安全通訊端層 (SSL) 啟用使用者驗證時，會忽略 NegotiateSecurityLayer。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否應顯示 [提示輸入認證] 對話方塊。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否可重新導向會話中所列舉的動態連接 PnP 裝置。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定在會話中列舉的動態連接 PnP 磁片磁碟機是否可用於重新導向。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定在啟動會話之前，是否應該顯示重新導向安全性警告對話方塊。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定在啟動會話之前，安全性警告對話方塊是否應包含關於剪貼簿重新導向的警告。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定在啟動會話之前，安全性警告是否應包含有關將認證傳送至遠端伺服器的警告。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient5 定義為4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting 定義為4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 定義為7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting 定義為 D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





