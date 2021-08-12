---
title: IMsTscAdvancedSettings 介面
description: 包含取得和設定屬性的方法，這些屬性可啟用點陣圖快取、壓縮和印表機和剪貼簿重新導向。
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- IMsTscAdvancedSettings 介面遠端桌面服務
- IMsTscAdvancedSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f1156f59178275ff9406299fc553afacd3ce99a0488497f836d147ec1d63547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606195"
---
# <a name="imstscadvancedsettings-interface"></a>IMsTscAdvancedSettings 介面

包含取得和設定屬性的方法，這些屬性可啟用點陣圖快取、壓縮和印表機和剪貼簿重新導向。 您也可以指定虛擬通道用戶端 Dll 的名稱。

您可以使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得這個介面的實例。

## <a name="members"></a>成員

**IMsTscAdvancedSettings** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IMsTscAdvancedSettings** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsTscAdvancedSettings** 介面具有這些屬性。



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
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否啟用背景輸入模式。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否啟用點陣圖快取。<br/>
<blockquote>
[!Note]<br />
屬性名稱中的拼寫錯誤是在控制項的發行版本中。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-compress.md"><strong>壓縮</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否啟用壓縮。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否啟用容器處理的全螢幕模式。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">指定是否啟用印表機和剪貼簿重新導向。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a><br/></td>
<td style="text-align: left;">唯寫<br/></td>
<td style="text-align: left;">指定檔案的名稱，這個檔案包含在全螢幕模式中顯示用戶端時，將會存取的圖示資料。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconindex.md"><strong>>iconindex</strong></a><br/></td>
<td style="text-align: left;">唯寫<br/></td>
<td style="text-align: left;">指定目前圖示檔中的圖示索引。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a><br/></td>
<td style="text-align: left;">唯寫<br/></td>
<td style="text-align: left;">指定使用中輸入地區設定識別碼的名稱 (先前稱為用於連接的鍵盤配置) 。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a><br/></td>
<td style="text-align: left;">唯寫<br/></td>
<td style="text-align: left;">指定要載入的虛擬通道用戶端 Dll 的名稱。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings 定義為809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

