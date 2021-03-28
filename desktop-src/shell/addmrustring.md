---
description: 將字串加入最近使用的 (MRU) 清單的最上方。
title: AddMRUStringW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026106"
---
# <a name="addmrustringw-function"></a>AddMRUStringW 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在後續版本的 Windows 中改變或無法使用。 \]

將字串加入最近使用的 (MRU) 清單的最上方。

## <a name="syntax"></a>語法


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMRU* \[在\]
</dt> <dd>

類型： **控制碼**

MRU 清單的控制碼。

</dd> <dt>

*szString* \[在\]
</dt> <dd>

類型： **LPCTSTR**

資料的指標。 這可以是字串，或者，如果使用 **mru \_ 二進位** 旗標的二進位資料來建立 mru 清單，則為。 在二進位資料的情況下，第一個 **DWORD** 會指出其大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果成功，則傳回非負數值，否則為-1。

## <a name="remarks"></a>備註

此函式不包含在公用標頭或程式庫中。 您可以透過 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 來存取它，也可以從 comctl32.dll 中解壓縮它的序數，也就是401（ **AddMRUStringW**）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (5.0 版或更新版本) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **AddMRUStringW** (Unicode) <br/>                                                                         |



 

