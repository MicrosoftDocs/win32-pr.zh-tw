---
title: IMsRdpClient7 介面
description: 提供設定和使用用戶端控制項所需的方法和屬性。 衍生自 IMsRdpClient6 介面。
ms.assetid: f6bc5d50-f16a-44be-8244-5aec13c52066
ms.tgt_platform: multiple
keywords:
- IMsRdpClient7 介面遠端桌面服務
- IMsRdpClient7 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClient7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1cdd90e9e05a0220fffa2646ae31cf652bb232283b0dec9c908202f38f950f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990528"
---
# <a name="imsrdpclient7-interface"></a>IMsRdpClient7 介面

提供設定和使用用戶端控制項所需的方法和屬性。 衍生自 [**IMsRdpClient6**](imsrdpclient6.md) 介面。

## <a name="members"></a>成員

**IMsRdpClient7** 介面繼承自 [**IMsRdpClient6**](imsrdpclient6.md)。 **IMsRdpClient7** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IMsRdpClient7** 介面具有這些方法。



| 方法                                               | 描述                                                         |
|:-----------------------------------------------------|:--------------------------------------------------------------------|
| [**GetStatusText**](imsrdpclient7-getstatustext.md) | 抓取指定狀態碼的狀態文字。<br/> |



 

### <a name="properties"></a>屬性

**IMsRdpClient7** 介面具有這些屬性。



| 屬性                                                                  | 存取類型          | Description                                                                                                                |
|:--------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>   | 唯讀<br/> | 支援 [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) 介面的物件。<br/>   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>         | 唯讀<br/> | 支援 [**ITSRemoteProgram2**](itsremoteprogram2.md) 介面的物件。<br/>                           |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>     | 唯讀<br/> | 支援 [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) 介面的物件。<br/>     |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/> | 唯讀<br/> | 支援 [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) 介面的物件。<br/> |



 

## <a name="remarks"></a>備註

下列介面已擴充 **IMsRdpClient7** 介面，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient7 定義為 b2a5b5ce-3461-444a-91d4-add26d070638<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





