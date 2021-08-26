---
description: CIM \_ HostedService 類別代表服務與功能所在系統之間的關聯。
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: 'CIM_HostedService 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7e70f7dea8fe6f5be0da7d76b37cf99ba4dcc7397c09cf27b542129232212286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921598"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a>CIM_HostedService 類別 (CIMWin32 WMI 提供者) 

**CIM \_ HostedService** 類別代表服務與功能所在系統之間的關聯。 系統可能會裝載許多服務，而這些服務會延後到裝載系統。 此模型不代表跨多個系統裝載的服務。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a>成員

**CIM \_ HostedService** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ HostedService** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 系統**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

描述裝載系統的 [**CIM \_ 系統**](cim-system.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 服務**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式
</dt> </dl>

[**CIM \_ 服務**](cim-service.md)，描述系統上裝載的服務。

</dd> </dl>

## <a name="remarks"></a>備註

**CIM \_HostedService** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。

WMI 不會執行這個類別。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> </dl>

 

