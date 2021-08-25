---
description: CIM \_ SettingCoNtext 類別會將設定物件與設定物件建立關聯。
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: CIM_SettingCoNtext 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: df59bff8be90d3db3ac6dfde638120779850f2691bd3e93826c57f829d034a4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919508"
---
# <a name="cim_settingcontext-class"></a>CIM \_ SettingCoNtext 類別

**CIM \_ SettingCoNtext** 類別會將設定物件與設定物件建立關聯。 例如，網路介面卡的設定可能會根據其主控電腦系統所連接的網站或網路而變更。 在這種情況下，電腦系統會有兩個不同的設定物件，對應至兩個網路區段的網路設定差異。 其中一個設定會在一段時間進行操作時匯總網路介面卡的設定物件;相反地，另一個設定會匯總不同的網路介面卡設定物件，該物件是另一個區段特有的。 請注意，許多電腦設定與網路設定無關。 例如，這兩個設定會匯總電腦系統監視器解析度的相同設定物件。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a>成員

**CIM \_ SettingCoNtext** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ SettingCoNtext** 類別具有這些屬性。

<dl> <dt>

**內容**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 設定
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**匯總**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

參考匯總設定的設定物件。

</dd> <dt>

**設定**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 設定**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

匯總設定的參考。

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



 

