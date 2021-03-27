---
description: 開始搜尋指定的搜尋字串。
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'IShellFolderSearchable：： FindString 方法 (Mmc.exe) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691208"
---
# <a name="ishellfoldersearchablefindstring-method"></a>IShellFolderSearchable：： FindString 方法

開始搜尋指定的搜尋字串。

## <a name="syntax"></a>語法


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszTarget* \[在\]
</dt> <dd>

類型： **LPCWSTR**

指定搜尋關鍵字之字串的指標。

</dd> <dt>

*pdwFlags* \[在\]
</dt> <dd>

類型： **DWORD \** _

目前未定義任何旗標;設定為 _ * Null * *。

</dd> <dt>

*punkOnAsyncSearch* \[在\]
</dt> <dd>

類型： **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

[_ *IUnknown* *](/windows/win32/api/unknwn/nn-unknwn-iunknown)類型之物件的指標。 這個物件必須支援 [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) 介面。 如果不需要回呼，請設定為 **Null** 。

</dd> <dt>

*ppidlOut* \[擴展\]
</dt> <dd>

類型： **LPITEMIDLIST**

搜尋資料夾之 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Mmc.exe</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
