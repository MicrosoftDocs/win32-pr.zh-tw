---
description: 列舉最近使用 (MRU) 清單的內容。 （選擇性）從列舉中抓取專案。
title: EnumMRUListW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851632"
---
# <a name="enummrulistw-function"></a>EnumMRUListW 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在後續版本的 Windows 中改變或無法使用。 \]

列舉最近使用 (MRU) 清單的內容。 （選擇性）從列舉中抓取專案。

## <a name="syntax"></a>語法


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMRU* \[在\]
</dt> <dd>

類型： **控制碼**

建立清單時所取得之 MRU 清單的控制碼。

</dd> <dt>

*nItem* \[在\]
</dt> <dd>

類型： **int**

要傳回的專案。 如果這個值小於0，函數會傳回 MRU 清單中的專案數。

</dd> <dt>

*lpData* \[擴展\]
</dt> <dd>

類型： **void \** _

接收 _nItem * 中所要求之專案的緩衝區指標。 如果 *nItem* 小於0，則這個緩衝區的內容不會變更。

</dd> <dt>

*uLen* \[在\]
</dt> <dd>

類型： **UINT**

緩衝區的大小，包括結束的 null 字元。 如果 MRU 清單是使用 **mru \_ 二進位** 旗標建立的，這就是以位元組為單位的大小。 否則，它是以字元為單位的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

傳回下列其中一個值。

-   如果 *nItem* 小於0，則傳回列舉中的專案數。
-   如果發生錯誤，則傳回-1。
-   否則，會傳回 *lpData* 中傳回的字串大小，包括終止的 null 字元。 如果 MRU 清單是使用 **mru \_ 二進位** 旗標建立的，這就是以位元組為單位的大小。 否則，它是以字元為單位的大小。

## <a name="remarks"></a>備註

此函式不包含在公用標頭或程式庫中。 您可以透過 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來存取它，也可以從 comctl32.dll 中解壓縮它的序數，也就是403（ **EnumMRUListW**）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (5.0 版或更新版本) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **EnumMRUListW** (Unicode) <br/>                                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateMRUListW**](createmrulist.md)
</dt> <dt>

[**MRUINFO**](mruinfo.md)
</dt> </dl>

 

 
