---
description: 從 InkDivider 物件取出分析結果。
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2e5f3060f261ba84b70272ed358a7c544f2b0e1582de310ed759b4ea40714359
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967757"
---
# <a name="calldivideresults-function"></a>CallDivideResults 函式

從 [**InkDivider**](inkdivider-class.md) 物件取出分析結果。

此函式不適合應用程式程式碼使用。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDivider* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件的控制碼。

</dd> <dt>

*aWordStrokeIds* \[擴展\]
</dt> <dd>

與傳遞給 [**InkDivider**](inkdivider-class.md) 類別的單字相關聯的識別碼陣列。

</dd> <dt>

*aLineStrokeIds* \[擴展\]
</dt> <dd>

[**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性陣列，這些物件與傳遞給 [**InkDivider**](inkdivider-class.md)類別的行相關聯。

</dd> <dt>

*aParagraphStrokeIds* \[擴展\]
</dt> <dd>

與 [**InkDivider**](inkdivider-class.md)類別中的段落相關聯之 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性陣列。

</dd> <dt>

*aDrawingStrokeIds* \[擴展\]
</dt> <dd>

與 [**InkDivider**](inkdivider-class.md)類別中的繪圖相關聯之 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性陣列。

</dd> <dt>

*pastrWords* \[擴展\]
</dt> <dd>

從筆墨分析傳回的單字陣列。

</dd> <dt>

*pastrLines* \[擴展\]
</dt> <dd>

從筆墨分析傳回的行陣列。

</dd> <dt>

*pastrParagraphs* \[擴展\]
</dt> <dd>

從筆墨分析傳回的段落陣列。

</dd> <dt>

*aWordRotationCenterX* \[擴展\]
</dt> <dd>

從筆墨分析沿著 X 軸的單字中心點陣列。

</dd> <dt>

*aWordRotationCenterY* \[擴展\]
</dt> <dd>

從筆墨分析沿著 y 軸的單字中心點陣列。

</dd> <dt>

*aWordAngle* \[擴展\]
</dt> <dd>

陣列，其中包含用來旋轉最佳分析結果之單字的角度。

</dd> <dt>

*aLineRotationCenterX* \[擴展\]
</dt> <dd>

陣列，包含沿著 X 軸之線條的中心點。

</dd> <dt>

*aLineRotationCenterY* \[擴展\]
</dt> <dd>

陣列，其中包含沿著 y 軸之線條的中心點。

</dd> <dt>

*aLineAngle* \[擴展\]
</dt> <dd>

陣列，其中包含用來旋轉最佳分析結果之線條的角度。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 此函數已成功。<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *HDivider* 參數無效。<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 無法配置足夠的記憶體來儲存結果。<br/> |



 

## <a name="remarks"></a>備註

若要避免記憶體流失，您必須釋放 *pastrWords*、 *pastrLines* 和 *pastrParagraphs* 的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 程式庫<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




