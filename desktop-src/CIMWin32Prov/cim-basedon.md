---
description: CIM \_ BasedOn 類別代表一種關聯，描述如何從較低層級的範圍組合儲存區。
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: 'CIM_BasedOn 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a6bdd4c61628c71dbcb58b7b1d177cf7e936f802165aa9beed0aa195aeef4a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439258"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a>CIM_BasedOn 類別 (CIMWin32 WMI 提供者) 

**CIM \_ BasedOn** 類別代表一種關聯，描述如何從較低層級的範圍組合儲存區。 例如，實體範圍包含受保護的空間範圍。 因此，系統會從一或多個實體或受保護的空間範圍組合磁片區集合。 快取記憶體可以獨立定義並在實體元素中實現，也可以根據暫時性或非暫時性的儲存區。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a>成員

**CIM \_ BasedOn** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ BasedOn** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ StorageExtent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

描述較低層級儲存區的 [**CIM \_ StorageExtent**](cim-storageextent.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ StorageExtent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

描述較高層級儲存區的 [**CIM \_ StorageExtent**](cim-storageextent.md) 。

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出較低層級儲存體中的高階範圍結尾。 當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示較低層級儲存體中的高階範圍開始。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ BasedOn** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。

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

 

