---
description: 釋出與最近使用的 (MRU) 清單相關聯的控制碼，並將快取的資料寫入登錄中。
title: FreeMRUList 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 8430142553e2c9e89a580760e9f9a041af07425f5380e35b7a2d53a48a953855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395898"
---
# <a name="freemrulist-function"></a>FreeMRUList 函式

釋出與最近使用的 (MRU) 清單相關聯的控制碼，並將快取的資料寫入登錄中。

## <a name="syntax"></a>語法


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMRU* \[在\]
</dt> <dd>

類型： **控制碼**

要釋放之 MRU 清單的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果成功，則傳回非負數值，否則為-1。

## <a name="remarks"></a>備註

如果 MRU 清單是使用 **mru \_ CACHEWRITE** 旗標建立的，則呼叫 **FreeMRUList** 會導致目前尚未寫入儲存在登錄中的 mru 清單版本的任何變更。

此函式不包含在公用標頭或程式庫中。 它必須由序數152從 comctl32.dll 解壓縮。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (5.0 版或更新版本) </dt> </dl> |



 

 




