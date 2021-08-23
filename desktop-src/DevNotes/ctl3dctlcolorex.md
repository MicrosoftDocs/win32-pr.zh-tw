---
description: '\_針對使用 CTL3D 的應用程式處理 WM CTLCOLOR 訊息。'
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 46fe35fd507f20e41e0a9b563ded5c9cf46e9c557893bc9287d65cbdf651b24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691638"
---
# <a name="ctl3dctlcolorex-function"></a>Ctl3dCtlColorEx 函式

針對使用 CTL3D 的應用程式處理 **WM \_ CTLCOLOR** 訊息。

## <a name="syntax"></a>語法


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wm* 
</dt> <dd>

應用程式的 **WM \_ CTLCOLOR** 訊息。

</dd> <dt>

*wParam* 
</dt> <dd>

 (DC) 的顯示內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

子視窗的控制碼 (控制項) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回適當筆刷的控制碼;否則會傳回， `(HBRUSH)(0)` 表示發生錯誤。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
