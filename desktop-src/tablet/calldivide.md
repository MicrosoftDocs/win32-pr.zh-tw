---
description: 從 InkDivider 物件中取出分析資訊。
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: CallDivide 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510762"
---
# <a name="calldivide-function"></a>CallDivide 函式

從 [**InkDivider**](inkdivider-class.md) 物件中取出分析資訊。

此函式不適合應用程式程式碼使用。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDivider* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件的控制碼。

</dd> <dt>

*pWordSize* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件所傳回的單字大小。

</dd> <dt>

*pLineSize* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件所傳回的行大小。

</dd> <dt>

*pParagraphSize* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件所傳回之段落的大小。

</dd> <dt>

*pDrawingSize* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件所傳回之繪圖的大小。

</dd> <dt>

*pWordCount* \[擴展\]
</dt> <dd>

筆墨分析所傳回的文字數目。

</dd> <dt>

*pLineCount* \[擴展\]
</dt> <dd>

筆墨分析所傳回的行數。

</dd> <dt>

*pParagraphCount* \[擴展\]
</dt> <dd>

筆墨分析傳回的段落數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。



| 傳回碼                                                                                  | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 函數成功。<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 一或多個參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 程式庫<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




