---
description: 在 InkDivider 物件上設定 LineHeight 屬性。
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: SetLineHeight 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2c6a176b5878b7aaee4a0e51a5a366302b13a1a643453ad2c6d57e103362c4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966817"
---
# <a name="setlineheight-function"></a>SetLineHeight 函式

在 [**InkDivider**](inkdivider-class.md)物件上設定 [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)屬性。

此 helper 函式不適合應用程式程式碼使用。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDivider* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件的控制碼。

</dd> <dt>

*lLineHeight* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件的 [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)屬性，以 HIMETRIC 單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。



| 傳回碼                                                                                  | 描述                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此函數已成功。<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *PDivider* 參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 程式庫<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 
