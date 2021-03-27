---
description: 用來判斷專案是否存在於最近使用的 (MRU) 清單中。
title: MRUCMPPROC 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943620"
---
# <a name="mrucmpproc-callback-function"></a>MRUCMPPROC 回呼函式

用來判斷專案是否存在於最近使用的 (MRU) 清單中。

## <a name="syntax"></a>語法


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pString1* 
</dt> <dd>

類型： **LPCTSTR**

第一個字串。

</dd> <dt>

*pString2* 
</dt> <dd>

類型： **LPCTSTR**

要與第一個比較的第二個字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果專案相同，則傳回 0; 否則傳回非零值。

## <a name="remarks"></a>備註

您可以選擇性地指定此函數，以便在傳遞至 [**CreateMRUListW**](createmrulist.md)的 [**MRUINFO**](mruinfo.md)結構中使用。 當使用 **mru \_ 二進位** 旗標建立 mru 清單時，這非常有用。 如果未指定此函數，則會使用標準字串比較函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>            |
| Unicode 與 ANSI 名稱<br/>   | **MRUCMPPROCW** (Unicode) 和 **MRUCMPPROCA** (ANSI) <br/> |



 

 




