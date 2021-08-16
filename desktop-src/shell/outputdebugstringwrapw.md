---
description: 將 Unicode 字串傳送至偵錯工具以供顯示。
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: 'OutputDebugStringWrapW 函式 (Shlwapip) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: cce8754b01ddf156951964b7189b4a7189759c52cdcd08e08091ca62b2e950bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858787"
---
# <a name="outputdebugstringwrapw-function"></a>OutputDebugStringWrapW 函式

\[這項功能可用於 Windows XP。 在後續版本中可能無法使用。 使用 [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) 的位置。\]

將 Unicode 字串傳送至偵錯工具以供顯示。

> [!Note]  
> **OutputDebugStringWrapW** 是 **OutputDebugStringW** 函數的包裝函式。 如需進一步的使用注意事項，請參閱 [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) 頁面。

 

## <a name="syntax"></a>語法


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpOutputString* \[在\]
</dt> <dd>

類型： **LPCWSTR**

要顯示之以 null 結束的 Unicode 字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**OutputDebugStringWrapW** 提供在 Windows XP 之前，在作業系統中使用 Unicode 字串的能力。 慣用的方法是使用 [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數115，直接從 Shlwapi.dll 呼叫 **OutputDebugStringWrapW** 。

如果應用程式沒有偵錯工具，系統偵錯工具就會顯示字串。 如果應用程式沒有偵錯工具，而系統偵錯工具未啟用，則 **OutputDebugStringWrapW** 不會執行任何動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shlwapip。h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
