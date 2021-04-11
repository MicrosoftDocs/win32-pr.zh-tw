---
description: 清空填充碼資料庫快取。 在安裝新的填充碼資料庫之後，應該呼叫此函式。
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025810"
---
# <a name="shimflushcache-function"></a>ShimFlushCache 函式

清空填充碼資料庫快取。 在安裝新的填充碼資料庫之後，應該呼叫此函式。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在中，選擇性\]
</dt> <dd>

尚未必須是0。

</dd> <dt>

*hInstance* \[在中，選擇性\]
</dt> <dd>

尚未必須是0。

</dd> <dt>

*lpszCmdLine* \[在中，選擇性\]
</dt> <dd>

尚未必須是0。

</dd> <dt>

*nCmdShow* \[在\]
</dt> <dd>

尚未必須是0。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="remarks"></a>備註

呼叫端必須是系統管理員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BaseFlushAppcompatCache**](baseflushappcompatcache.md)
</dt> </dl>

 

 




