---
description: CIM \_ MemoryWithMedia 類別會將實體記憶體與實體媒體和其墨水匣產生關聯。 記憶體會提供媒體識別，並儲存使用者專屬的資料。
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: CIM_MemoryWithMedia 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b990f8ba842f313449b6f24f4e2ce59787f7841
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321631"
---
# <a name="cim_memorywithmedia-class"></a>CIM \_ MemoryWithMedia 類別

**CIM \_ MemoryWithMedia** 類別會將實體記憶體與實體媒體和其墨水匣產生關聯。 記憶體會提供媒體識別，並儲存使用者專屬的資料。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a>成員

**CIM \_ MemoryWithMedia** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ MemoryWithMedia** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalMemory**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md) ，描述與實體媒體相關聯的記憶體。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ PhysicalMedia**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

描述實體媒體的 [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) 。

</dd> </dl>

## <a name="remarks"></a>備註

**CIM \_MemoryWithMedia** 繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

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

 

