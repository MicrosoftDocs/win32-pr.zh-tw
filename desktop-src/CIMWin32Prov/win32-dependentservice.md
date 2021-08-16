---
description: Win32 \_ DependentService 關聯 WMI 類別會關聯兩個相互依存的基礎服務。
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Win32_DependentService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 391db343723af04536ac970e1d8beb0d7c7fb4bb1fe47ac15846a877999f4e6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417624"
---
# <a name="win32_dependentservice-class"></a>Win32 \_ DependentService 類別

**Win32 \_ DependentService** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會關聯兩個相互依存的基礎服務。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ DependentService** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ DependentService** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ BaseService**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ BaseService" ) 
</dt> </dl>

代表基底服務的 [**Win32 \_ BaseService**](win32-baseservice.md) 依賴這個類別的 **相依** 屬性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ BaseService**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 BaseService」 \_ ) 
</dt> </dl>

[**Win32 \_ BaseService**](win32-baseservice.md) ，代表相依于這個類別之 **Antecedent** 屬性的基底服務。

</dd> <dt>

**TypeOfDependency**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

服務對服務相依性的本質。 這個屬性工作表示相關聯的服務必須已完成、必須啟動，或不能啟動，服務才能運作。

這個屬性繼承自 [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**服務必須已完成** (2) 


</dt> <dd>

服務必須已完成。

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**服務必須啟動** (3) 


</dt> <dd>

必須啟動服務。

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**服務不得啟動** (4) 


</dt> <dd>

服務不得啟動。

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ DependentService** 類別衍生自 [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)。

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

[**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

