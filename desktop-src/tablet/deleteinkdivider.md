---
description: 刪除 InkDivider 物件，並釋放相關聯的資源。
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: DeleteInkDivider 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 526186dd2a867f8fb3ee9201ca13df6afd43cb02f8361da202a036dde8e9fb56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709518"
---
# <a name="deleteinkdivider-function"></a>DeleteInkDivider 函式

刪除 [**InkDivider**](inkdivider-class.md) 物件，並釋放相關聯的資源。

此函式不適合應用程式程式碼使用。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDivider* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。



| 傳回碼                                                                                  | 描述                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法已成功。<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *HDivider* 參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 程式庫<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




