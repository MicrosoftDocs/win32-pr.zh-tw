---
description: 重建專案識別碼清單的指標， (從 Shell 資料夾的一個階層式標記法轉換成不同的標記法，以 PIDL) 。
title: IShellFolderViewType：： TranslateViewPidl 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 00d419d05a21c9328d29c23ee4c6475254cc6635594cc20e989144361caab3dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443278"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a>IShellFolderViewType：： TranslateViewPidl 方法

重建專案識別碼清單的指標， (從 Shell 資料夾的一個階層式標記法轉換成不同的標記法，以 PIDL) 。

## <a name="syntax"></a>語法


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pidl* \[在\]
</dt> <dd>

類型： **PCUIDLIST \_ 相對**

相對於根資料夾之專案識別碼的陣列。

</dd> <dt>

*pidlView* \[在\]
</dt> <dd>

類型： **PCUIDLIST \_ 相對**

視圖的特殊 PIDL。

</dd> <dt>

*ppidlOut* \[在\]
</dt> <dd>

類型： **PCUIDLIST \_ 相對 \***

要接收翻譯之 PIDL 變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

完成時，您應該使用 [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree)釋放傳回的 PIDL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




