---
description: CIM \_ AllocatedResource 類別代表邏輯裝置與系統資源之間的關聯，並指出資源已指派給裝置。
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: CIM_AllocatedResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2caf51e4b6a76693a64253e1046ea74c6ec19b8f5895618419aa693a10260f56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322698"
---
# <a name="cim_allocatedresource-class"></a>CIM \_ AllocatedResource 類別

**CIM \_ AllocatedResource** 類別代表邏輯裝置與系統資源之間的關聯，並指出資源已指派給裝置。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a>成員

**CIM \_ AllocatedResource** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ AllocatedResource** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ SystemResource**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

描述資源的 [**CIM \_ SystemResource**](cim-systemresource.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalDevice**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，其中包含指派給資源的邏輯裝置。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ AllocatedResource** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。

WMI 不會執行這個類別。 如需衍生自 **CIM \_ AllocatedResource** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。

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

 

