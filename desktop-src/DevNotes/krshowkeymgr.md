---
description: 將 [金鑰管理員] 對話方塊顯示在使用者介面中。
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983960"
---
# <a name="krshowkeymgr-function"></a>KRShowKeyMgr 函式

\[這個函式只會包含在 Windows XP 中。 它目前不包含在其他任何版本的 Windows 中，也不會包含在任何未來版本的 Windows 中。\]

將 [金鑰管理員] 對話方塊顯示在使用者介面中。

## <a name="syntax"></a>語法


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwParent* 
</dt> <dd>

對話方塊的父視窗控制碼。 此參數可以是 **Null**。

</dd> <dt>

*hInstance* 
</dt> <dd>

不使用此參數，應該設定為 **Null**。

</dd> <dt>

*pszCmdLine* 
</dt> <dd>

不使用此參數，應該設定為 **Null**。

</dd> <dt>

*CmdShow* 
</dt> <dd>

不使用此參數，應該設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
