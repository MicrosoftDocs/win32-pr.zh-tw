---
description: 分派傳入的已傳送訊息、檢查已張貼訊息的執行緒訊息佇列，以及抓取訊息 (如果有任何) 存在的話。
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000703"
---
# <a name="_peekmessage-function"></a>\_PeekMessage 函式

\[此函式是 **PeekMessage** 函數的包裝函式。 這項功能可能會在未來變更或無法使用。 應用程式應該直接呼叫 **PeekMessage** 。\]

分派傳入的已傳送訊息、檢查已張貼訊息的執行緒訊息佇列，以及抓取訊息 (如果有任何) 存在的話。 請參閱 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)。

## <a name="syntax"></a>語法


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
