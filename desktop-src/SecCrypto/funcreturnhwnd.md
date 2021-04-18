---
description: 密碼編譯服務提供者 (CSP) 用來取得 windows 控制碼，CSP 應使用該控制碼做為顯示之任何使用者介面的父系或擁有者。
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: 'CRYPT_RETURN_HWND 函式指標 (Cspdk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971592"
---
# <a name="crypt_return_hwnd-function-pointer"></a>CRYPT \_ RETURN \_ HWND 函數指標

[*密碼編譯服務提供者*](../secgloss/c-gly.md) (csp) 使用 **FuncReturnhWnd** 回呼函式，以取得 CSP 應使用的視窗控制碼，作為所顯示任何使用者介面的父系或擁有者。

## <a name="syntax"></a>語法


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phWnd* \[in、out\]
</dt> <dd>

接收父視窗控制碼之 **HWND** 變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個函式指標不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Cspdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPAcquireCoNtext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
