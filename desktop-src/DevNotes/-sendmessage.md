---
description: 將指定的訊息傳送至視窗或視窗。
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993981"
---
# <a name="_sendmessage-function"></a>\_SendMessage 函式

\[此函式是 **SendMessage** 函數的包裝函式。 這項功能可能會在未來變更或無法使用。 應用程式應該直接呼叫 **SendMessage** 。\]

將指定的訊息傳送至視窗或視窗。 請參閱 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)。

## <a name="syntax"></a>語法


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
