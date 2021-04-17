---
description: 抓取指定標記的顯示名稱。
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468148"
---
# <a name="sdbtagtostring-function"></a>SdbTagToString 函式

抓取指定標記的顯示名稱。

## <a name="syntax"></a>語法


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*標記* \[在\]
</dt> <dd>

標記。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回以 null 結束的字串或 "InvalidTag" 的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**標記**](tag.md)
</dt> </dl>

 

 




