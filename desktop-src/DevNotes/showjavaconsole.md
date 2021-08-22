---
description: ShowJAVAConsole 函式是適用于 JAVA 開發人員的偵錯工具。 在 Internet Explorer 內執行的 applet (或其他 JAVA 程式碼) 可以用來顯示錯誤訊息和其他資訊。
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJAVAConsole 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 0a8517d32057b6434d3822cc02977f6afd72c1b387b78e85e53810bd27f00550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075852"
---
# <a name="showjavaconsole-function"></a>ShowJAVAConsole 函式

**ShowJAVAConsole** 函式是適用于 JAVA 開發人員的偵錯工具。 在 Internet Explorer 內執行的 applet (或其他 JAVA 程式碼) 可以用來顯示錯誤訊息和其他資訊。

## <a name="syntax"></a>語法


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

<dl></dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

呼叫 **ShowJAVAConsole** 會導致 java 虛擬機器 (VM) 顯示 java 主控台視窗。 JAVA 主控台視窗本身可以顯示在呼叫進程中執行的 JAVA 程式碼的偵錯工具輸出。 一般來說，這僅供裝載 JAVA VM 的應用程式使用。 每個進程只有一個 JAVA 主控台視窗;對 API 的多個呼叫會導致相同的視窗顯示。 換句話說，如果主控台視窗已經顯示，就不會發生任何事;如果視窗尚未顯示，或使用者已關閉，則會快顯視窗。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
