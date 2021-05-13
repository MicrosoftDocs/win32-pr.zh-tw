---
description: 建立最近使用的新 (MRU) 清單。
title: CreateMRUListW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843379"
---
# <a name="createmrulistw-function"></a>CreateMRUListW 函式

建立最近使用的新 (MRU) 清單。

## <a name="syntax"></a>語法


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpmi* \[在\]
</dt> <dd>

類型： **LPMRUINFO**

定義 MRU 清單的 [**MRUINFO**](mruinfo.md) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

傳回新 MRU 清單的控制碼，如果發生錯誤，則傳回0。

## <a name="remarks"></a>備註

此函式不包含在公用標頭或程式庫中。 您可以透過 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來存取它，也可以從 comctl32.dll 中解壓縮它的序數，也就是400（ **CreateMRUListW**）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (5.0 版或更新版本) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CreateMRUListW** (Unicode) <br/>                                                                        |



 

 
