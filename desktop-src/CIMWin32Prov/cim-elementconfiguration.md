---
description: CIM \_ ElementConfiguration 關聯會將 cim 設定 \_ 物件與一或多個受管理的系統元素產生關聯。 CIM 設定 \_ 物件代表特定的行為，或相關聯之 CIM ManagedSystemElement 所需的功能狀態 \_ 。
ms.assetid: 4d2af009-7466-4394-af42-72c8d96e0786
ms.tgt_platform: multiple
title: CIM_ElementConfiguration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConfiguration
- CIM_ElementConfiguration.Configuration
- CIM_ElementConfiguration.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7707338a3c2268cba51146aa8462b3b244b149ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025940"
---
# <a name="cim_elementconfiguration-class"></a>CIM \_ ElementConfiguration 類別

**Cim \_ ElementConfiguration** 關聯會將 [**cim \_ 設定**](cim-configuration.md)物件與一或多個受管理的系統元素產生關聯。 **Cim 設定 \_** 物件代表特定的行為，或相關聯之 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)所需的功能狀態。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{FC049DCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ElementConfiguration
{
  CIM_Configuration        REF Configuration;
  CIM_ManagedSystemElement REF Element;
};
```

## <a name="members"></a>成員

**CIM \_ ElementConfiguration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ElementConfiguration** 類別具有這些屬性。

<dl> <dt>

**Configuration**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 設定
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**CIM \_**](cim-configuration.md)設定物件的參考，此物件會將與 managed 系統專案相關聯的設定和相依性進行分組。

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Managed 系統元素的參考。

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



 

 




