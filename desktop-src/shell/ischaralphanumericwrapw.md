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
ms.openlocfilehash: bf7f1b4db54cc5374214ff45b51579556dc22062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972433"
---
# <a name="ischaralphanumericwrapw-function"></a>IsCharAlphaNumericWrapW 函式

\[**IsCharAlphaNumericWrapW** 可用於 Windows XP。 在後續版本中將無法使用。 您應該在其位置使用 [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) 。\]

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

**IsCharAlphaNumericWrapW** 能讓您在 Windows XP 之前的作業系統中使用 Unicode 字串。 慣用的方法是使用 [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數28，直接從 Shlwapi.dll 呼叫 **IsCharAlphaNumericWrapW** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
