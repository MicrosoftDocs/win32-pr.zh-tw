---
description: 開始取消暫止之非同步搜尋的進程。
title: IShellFolderSearchable：： CancelAsyncSearch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972349"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>IShellFolderSearchable：： CancelAsyncSearch 方法

開始取消暫止之非同步搜尋的進程。

## <a name="syntax"></a>語法


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pidlSearch* \[在\]
</dt> <dd>

類型： **LPCITEMIDLIST**

搜尋 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 的指標。

</dd> <dt>

*pdwFlags* \[在\]
</dt> <dd>

類型： **DWORD \** _

目前未定義任何旗標;設定為 _ * Null * *。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

\_如果取消，則傳回 s OK; \_ 如果搜尋未執行，則傳回 FALSE。

## <a name="remarks"></a>備註

實際取消搜尋時，會呼叫 [**RunEnd**](ishellfoldersearchablecallback-runend.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




