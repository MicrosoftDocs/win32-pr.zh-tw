---
description: CIM \_ StatisticalInformation 類別是適用于一或多個 managed 系統專案之統計資料或計量的任意集合的根類別。
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: CIM_StatisticalInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cb392f787c9f05d6c33545706bb55c90cda5e0ee14fa6e24fe7e6c8a878fe1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919188"
---
# <a name="cim_statisticalinformation-class"></a>CIM \_ StatisticalInformation 類別

**CIM \_ StatisticalInformation** 類別是適用于一或多個 managed 系統專案之統計資料或計量的任意集合的根類別。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>成員

**CIM \_ StatisticalInformation** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ StatisticalInformation** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

統計資料或度量的簡短文字描述。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

統計資料或度量的文字描述。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

統計資料或度量已知的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。 針對衍生自 **CIM \_ STATISTICALINFORMATION** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

