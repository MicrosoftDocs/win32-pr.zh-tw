---
description: CIM \_ DependencyCoNtext 關聯性會將 cim 相依性 \_ 類別與一個或多個 cim 設定物件產生關聯 \_ 。 例如，電腦系統的相依性可能會根據系統所連接的網路而變更。
ms.assetid: 9f35fc41-1bfa-4018-a54c-64c875c710d4
ms.tgt_platform: multiple
title: CIM_DependencyCoNtext 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DependencyContext
- CIM_DependencyContext.Context
- CIM_DependencyContext.Dependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 845086b7d41eb03227d6b5b47240ef4bf9e1a2c35f8049c96d5c665800b327e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924638"
---
# <a name="cim_dependencycontext-class"></a>CIM \_ DependencyCoNtext 類別

**Cim \_ DependencyCoNtext** 關聯性會將 [**cim \_**](cim-dependency.md)相依性類別與一個或多個 [**cim \_ 設定物件**](cim-configuration.md)產生關聯。 例如，電腦系統的相依性可能會根據系統所連接的網路而變更。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Aggregation, Association, UUID("{A228E208-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DependencyContext
{
  CIM_Configuration REF Context;
  CIM_Dependency    REF Dependency;
};
```

## <a name="members"></a>成員

**CIM \_ DependencyCoNtext** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ DependencyCoNtext** 類別具有這些屬性。

<dl> <dt>

**內容**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 設定
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

參考匯總相依性的設定物件。

</dd> <dt>

**相依性**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 相依性
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯總相依性的參考。

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



 

