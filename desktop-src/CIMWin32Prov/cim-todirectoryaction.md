---
description: CIM \_ ToDirectoryAction 關聯會識別檔案動作的目標目錄。
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: CIM_ToDirectoryAction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 37ecee55fa76f6e86ccc60921851eca6cb922bec8fb6b00de01c3e410ca19940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020866"
---
# <a name="cim_todirectoryaction-class"></a>CIM \_ ToDirectoryAction 類別

**CIM \_ ToDirectoryAction** 關聯會識別檔案動作的目標目錄。 使用這個關聯時，會假設目標目錄是由先前的動作所建立。 此關聯無法與 [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) 關聯存在，因為檔案動作只能包含單一目標目錄。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a>成員

**CIM \_ ToDirectoryAction** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ToDirectoryAction** 類別具有這些屬性。

<dl> <dt>

**DestinationDirectory**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ DirectoryAction**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ， [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

目的地目錄的參考。

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ CopyFileAction**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 
</dt> </dl>

檔案名的參考。

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



 

