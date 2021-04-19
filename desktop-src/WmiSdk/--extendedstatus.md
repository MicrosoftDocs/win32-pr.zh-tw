---
description: 用來報告詳細的狀態和錯誤資訊。
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: __ExtendedStatus 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975334"
---
# <a name="__extendedstatus-class"></a>\_\_ExtendedStatus 類別

**\_ \_ ExtendedStatus** 系統類別可用來報告詳細的狀態和錯誤資訊。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a>成員

**\_ \_ ExtendedStatus** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ ExtendedStatus** 類別具有這些屬性。

<dl> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述錯誤或操作狀態的任何使用者定義字串。

</dd> <dt>

**運算**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生失敗或異常時所發生的作業。 一般來說，Windows Management Instrumentation (WMI) 會將這個屬性設定為 WMI 方法的 COM API 名稱，如下所示： [**IWbemServices：： CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)。

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

錯誤或狀態變更所涉及的參數。 例如，如果應用程式嘗試取得不存在的類別，這個屬性會設定為違規的類別名稱。

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別導致或報告錯誤或狀態變更的提供者。 如果不牽涉到提供者，此字串會設定為「Windows 管理」。

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含作業的錯誤或資訊代碼。 這可以是提供者所定義的任何值，但值 0 (零) 通常會保留以表示成功。 這個屬性繼承自 [**\_ \_ NotifyStatus**](--notifystatus.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ ExtendedStatus** 類別衍生自 [**\_ \_ NotifyStatus**](--notifystatus.md)類別。

您可以使用 **\_ \_ ExtendedStatus** 類別來報告比簡單的結果碼更複雜的資訊。 如果提供者需要更多屬性來描述錯誤，則可以從 **\_ \_ ExtendedStatus** 衍生自己的類別。

**StatusCode** 屬性（繼承自 [**\_ \_ NotifyStatus**](--notifystatus.md)父類別）是一個不帶正負號的整數，代表錯誤或狀態值。 當動態提供者從方法傳回這個類別的實例時， **StatusCode** 和 **Description** 屬性是由提供者設定，而其他屬性則由 WMI 設定。

## <a name="examples"></a>範例

下列程式碼範例（取自 [FND：如何使用](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa)TechNet 資源庫上的 WMI VBScript 程式碼範例處理設定管理員非同步錯誤）說明如何使用 **\_ \_ ExtendedStatus** 來取得錯誤資訊。


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 

