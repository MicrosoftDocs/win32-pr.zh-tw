---
description: 判斷字元是否為字母或數位字元。
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf0a9752162c1593928e1bed270859ec4166230fe1f7e2d46d979c5c989ca237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452993"
---
# <a name="ischaralphanumericwrapw-function"></a>IsCharAlphaNumericWrapW 函式

\[**IsCharAlphaNumericWrapW** 可在 Windows XP 中使用。 在後續版本中將無法使用。 您應該在其位置使用 [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) 。\]

判斷字元是否為字母或數位字元。 這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。

> [!Note]  
> **IsCharAlphaNumericWrapW** 是 **IsCharAlphaNumericW** 函數的包裝函式。 如需進一步的使用注意事項，請參閱 [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) 頁面。

 

## <a name="syntax"></a>語法


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ch* \[在\]
</dt> <dd>

類型： **WCHAR**

要測試的 Unicode 字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **BOOL**

如果字元是英數位元，則傳回值為非零。

如果字元不是英數位元，則傳回值為零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

**IsCharAlphaNumericWrapW** 能讓您在早于 Windows XP 的作業系統中使用 Unicode 字串。 慣用的方法是使用 [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數28，直接從 Shlwapi.dll 呼叫 **IsCharAlphaNumericWrapW** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
