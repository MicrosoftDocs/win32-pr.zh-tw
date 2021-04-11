---
description: 當 InkEdit 控制項以手動方式從 InkEdit：：辨識方法的呼叫取得結果，或在辨識超時引發之後自動取得結果時發生。
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: 'InkEdit. RecognitionResult 事件 (筆跡 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194797"
---
# <a name="inkeditrecognitionresult-event"></a>InkEdit. RecognitionResult 事件

當 [InkEdit](inkedit-control-reference.md) 控制項以手動方式從 [**InkEdit：：辨識**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) 方法的呼叫取得結果，或在辨識超時引發之後自動取得結果時發生。

## <a name="syntax"></a>語法


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RecognitionResult* \[在\]
</dt> <dd>

[**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)物件，其中包含辨識的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkEditEvents** 介面中定義。 **\_ IInkEditEvents** 介面會以 DISPID IeeRecognitionResult 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>筆跡 (也需要筆跡 \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**辨識方法 \[ InkEdit 控制項\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

