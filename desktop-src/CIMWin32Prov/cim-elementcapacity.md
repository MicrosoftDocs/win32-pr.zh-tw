---
description: CIM \_ ElementCapacity 類別會將 cim \_ PhysicalCapacity 物件與一或多個實體元素產生關聯。 它會將最小和最大硬體需求的描述與所述的實體元素)  (或功能相關聯。
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468273"
---
# <a name="cim_elementcapacity-class"></a>CIM \_ ElementCapacity 類別

**Cim \_ ElementCapacity** 類別會將 [**cim \_ PhysicalCapacity**](cim-physicalcapacity.md)物件與一或多個實體元素產生關聯。 它會將最小和最大硬體需求的描述與所述的實體元素)  (或功能相關聯。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a>成員

**CIM \_ ElementCapacity** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ElementCapacity** 類別具有這些屬性。

<dl> <dt>

**容量**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalCapacity**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考 [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) 類別，其描述最小和最大需求，以及支援實體元素的不同硬體類型的能力。

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

所述實體元素的參考。

</dd> </dl>

## <a name="remarks"></a>備註

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



 

