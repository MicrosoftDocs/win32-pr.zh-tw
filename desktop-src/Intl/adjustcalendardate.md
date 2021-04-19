---
description: 已取代。 以指定的年、月、周或日數來調整日期。
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: AdjustCalendarDate 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: ce2f61fd7d7d6354130873b5b2b2376c856e3958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972198"
---
# <a name="adjustcalendardate-function"></a>AdjustCalendarDate 函式

已取代。 以指定的年、月、周或日數來調整日期。

## <a name="syntax"></a>語法


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpCalDateTime* \[in、out\]
</dt> <dd>

[**CALDATETIME**](caldatetime.md)結構的指標，其中包含要調整的日期和行事曆資訊。

</dd> <dt>

*calUnit* \[在\]
</dt> <dd>

指出日期單位的 [**CALDATETIME \_ DATEUNIT**](caldatetime-dateunit.md) 列舉值，例如 DayUnit。

</dd> <dt>

*金額* \[擴展\]
</dt> <dd>

用來調整指定日期的量。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。 若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：

-   錯誤 \_ 日期 \_ 超出 \_ \_ 範圍。 指定的日期超出範圍。
-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

此函數沒有相關聯的標頭檔或程式庫檔案。 應用程式可以使用 DLL 名稱 (Kernel32.dll) 來呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。 然後，它可以使用模組控制碼和此函式的名稱來呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，以取得函數位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援](national-language-support.md)
</dt> <dt>

[國家語言支援功能](national-language-support-functions.md)
</dt> <dt>

[NLS：以名稱為基礎的 Api 範例](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
