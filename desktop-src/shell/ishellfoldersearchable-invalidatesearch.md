---
description: 將這個指標變成專案識別碼清單 (PIDL) Shell 資料夾的無效部分。
title: IShellFolderSearchable：： InvalidateSearch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 5f443f3abd4a5cf2c1d0fc473c9267660d05c183a02c7f7705c1fabcbc9a8918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596568"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>IShellFolderSearchable：： InvalidateSearch 方法

將這個指標變成專案識別碼清單 (PIDL) Shell 資料夾的無效部分。

## <a name="syntax"></a>語法


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pidlSearch* \[在\]
</dt> <dd>

類型： **LPCITEMIDLIST**

搜尋資料夾之 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的指標。

</dd> <dt>

*pdwFlags* \[在\]
</dt> <dd>

類型： **DWORD \***

目前未定義任何旗標;設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當搜尋資料夾無效時，它可以對其使用的任何資源執行清除。 **IShellFolderSearchable：： InvalidateSearch** 方法可能會導致取消非同步搜尋，而且會產生 [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md)介面物件的最終版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




