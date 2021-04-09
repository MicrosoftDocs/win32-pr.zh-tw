---
description: CIM \_ SoftwareElementChecks 關聯類別會將 software 元素與功能可能需要的條件或位置資訊產生關聯。
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: CIM_SoftwareElementChecks 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847152"
---
# <a name="cim_softwareelementchecks-class"></a>CIM \_ SoftwareElementChecks 類別

**CIM \_ SoftwareElementChecks** 關聯類別會將 software 元素與功能可能需要的條件或位置資訊產生關聯。

因為處於已就緒狀態的軟體專案無法轉換成另一個狀態，所以 **階段** 屬性的值會限制為處於隨時可用狀態的 [**CIM \_ SoftwareElement**](cim-softwareelement.md) 物件狀態。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a>成員

**CIM \_ SoftwareElementChecks** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ SoftwareElementChecks** 類別具有這些屬性。

<dl> <dt>

**檢查**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 檢查**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE) 、[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式
</dt> </dl>

檢查的參考。

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ SoftwareElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

元素的參考。

</dd> <dt>

**階段**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出參考的檢查是否為狀態檢查或下一次狀態檢查。

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

**狀態** (0) 


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

**下一步-狀態** (1) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。 針對衍生自 **CIM \_ SOFTWAREELEMENTCHECKS** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

