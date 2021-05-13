---
description: 抓取列舉值，這個列舉值會為每個擴充視圖 (PIDL) 的專案識別碼清單傳回一個指標。
title: IShellFolderViewType：： EnumViews 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.EnumViews
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e44cd774-1d16-4faa-b5ca-fcaf2740cdca
ms.openlocfilehash: 1627bb134066821444788ca44a3527278a02f4c7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842769"
---
# <a name="ishellfolderviewtypeenumviews-method"></a>IShellFolderViewType：： EnumViews 方法

抓取列舉值，這個列舉值會為每個擴充視圖 (PIDL) 的專案識別碼清單傳回一個指標。

## <a name="syntax"></a>語法


```C++
HRESULT EnumViews(
  [in]  ULONG       grfFlags,
  [out] IEnumIDList **ppenum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*grfFlags* \[在\]
</dt> <dd>

類型： **ULONG**

旗標，指出列舉中要包含的專案。 如需可能值的清單，請參閱 [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) 列舉型別。 您可以忽略這個參數。

</dd> <dt>

*ppenum* \[擴展\]
</dt> <dd>

類型： **[ **IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist)\*\***

接收列舉值之 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 型別指標變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

Views 會以 Pidl) 表示的根目錄 (，以隱藏資料夾的形式呈現給使用者。 在適當的情況下，預設 view (off 根資料夾) 會以 **Null** 或空白 PIDL 來表示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




