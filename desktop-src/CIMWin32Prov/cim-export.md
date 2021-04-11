---
description: CIM \_ 匯出類別代表本機檔案系統與其目錄之間的關聯，這表示指定的目錄可供掛接。
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: CIM_Export 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936318"
---
# <a name="cim_export-class"></a>CIM \_ 匯出類別

**CIM \_ 匯出** 類別代表本機檔案系統與其目錄之間的關聯，這表示指定的目錄可供掛接。 匯出整個檔案系統時，目錄應該參考檔案系統的最上層目錄。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a>成員

**CIM \_ 匯出** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ 匯出** 類別具有這些屬性。

<dl> <dt>

**目錄**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 目錄**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考針對網路檔案系統匯出的目錄 (NFS) 掛接。

</dd> <dt>

**ExportedDirectoryName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯出目錄時所用的名稱。

</dd> <dt>

**LocalFS**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LocalFileSystem**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

本機檔案系統的參考。

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



 

