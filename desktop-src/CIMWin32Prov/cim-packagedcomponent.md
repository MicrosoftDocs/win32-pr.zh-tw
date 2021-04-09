---
description: CIM \_ PackagedComponent 關聯表示一個明確的關聯性，其中元件通常包含在實體封裝中，例如底座或卡片。
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: CIM_PackagedComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b95cbbea60bfbd6bb352e53cfecb8819d99ec24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847106"
---
# <a name="cim_packagedcomponent-class"></a>CIM \_ PackagedComponent 類別

**CIM \_ PackagedComponent** 關聯表示一個明確的關聯性，其中元件通常包含在實體封裝中，例如底座或卡片。

**注意** 元件可能會從其包含的封裝中移除（或尚未插入） (也就是，「卸載式布林值 **」** **屬性) 。** 因此，元件可能不會永遠與容器相關聯。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a>成員

**CIM \_ PackagedComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ PackagedComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalPackage**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md) ，描述包含) 元件 (的實體套件。

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式的字串，表示實體元素在實體封裝內的位置。 與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。 此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。

這個屬性繼承自 [**CIM \_ 容器**](cim-container.md)。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalComponent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) ，描述封裝中包含的實體元件。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ PackagedComponent** 類別衍生自 [**cim \_ 容器**](cim-container.md)。

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

[**CIM \_ 容器**](cim-container.md)
</dt> </dl>

 

