---
description: CIM \_ ProcessExecutable 類別代表進程和資料檔之間的連結，表示檔案參與處理常式的執行。
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: CIM_ProcessExecutable 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e55d5116c4f3f9d14840b5a5e0b75205156dbbaee3aa21c2d14dbb25c53d4b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080412"
---
# <a name="cim_processexecutable-class"></a>CIM \_ ProcessExecutable 類別

**CIM \_ ProcessExecutable** 類別代表進程和資料檔之間的連結，表示檔案參與處理常式的執行。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a>成員

**CIM \_ ProcessExecutable** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ProcessExecutable** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM 資料 \_ 檔**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) () ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

[**CIM 資料 \_ 檔**](cim-datafile.md)，描述參與進程執行的資料檔。

</dd> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 
</dt> </dl>

相關聯進程的位址空間中模組的基底位址。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 進程**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (相依) ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述進程的 [**CIM \_ 處理**](cim-process.md) 程式。

</dd> <dt>

**GlobalProcessCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 
</dt> </dl>

目前已將檔案載入記憶體中的進程數目。

</dd> <dt>

**ModuleInstance**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 
</dt> </dl>

Win32 實例控制碼。 這個屬性已過時，而且沒有取代值。

</dd> <dt>

**ProcessCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) 
</dt> </dl>

相關進程中檔案的參考計數。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ ProcessExecutable** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。

WMI 會實行 **CIM \_ ProcessExecutable** 類別。 **CIM \_ ProcessExecutable** 類別是動態類別。

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

 

