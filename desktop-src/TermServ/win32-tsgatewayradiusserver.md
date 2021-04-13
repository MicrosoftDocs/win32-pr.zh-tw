---
title: Win32_TSGatewayRADIUSServer 類別
description: 描述遠端驗證撥入消費者服務 (RADIUS) 伺服器，其具有一組遠端桌面服務連線授權原則 (RD \ 160;CAPs) 。
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer 類別遠端桌面服務
- Win32_TSGatewayRADIUSServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465088"
---
# <a name="win32_tsgatewayradiusserver-class"></a>Win32 \_ TSGatewayRADIUSServer 類別

描述遠端驗證撥入消費者服務 (RADIUS) 伺服器，其具有一組遠端桌面服務連線授權原則 (RD Cap) 。

RADIUS 是一種業界標準的通訊協定，可用來在伺服器電腦與驗證服務器（稱為 RADIUS 伺服器）之間傳輸驗證、授權和設定資訊，以及儲存使用者資訊的資料庫。 如需詳細資訊，請參閱 [RADIUS 通訊協定](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10))。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a>成員

**Win32 \_ TSGatewayRADIUSServer** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSGatewayRADIUSServer** 類別具有這些方法。



| 方法                                                                 | 描述                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**添加**](win32-tsgatewayradiusserver-add.md)                         | 新增 RADIUS 伺服器。<br/>                                         |
| [**MoveDown**](movedown-win32-tsgatewayradiusserver.md)               | 以優先權順序將此 RADIUS 伺服器向下移動一個位置。<br/> |
| [**上移**](moveup-win32-tsgatewayradiusserver.md)                   | 以優先權順序將此 RADIUS 伺服器往上移動一個位置。<br/>   |
| [**移除**](win32-tsgatewayradiusserver-remove.md)                   | 移除目前的 RADIUS 伺服器。<br/>                                |
| [**SetName**](setname-win32-tsgatewayradiusserver.md)                 | 設定此 RADIUS 伺服器的 **名稱** 屬性。<br/>                |
| [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) | 設定此 RADIUS 伺服器的 **SharedSecret** 屬性。<br/>        |
| [**更新**](update-win32-tsgatewayradiusserver.md)                   | 更新目前的 RADIUS 伺服器。<br/>                                |



 

### <a name="properties"></a>屬性

**Win32 \_ TSGatewayRADIUSServer** 類別具有這些屬性。

<dl> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

RADIUS 伺服器的名稱。 這個屬性可以使用 [**SetName**](setname-win32-tsgatewayradiusserver.md) 方法來變更。

</dd> <dt>

**優先順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RADIUS 伺服器的優先順序。 RD 閘道伺服器會根據優先順序在 RADIUS 伺服器上尋找 RD Cap。 您可以使用 [**上移**](moveup-win32-tsgatewayradiusserver.md)、 [**MoveDown**](movedown-win32-tsgatewayradiusserver.md)、 [**Add**](win32-tsgatewayradiusserver-add.md)和 [**Remove**](win32-tsgatewayradiusserver-remove.md) 方法來變更這個屬性。

</dd> <dt>

**SharedSecret**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RADIUS 伺服器的共用密碼。 這個屬性可以使用 [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) 方法來變更。

</dd> </dl>

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能使用這個類別。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

