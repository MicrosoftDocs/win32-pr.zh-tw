---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別
description: 描述 (RD \ 160; 的遠端桌面資源授權原則。RAP) 。 RD \ 160;RAP 用來決定是否授權使用者透過遠端桌面閘道 (RD 閘道) 連接到指定的資源。
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9748ddc4feccd504d823025ea70877004417717d625c904ccae4445f05e6eb03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999818"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>Win32 \_ TSGatewayResourceAuthorizationPolicy 類別

描述 (RD RAP) 的遠端桌面資源授權原則。 RD RAP 用來決定是否授權使用者透過遠端桌面閘道 (RD 閘道) 連接到指定的資源。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a>成員

**Win32 \_ TSGatewayResourceAuthorizationPolicy** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSGatewayResourceAuthorizationPolicy** 類別具有這些方法。



| 方法                                                                                          | 描述                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | 將指定的使用者組名加入至 **UserGroupNames** 屬性中的現有使用者群組。<br/>      |
| [**建立**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | 建立 RD RAP。<br/>                                                                                       |
| [**刪除**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | 刪除目前的 RD RAP。<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | 從 **UserGroupNames** 屬性中的現有使用者群組中移除指定的使用者組名。<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | 設定 RD RAP 的 **Description** 屬性。<br/>                                                        |
| [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | 藉由設定 **Enabled** 屬性來啟用或停用 RD RAP。<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | 設定 RD RAP 的 **名稱** 屬性。<br/>                                                               |
| [**SetPortNumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | 設定 RD RAP 的 **PortNumbers** 屬性。<br/>                                                        |
| [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | 設定 **ResourceGroupType** 和 **ResourceGroupName** 屬性。<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | 設定 RD RAP 的 **UserGroupNames** 屬性。<br/>                                                     |
| [**更新**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | 更新目前的 RD RAP。<br/>                                                                              |



 

### <a name="properties"></a>屬性

**Win32 \_ TSGatewayResourceAuthorizationPolicy** 類別具有這些屬性。

<dl> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD RAP 的描述。 這個屬性會以 [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否已啟用此 RD RAP。 這個屬性會以 [**SetEnabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

RD RAP 的名稱。 這個屬性會以 [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。

</dd> <dt>

**PortNumbers**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此原則允許的分號分隔通訊埠編號清單。 若要允許任何埠號碼，請設定 " \* "。

</dd> <dt>

**ProtocolNames**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

針對此原則啟用之以分號分隔的通訊協定名稱清單。 名稱必須符合 [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)類別的 [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)方法傳回。

</dd> <dt>

**resourceGroupName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源群組名稱。 這個屬性會以 [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別資源群組的類型。 這個屬性會以 [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) 方法變更。

<dt>

RG
</dt> <dd>

資源群組。

</dd> <dt>

CG
</dt> <dd>

電腦群組，儲存在 Active Directory Domain Services 中。

</dd> <dt>

ALL
</dt> <dd>

所有資源。

</dd> </dl>

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以分號分隔的使用者組名清單。 如果使用者隸屬于這些使用者群組中的任何一項，則會允許存取。 這個屬性會隨著 [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)、 [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)和 [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) 方法而變更。

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

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

