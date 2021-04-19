---
description: CIM \_ ActionSequence 關聯會定義一系列的作業，這些作業會將 CIM SoftwareElementActions) 關聯 (所參考的軟體專案轉換 \_ 為下一個狀態，或從其目前的狀態中移除軟體元素。
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: CIM_ActionSequence 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986255"
---
# <a name="cim_actionsequence-class"></a>CIM \_ ActionSequence 類別

**Cim \_ ActionSequence** 關聯會定義一系列的作業，這些作業會將 [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)) 關聯 (所參考的軟體專案轉換為下一個狀態，或從其目前的狀態中移除軟體元素。

與特定軟體元素相關聯的下一個狀態動作和卸載動作必須是連續順序。 因為 **cim \_ ActionSequence** 是關聯，所以 [**cim \_ 動作**](cim-action.md) 類別上的迴圈會以「先前」動作和「下一個」動作的角色形成序列。

連續順序的需求表示：

-   在下一組狀態或卸載動作中，只有一個動作沒有 **CIM \_ ActionSequence** 關聯的實例在「下一個」角色中參考它。 這是序列中的第一個動作。
-   在下一組狀態或卸載動作中，只有一個動作沒有 **CIM \_ ActionSequence** 關聯的實例，其會在「先前」角色中參考它。 這是序列中的最後一個動作。
-   下一組狀態和卸載動作集合內的所有其他動作都必須參與 **CIM \_ ActionSequence** 關聯的兩個實例，一個是「先前」角色，另一個則是「下一個」角色。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a>成員

**CIM \_ ActionSequence** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ActionSequence** 類別具有這些屬性。

<dl> <dt>

**下一步**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 動作**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ， [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

下一個動作的參考。

</dd> <dt>

**之前**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 動作**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ， [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

先前動作的參考。

</dd> </dl>

## <a name="remarks"></a>備註

參與此關聯的 [**CIM \_ 動作**](cim-action.md) 類別必須具有與 **Direction** 屬性相同的值。

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

[CIM 類別](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

