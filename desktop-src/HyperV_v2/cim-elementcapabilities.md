---
description: 代表 managed 元素與其功能之間的關聯。
ms.assetid: 0e080042-4a56-40b7-acc5-cf69eb2a0604
title: CIM_ElementCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapabilities
- CIM_ElementCapabilities.ManagedElement
- CIM_ElementCapabilities.Capabilities
- CIM_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c705d0bb4743d4919ca840f51b3324510558078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973503"
---
# <a name="cim_elementcapabilities-class"></a>CIM \_ ElementCapabilities 類別

代表 managed 元素與其功能之間的關聯。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a>成員

**CIM \_ ElementCapabilities** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ElementCapabilities** 類別具有這些屬性。

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 功能**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

與 managed 元素相關聯的功能。

</dd> <dt>

**特性**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

一組有關功能的描述性資訊。

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**預設** (2) 


</dt> <dd></dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>

**目前** 的 (3) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**廠商特定** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

Managed 元素。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

