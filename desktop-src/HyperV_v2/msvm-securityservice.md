---
description: 表示安全性服務。 它是用來設定虛擬系統安全性設定。
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Msvm_SecurityService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944373"
---
# <a name="msvm_securityservice-class"></a>Msvm \_ SecurityService 類別

表示安全性服務。 它是用來設定虛擬系統安全性設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a>成員

**Msvm \_ SecurityService** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Msvm \_ SecurityService** 類別具有這些方法。



| 方法                                                                                            | 描述                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**GetKeyProtector**](msvm-securityservice-getkeyprotector.md)                                   | 取得虛擬系統金鑰保護裝置的方法。<br/>   |
| [**ModifySecuritySettings**](msvm-securityservice-modifysecuritysettings.md)                     | 修改虛擬機器的目前安全性設定。<br/> |
| [**RestoreLastKnownGoodKeyProtector**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | 還原到最後一個已知良好的金鑰保護裝置的方法。<br/> |
| [**SetKeyProtector**](msvm-securityservice-setkeyprotector.md)                                   | 為虛擬系統設定金鑰保護裝置的方法。<br/>        |
| [**SetSecurityPolicy**](msvm-securityservice-setsecuritypolicy.md)                               | 為虛擬系統設定金鑰保護裝置的方法。<br/>        |
| [**StartService**](msvm-securityservice-startservice.md)                                         | 啟動服務。<br/>                                          |
| [**StopService**](msvm-securityservice-stopservice.md)                                           | 停止服務。<br/>                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 服務**](cim-service.md)
</dt> </dl>

 

 




