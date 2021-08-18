---
description: CIM \_ AggregateRedundancyComponent 類別描述儲存體冗余群組中的匯總實體範圍。
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: CIM_AggregateRedundancyComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dec68f7c5464774f6b9aa8ef91ec427857dd09cb73bf709c207f0e8bfb4d319c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322778"
---
# <a name="cim_aggregateredundancycomponent-class"></a>CIM \_ AggregateRedundancyComponent 類別

**CIM \_ AggregateRedundancyComponent** 類別描述儲存體冗余群組中的匯總實體範圍。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a>成員

**CIM \_ AggregateRedundancyComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ AggregateRedundancyComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ StorageRedundancyGroup**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 
</dt> </dl>

包含儲存體冗余群組的 [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) 。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ AggregatePExtent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

[**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) ，包含參與冗余群組的匯總實體範圍。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ AggregateRedundancyComponent** 類別衍生自 [**cim \_ RedundancyComponent**](cim-redundancycomponent.md)。

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

[**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)
</dt> </dl>

 

