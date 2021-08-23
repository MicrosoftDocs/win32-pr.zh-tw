---
description: 在對話方塊中，將訊息傳送至指定的控制項。
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 3a1c17ab1ad303ce95755140ebe7f264b976471c7ecfa507f2152ec9e0ad221c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538831"
---
# <a name="_senddlgitemmessage-function"></a>\_SendDlgItemMessage 函式

\[此函式是 **SendDlgItemMessage** 函數的包裝函式。 這項功能可能會在未來變更或無法使用。 應用程式應該直接呼叫 **SendDlgItemMessage** 。\]

在對話方塊中，將訊息傳送至指定的控制項。 請參閱 [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)。

## <a name="syntax"></a>語法


```C++
LRESULT _SendDlgItemMessage(
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

[**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
