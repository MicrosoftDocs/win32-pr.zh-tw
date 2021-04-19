---
description: SetDateTime&\# 8194;WMI 類別方法會在電腦上設定目前的系統時間。
ms.assetid: b9b86a52-c3d7-489d-8632-b297970dbeac
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的 SetDateTime 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.SetDateTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60316904d58ffec38aa912a1454082e7edfae5a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001322"
---
# <a name="setdatetime-method-of-the-win32_operatingsystem-class"></a>Win32 作業系統類別的 SetDateTime 方法 \_

**SetDateTime** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會設定電腦上目前的系統時間。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetDateTime(
  [in] datetime LocalDatetime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>datetimeoffset.localdatetime* \[在\]
</dt> <dd>

目前時間的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**其他** (1 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

呼叫進程必須具有 SE \_ SYSTEMTIME \_ NAME 許可權。

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

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 作業系統**](win32-operatingsystem.md)
</dt> <dt>

[WMI 工作：桌面管理](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

