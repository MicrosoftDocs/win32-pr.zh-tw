---
title: Win32_TSGatewayResourceGroup 類別
description: 描述資源群組，這會將一組資源 (電腦名稱稱) 對應至單一實體。
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup 類別遠端桌面服務
- Win32_TSGatewayResourceGroup 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965713"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>Win32 \_ TSGatewayResourceGroup 類別

描述資源群組，這會將一組資源 (電腦名稱稱) 對應至單一實體。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a>成員

**Win32 \_ TSGatewayResourceGroup** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSGatewayResourceGroup** 類別具有這些方法。



| 方法                                                                  | 描述                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)       | 將資源新增至此資源群組的 **資源** 屬性。<br/>      |
| [**建立**](create-win32-tsgatewayresourcegroup.md)                   | 建立資源群組。<br/>                                                  |
| [**刪除**](delete-win32-tsgatewayresourcegroup.md)                   | 刪除此資源群組。<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | 從資源屬性中刪除此資源群組 **的資源。**<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | 設定此資源群組的 **Description** 屬性。<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | 設定此資源群組的 **名稱** 屬性。<br/>                        |
| [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)       | 設定此資源群組的 **資源** 屬性。<br/>                   |
| [**更新**](update-win32-tsgatewayresourcegroup.md)                   | 更新此資源群組。<br/>                                               |



 

### <a name="properties"></a>屬性

**Win32 \_ TSGatewayResourceGroup** 類別具有這些屬性。

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與此資源群組相關聯 (RD Rap) 的遠端桌面服務資源授權原則清單（以分號分隔）。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資源群組的描述。 這個屬性可以使用 [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) 方法來變更。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

資源群組的名稱。 這個屬性可以使用 [**SetName**](setname-win32-tsgatewayresourcegroup.md) 方法來變更。

</dd> <dt>

**資源**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此資源群組中的資源清單（以分號分隔）。 「」 \* 表示所有資源。 您可以使用 [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)、 [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)、 [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)和 [**Update**](update-win32-tsgatewayresourcegroup.md) 方法來變更這個屬性。

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

