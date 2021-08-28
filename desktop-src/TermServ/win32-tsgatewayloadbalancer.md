---
title: Win32_TSGatewayLoadBalancer 類別
description: 描述一組遠端桌面閘道 (RD 閘道) 負載平衡伺服器。 這些是用來在多部伺服器之間 RD 閘道連接之間進行負載平衡。
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer 類別遠端桌面服務
- Win32_TSGatewayLoadBalancer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584077911faf8593e7c26aadd36ca17a0a11d82b18d1d6ade20be1f1444fedf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769868"
---
# <a name="win32_tsgatewayloadbalancer-class"></a>Win32 \_ TSGatewayLoadBalancer 類別

描述一組遠端桌面閘道 (RD 閘道) 負載平衡伺服器。 這些是用來在多部伺服器之間 RD 閘道連接之間進行負載平衡。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a>成員

**Win32 \_ TSGatewayLoadBalancer** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSGatewayLoadBalancer** 類別具有這些方法。



| 方法                                                                             | 描述                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**AddServers**](addservers-win32-tsgatewayloadbalancer.md)                       | 將伺服器新增至 [ **伺服器** ] 屬性。<br/>                                                             |
| [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md)           | 刪除參與負載平衡伺服器陣列的所有 RD 閘道負載平衡伺服器。<br/>               |
| [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)                 | 從 **伺服器** 屬性刪除伺服器。<br/>                                                        |
| [**IsLoadBalancingServer**](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | 判斷伺服器是否可以執行負載平衡。<br/>                                             |
| [**SetServers**](setservers-win32-tsgatewayloadbalancer.md)                       | 以分號分隔的 RD 閘道負載平衡伺服器清單來設定 **伺服器** 屬性。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ TSGatewayLoadBalancer** 類別具有這些屬性。

<dl> <dt>

**伺服器**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

RD 閘道的負載平衡伺服器清單（以分號分隔）。 您可以使用 [**SetServers**](setservers-win32-tsgatewayloadbalancer.md)、 [**AddServers**](addservers-win32-tsgatewayloadbalancer.md)、 [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)和 [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) 方法來變更這個屬性。

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

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

