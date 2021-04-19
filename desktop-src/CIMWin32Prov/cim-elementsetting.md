---
description: CIM \_ ElementSetting 類別代表 managed 系統專案與其定義的設定類別之間的關聯。
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: 'CIM_ElementSetting 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c1ea52648728397e811cfae35e7a83e272ab8d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979713"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a>CIM_ElementSetting 類別 (CIMWin32 WMI 提供者) 

**CIM \_ ElementSetting** 類別代表 managed 系統專案與其定義的設定類別之間的關聯。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a>成員

**CIM \_ ElementSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ElementSetting** 類別具有這些屬性。

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**Cim \_ ElementSetting** 關聯之 [**cim \_ ManagedSystemElement**](cim-managedsystemelement.md)物件角色的參考。 相關聯的 managed system 元素提供可執行專案設定的元素。

</dd> <dt>

**設定**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 設定**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**Cim \_ ElementSetting** 關聯之 [**cim \_ 設定**](cim-setting.md)物件角色的參考。 相關聯的設定提供可執行元素設定的設定。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。 針對衍生自 **CIM \_ ElementSetting** 的類別，請參閱 [Win32 類別](win32-provider.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




