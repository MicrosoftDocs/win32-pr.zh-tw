---
description: 將應用程式取消註冊為 CTL3D 的用戶端。
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 32a954efceba7400692ad92c91bedb47283587827739c19f23e7802e1481fbe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691498"
---
# <a name="ctl3dunregister-function"></a>Ctl3dUnregister 函式

將應用程式取消註冊為 CTL3D 的用戶端。

## <a name="syntax"></a>語法


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hinstApp* 
</dt> <dd>

要以用戶端的形式取消註冊之應用程式的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果將應用程式取消註冊為 CTL3D 的用戶端，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

使用 CTL3D 的應用程式應該在 WinMain 中呼叫此函數。

不在 VGA 解析度的系統上無法使用3D 效果。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
