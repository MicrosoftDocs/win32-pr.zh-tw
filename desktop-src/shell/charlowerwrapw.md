---
description: 將 Unicode 字元字串或單一字元轉換成小寫。
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511062"
---
# <a name="charlowerwrapw-function"></a>CharLowerWrapW 函式

\[**CharLowerWrapW** 可用於 Windows XP。 在後續版本中可能無法使用。 您應該在其位置使用 [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) 。\]

將 Unicode 字元字串或單一字元轉換成小寫。 如果運算元是字元字串，則函式會就地轉換字元。

> [!Note]  
> **CharLowerWrapW** 是 **CharLowerW** 函數的包裝函式。 如需進一步的使用注意事項，請參閱 [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) 頁面。

 

## <a name="syntax"></a>語法


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pch* \[in、out\]
</dt> <dd>

類型： **LPWSTR**

指標，指向以 null 終止的 Unicode 字串或單一字元。 如果此參數的高序位字為零，則低序位單字必須只包含要轉換的單一字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LPWSTR**

如果 *pch* 是字元字串，則函式會傳回已轉換之字串的指標。 因為字串會就地轉換，所以傳回值等於 *pch*。

如果 *pch* 是單一字元，則傳回值為32位值，其高序位字組為零，而低序位字組包含轉換的字元。

沒有指示成功或失敗。 失敗很罕見。 此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

慣用的方法是使用 [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數38，直接從 Shlwapi.dll 呼叫 **CharLowerWrapW** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
