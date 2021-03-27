---
description: 用來判斷是否要在 web view 中顯示 [共用此資料夾] 選項。
title: CanShareFolderW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511063"
---
# <a name="cansharefolderw-function"></a>CanShareFolderW 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在後續版本的 Windows 中改變或無法使用。\]

用來判斷是否要在 web view 中顯示 [ **共用此資料夾** ] 選項。

## <a name="syntax"></a>語法


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszPath* \[在\]
</dt> <dd>

類型： **LPCWSTR**

指定要測試之資料夾路徑的字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **STDAPI**

傳回值包括下列各項。



| 傳回碼/值                                                                        | Description                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>     | *PszPath* 所指向的路徑會指定可共用的資料夾。<br/>    |
| <dl> <dt>**S \_ FALSE**</dt> </dl>  | *PszPath* 所指向的路徑會指定無法共用的資料夾。<br/> |
| <dl> <dt>HRESULT 錯誤</dt> </dl> | 發生錯誤了。<br/>                                                     |



 

## <a name="remarks"></a>備註

此函數沒有相關聯的 .lib 檔案。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 才能使用它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CanShareFolderW** (Unicode) <br/>                                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ShowShareFolderUI**](./showsharefolderui.md)
</dt> </dl>

 

 
