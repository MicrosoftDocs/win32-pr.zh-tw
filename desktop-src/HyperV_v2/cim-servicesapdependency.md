---
description: 代表服務與服務存取點之間的關聯， (可為服務提供功能的 SAP) 。
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: 'CIM_ServiceSAPDependency 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980349"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a>CIM_ServiceSAPDependency 類別 (Hyper-v 管理) 

代表服務與服務存取點之間的關聯， (可為服務提供功能的 SAP) 。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a>成員

**CIM \_ ServiceSAPDependency** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ServiceSAPDependency** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ServiceAccessPoint**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

必要的服務存取點。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 服務**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

相依于 SAP 的服務。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> </dl>

 

