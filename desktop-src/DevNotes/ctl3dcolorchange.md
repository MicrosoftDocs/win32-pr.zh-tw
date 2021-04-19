---
description: 處理使用 CTL3D 之應用程式的系統色彩變更。
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Ctl3dColorChange 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985770"
---
# <a name="ctl3dcolorchange-function"></a>Ctl3dColorChange 函式

處理使用 CTL3D 之應用程式的系統色彩變更。

## <a name="syntax"></a>語法


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

此函式應針對 **WM \_ SYSCOLORCHANGE** 訊息在應用程式的主要視窗程式中呼叫，如下所示。

## <a name="examples"></a>範例

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
