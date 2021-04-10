---
description: CIM \_ LogicalIdentity 類別是抽象和泛型關聯，表示兩個邏輯元素代表相同基礎實體的不同層面。
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: 'CIM_LogicalIdentity 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936155"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a>CIM_LogicalIdentity 類別 (CIMWin32 WMI 提供者) 

**CIM \_ LogicalIdentity** 類別是抽象和泛型關聯，表示兩個邏輯元素代表相同基礎實體的不同層面。 此關聯會傳達可使用多個繼承定義的內容，並且限制為 managed 系統專案的邏輯部分。 在大部分的情況下，識別關聯性是由索引鍵的相等或相關專案的其他一些識別屬性所決定。

關聯應僅用於已清楚瞭解的案例中，在子類別中允許更明確的定義和澄清。 以合理的關聯性為例，例如，表示同時為匯流排實體的裝置，以及裝置為 USB (匯流排) 和鍵盤 (功能) 實體的功能實體。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>成員

**CIM \_ LogicalIdentity** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ LogicalIdentity** 類別具有這些屬性。

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統實體替代層面的參考。

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯元素的一個層面參考。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。 針對衍生自 **CIM \_ LogicalIdentity** 的類別，請參閱 [Win32 類別](win32-provider.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




