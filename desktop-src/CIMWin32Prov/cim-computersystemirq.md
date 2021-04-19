---
description: CIM \_ ComputerSystemIRQ 類別代表電腦系統與其可用的插斷要求 () 的 irq 之間的關聯。
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: CIM_ComputerSystemIRQ 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972139"
---
# <a name="cim_computersystemirq-class"></a>CIM \_ ComputerSystemIRQ 類別

**CIM \_ ComputerSystemIRQ** 類別代表電腦系統與其可用的插斷要求 () 的 irq 之間的關聯。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a>成員

**CIM \_ ComputerSystemIRQ** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ComputerSystemIRQ** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (的 GroupComponent) 
</dt> </dl>

CIM 的電腦，其描述與 IRQ 相關聯的電腦。 [**\_**](cim-computersystem.md)

這個屬性繼承自 [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ IRQ**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) ，[**弱**](/windows/desktop/WmiSdk/standard-qualifiers)式
</dt> </dl>

描述電腦系統之 IRQ 的 [**CIM \_ IRQ**](cim-irq.md) 。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ ComputerSystemIRQ** 類別衍生自 [**cim \_ ComputerSystemResource**](cim-computersystemresource.md)。

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

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)
</dt> </dl>

 

