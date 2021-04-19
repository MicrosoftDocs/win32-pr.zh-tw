---
description: CIM \_ ElementsLinked 關聯表示以實體連結連接在一起的實體元素。
ms.assetid: b9e1d11e-6f89-4d7a-9b5c-01161e7c1bdf
ms.tgt_platform: multiple
title: CIM_ElementsLinked 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementsLinked
- CIM_ElementsLinked.Dependent
- CIM_ElementsLinked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353809056d1ca3bae710272b02c2636a3f02eef1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986260"
---
# <a name="cim_elementslinked-class"></a>CIM \_ ElementsLinked 類別

**CIM \_ ElementsLinked** 關聯表示以實體連結連接在一起的實體元素。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{FAF76B83-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementsLinked : CIM_Dependency
{
  CIM_PhysicalElement REF Dependent;
  CIM_PhysicalLink    REF Antecedent;
};
```

## <a name="members"></a>成員

**CIM \_ ElementsLinked** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ElementsLinked** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalLink**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

描述實體連結的 [**CIM \_ PhysicalLink**](cim-physicallink.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**CIM \_ PhysicalElement**](cim-physicalelement.md) ，描述已連結的實體元素。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ ElementsLinked** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。

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

[**CIM \_ 相依性**](cim-dependency.md)
</dt> </dl>

 

