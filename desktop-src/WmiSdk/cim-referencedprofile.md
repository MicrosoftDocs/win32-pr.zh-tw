---
description: 用來將實例 CIM \_ RegisteredProfile 與 \_ 另一個參考相依設定檔的另一個設定檔的 cim RegisteredProfile 實例相關聯，做為相關的設定檔。
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997890"
---
# <a name="cim_referencedprofile-class"></a>CIM \_ ReferencedProfile 類別

用來將實例 [**cim \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) 與另一個參考相依設定檔的另一個設定檔的 **cim \_ RegisteredProfile** 實例相關聯，做為相關的設定檔。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>成員

**CIM \_ ReferencedProfile** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ReferencedProfile** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 **相依** 設定檔所參考的 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))實例。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定參考其他設定檔的 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) 實例。

</dd> </dl>

## <a name="remarks"></a>備註

系統會定義 **CIM \_ ReferencedProfile** 關聯中的 **相依** 和 **Antecedent** 屬性，讓參考的設定檔是前一個，而執行參考的設定檔是相依的。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                      |
| 命名空間<br/>                | 根 \\ interop<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop. mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

