---
title: Win32_TerminalError 類別
description: 表示終端機錯誤。
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Win32_TerminalError 類別遠端桌面服務
- Win32_TerminalError 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094095"
---
# <a name="win32_terminalerror-class"></a>Win32 \_ TerminalError 類別

表示終端機錯誤。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a>成員

**Win32 \_ TerminalError** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ TerminalError** 類別具有這些屬性。

<dl> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述錯誤或操作狀態的任何使用者定義字串。

這個屬性繼承自 [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)。

</dd> <dt>

**運算**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生失敗或異常時所發生的作業。 一般而言，WMI 會將此屬性設定為 WMI 方法的 COM API 名稱，如下所示： [**IWbemServices：： CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum)。

這個屬性繼承自 [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)。

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

錯誤或狀態變更所涉及的參數。 例如，如果應用程式嘗試取得不存在的類別，這個屬性會設定為違規的類別名稱。

這個屬性繼承自 [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)。

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別導致或報告錯誤或狀態變更的提供者。 如果不牽涉到提供者，此字串會設定為「Windows 管理」。

這個屬性繼承自 [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)。

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含作業的錯誤或資訊代碼。 這可以是提供者所定義的任何值，但值 0 (零) 通常會保留以表示成功。 這個屬性繼承自 [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus)。

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生錯誤之終端機 sin 的名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

