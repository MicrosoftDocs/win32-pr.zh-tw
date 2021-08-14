---
description: 將緩衝區中的小寫字元轉換成大寫字元。
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: CharUpperBuffWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 288a119586e9f2e58172daaba33a8b9f27c791aa0005b5349f47cb0b2670a631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861553"
---
# <a name="charupperbuffwrapw-function"></a>CharUpperBuffWrapW 函式

\[**CharUpperBuffWrapW** 可在 Windows XP 中使用。 在後續版本中可能無法使用。 您應該在其位置使用 [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) 。\]

將緩衝區中的小寫字元轉換成大寫字元。 函數會就地轉換字元。

> [!Note]  
> **CharUpperBuffWrapW** 是 **CharUpperBuffW** 函數的包裝函式。 如需進一步的使用注意事項，請參閱 [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) 頁面。

 

## <a name="syntax"></a>語法


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pch* \[在\]
</dt> <dd>

類型： **LPWSTR**

包含一或多個要處理的 Unicode 字元之緩衝區的指標。

</dd> <dt>

*cchLength* \[在\]
</dt> <dd>

類型： **DWORD**

指定 *pch* 所指向之緩衝區的大小（以字元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **DWORD**

處理的字元數。

## <a name="remarks"></a>備註

慣用的方法是使用 [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數44，直接從 Shlwapi.dll 呼叫 **CharUpperBuffWrapW** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
