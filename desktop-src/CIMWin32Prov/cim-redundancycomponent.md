---
description: CIM \_ RedundancyComponent 類別會將由受管理系統專案組成的複製群組產生關聯，並指出這些元素一起提供冗余。
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: CIM_RedundancyComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847055"
---
# <a name="cim_redundancycomponent-class"></a>CIM \_ RedundancyComponent 類別

**CIM \_ RedundancyComponent** 類別會將由受管理系統專案組成的複製群組產生關聯，並指出這些元素一起提供冗余。 在冗余群組中匯總的所有元素都應該是相同物件類別的具現化。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>成員

**CIM \_ RedundancyComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ RedundancyComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ RedundancyGroup**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 
</dt> </dl>

**CIM \_ RedundancyComponent** 關聯表示「這組風扇」或「這些實體範圍」參與單一的複製群組。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) ，描述關聯中的子項目。

這個屬性繼承自 [**CIM \_ 元件**](cim-component.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**CIM \_RedundancyComponent** 衍生自 [**CIM \_ 元件**](cim-component.md)。

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

[**CIM \_ 元件**](cim-component.md)
</dt> </dl>

 

