---
description: 將應用程式註冊為 CTL3D 的用戶端。
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990966"
---
# <a name="ctl3dregister-function"></a>Ctl3dRegister 函式

將應用程式註冊為 CTL3D 的用戶端。

## <a name="syntax"></a>語法


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hinstApp* 
</dt> <dd>

要註冊為用戶端之應用程式的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果3D 效果為使用中，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="remarks"></a>備註

使用 CTL3D 的應用程式應該在 WinMain 中呼叫此函數。

不在 VGA 解析度的系統上無法使用3D 效果。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
