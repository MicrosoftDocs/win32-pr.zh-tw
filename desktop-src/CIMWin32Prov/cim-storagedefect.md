---
description: CIM \_ StorageDefect 匯總會收集儲存區的儲存錯誤。
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: CIM_StorageDefect 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 157714f9af979b34d647b1b02b1055b1cdac2ca0d84d3328c2c4740f9992024e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420966"
---
# <a name="cim_storagedefect-class"></a>CIM \_ StorageDefect 類別

**CIM \_ StorageDefect** 匯總會收集儲存區的儲存錯誤。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a>成員

**CIM \_ StorageDefect** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ StorageDefect** 類別具有這些屬性。

<dl> <dt>

**錯誤**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ StorageError**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**弱** 式](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

錯誤物件的參考，這個物件會定義對應于儲存區的開始和結束位址。

</dd> <dt>

**Extent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ StorageExtent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

參考發生錯誤的儲存區。

</dd> </dl>

## <a name="remarks"></a>備註

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



 

