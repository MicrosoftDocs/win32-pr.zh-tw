---
description: 在 [內容] 工作表上，顯示指定資料夾的 [資料夾共用] 索引標籤。
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: 9683d7faee4bd44bd8f21e14250503f351e1a134119f978f872d7a0fe3ad6c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968257"
---
# <a name="showsharefolderui-function"></a>ShowShareFolderUI 函式

在 [內容] 工作表上，顯示指定資料夾的 [ **資料夾共用** ] 索引標籤。

## <a name="syntax"></a>語法


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

類型： **HWND**

屬性工作表的父視窗控制碼。

</dd> <dt>

*pszPath* \[在\]
</dt> <dd>

類型： **LPCWSTR**

字串的指標，指定資料夾的路徑，該路徑會顯示資料夾的 [ **共用** ] 索引標籤。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

此函式一律會傳回 S \_ OK。

## <a name="remarks"></a>備註

此函數沒有相關聯的 .lib 檔案。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 才能使用它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **ShowShareFolderUIW** (Unicode) <br/>                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
