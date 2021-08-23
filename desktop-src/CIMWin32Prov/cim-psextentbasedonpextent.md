---
description: CIM \_ PSExtentBasedOnPExtent 類別會將以實體範圍為基礎的受保護空間範圍產生關聯。
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: CIM_PSExtentBasedOnPExtent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 788d19eb2d9d11f5515f3507431498e713b3d1f98871ec79065f616cc606dea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080322"
---
# <a name="cim_psextentbasedonpextent-class"></a>CIM \_ PSExtentBasedOnPExtent 類別

**CIM \_ PSExtentBasedOnPExtent** 類別會將以實體範圍為基礎的受保護空間範圍產生關聯。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a>成員

**CIM \_ PSExtentBasedOnPExtent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ PSExtentBasedOnPExtent** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalExtent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

描述實體範圍的 [**CIM \_ PhysicalExtent**](cim-physicalextent.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ProtectedSpaceExtent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) ，描述以實體範圍為基礎的受保護空間範圍。

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出較低層級儲存體中的高階範圍結尾。 當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示較低層級儲存體中的高階範圍開始。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ PSExtentBasedOnPExtent** 類別衍生自 [**cim \_ BasedOn**](cim-basedon.md)。

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

[**CIM \_ BasedOn**](cim-basedon.md)
</dt> </dl>

 

