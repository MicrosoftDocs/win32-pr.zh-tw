---
description: CIM \_ SlotInSlot 關聯性代表特殊介面卡擴充現有插槽結構的能力，以啟用其他不相容的卡片來插入框架或主控面板。
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: CIM_SlotInSlot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972761"
---
# <a name="cim_slotinslot-class"></a>CIM \_ SlotInSlot 類別

**CIM \_ SlotInSlot** 關聯性代表特殊介面卡擴充現有插槽結構的能力，以啟用其他不相容的卡片來插入框架或主控面板。 位置是一種特殊類型的連接器，通常會在其中插入介面卡。 介面卡可有效地建立新的位置，並可將其視為 (在概念上) 作為插槽中的位置。 如果是與現有插槽不相容的卡片，則可透過與介面卡所提供的插槽互動來支援。 例如，網路板的成本很高。 當有可用的新硬體時，會變更底座和卡片設定。 為了保護其客戶的投資，網路廠商會製造特殊的介面卡，以使用符合一或多個現有插槽的特殊介面卡，讓舊卡符合新的底座或主機面板或新卡片，並顯示可容納卡片的新位置。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>成員

**CIM \_ SlotInSlot** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ SlotInSlot** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 位置
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

[**CIM 位置 \_**](cim-slot.md) ，可描述主控面板的現有插槽 (s) ，或要調整以容納不會與它實際及/或電相容之卡片的框架。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 位置
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

[**CIM 位置 \_**](cim-slot.md) ，描述介面卡面板所提供的新位置。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ SlotInSlot** 類別衍生自 [**cim \_ ConnectedTo**](cim-connectedto.md)。

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

[**CIM \_ ConnectedTo**](cim-connectedto.md)
</dt> </dl>

 

