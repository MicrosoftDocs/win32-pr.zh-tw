---
description: 抓取筆墨分析所決定之對應單字、線條、段落或繪圖的 IInkStrokeDisp 物件的識別碼屬性。
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970553"
---
# <a name="calldivideresultsstrokeids-function"></a>CallDivideResultsStrokeIds 函式

抓取筆墨分析所決定之對應單字、線條、段落或繪圖的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性。

此函式不適合應用程式程式碼使用。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDivider* \[在\]
</dt> <dd>

[分隔](the-divider-object.md)物件的控制碼。

</dd> <dt>

*\[ aWordStrokeIds \]*\[out\]
</dt> <dd>

單字中筆墨的筆觸識別碼陣列。

</dd> <dt>

*\[ aLineStrokeIds \]*\[out\]
</dt> <dd>

線條中筆墨的筆觸識別碼陣列。

</dd> <dt>

*\[ aParagraphStrokeIds \]*\[out\]
</dt> <dd>

段落中筆墨的筆觸識別碼陣列。

</dd> <dt>

*\[ aDrawingStrokeIds \]*\[out\]
</dt> <dd>

繪圖中筆墨的筆觸識別碼陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。



| 傳回碼                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此函數已成功。<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *HDivider* 參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 程式庫<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




