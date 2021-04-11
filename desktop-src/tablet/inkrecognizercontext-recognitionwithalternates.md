---
description: InkRecognizerCoNtext 類別在呼叫 BackgroundRecognizeWithAlternates 方法方法之後產生結果時發生。
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: 'InkRecognizerCoNtext. RecognitionWithAlternates 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193723"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a>InkRecognizerCoNtext. RecognitionWithAlternates 事件

[**InkRecognizerCoNtext 類別**](inkrecognizercontext-class.md)在呼叫 [**BackgroundRecognizeWithAlternates 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)方法之後產生結果時發生。

## <a name="syntax"></a>語法


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RecognitionResult* \[在\]
</dt> <dd>

事件的辨識結果。

</dd> <dt>

*CustomData* \[在\]
</dt> <dd>

辨識結果的自訂資料。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> <dt>

*RecognitionStatus* \[在\]
</dt> <dd>

從最新的辨識結果到的認可狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

如果您嘗試從辨識事件處理常式取得原始 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件的存取權，則應用程式開發介面 (API) 的行為無法預期。 請勿嘗試這麼做。 相反地，如果您需要這樣做，請建立旗標， [**並在辨識事件處理**](inkrecognizercontext-recognition.md) 程式中加以設定。 然後您可以輪詢該旗標，判斷何時要變更事件處理常式以外的 **InkRecognizerCoNtext** 屬性。

此事件方法是在 \_ IInkEvents 介面中定義。 \_IInkEvents 介面會以 DISPID IRERecognitionWithAlternates 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkRecognizerCoNtext 類別**](inkrecognizercontext-class.md)
</dt> <dt>

[**BackgroundRecognizeWithAlternates 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[**辨識方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**IInkRecognitionResult 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

