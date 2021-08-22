---
description: 初始化追蹤。
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: InitAsyncTrace 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: d64fcf9f787587165c12e675d79cfca641b0ab5086a5cce6b13029da46def974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956297"
---
# <a name="initasynctrace-function"></a>InitAsyncTrace 函式

初始化追蹤。

## <a name="syntax"></a>語法


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果函式成功，則此函數會傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

Exstrace.dll 是選用的元件，會以 Simple Mail 傳送通訊協定來安裝， (SMTP) 和網路新聞傳輸通訊協定 (NNTP) 。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
