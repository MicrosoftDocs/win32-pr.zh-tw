---
description: 啟用執行筆跡辨識、取出辨識結果，以及取得替代項的能力。 InkRecognizerCoNtext 可讓安裝在系統上的各種辨識器使用筆墨辨識來適當地處理輸入。
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: 'InkRecognizerCoNtext 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerContext
- InkRecognizerContext.IInkRecognizerContext
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 781d1b440f1287b22d5c3ddf7ecf7132f7311fc5f48da5da20e4145717f65bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218399"
---
# <a name="inkrecognizercontext-class"></a>InkRecognizerCoNtext 類別

啟用執行筆跡辨識、取出辨識結果，以及取得替代項的能力。 **InkRecognizerCoNtext** 可讓安裝在系統上的各種辨識器使用筆墨辨識來適當地處理輸入。

**InkRecognizerCoNtext** 具有下列類型的成員：

-   [事件](#events)
-   [介面](#interfaces)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**InkRecognizerCoNtext** 類別具有這些事件。



| 事件                                                                               | 描述                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**辨識**](inkrecognizercontext-recognition.md)                             | 當 InkRecognizerCoNtext 從 BackgroundRecognize 方法產生結果時發生。<br/>                                                                                             |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | **InkRecognizerCoNtext** 在呼叫 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)方法之後產生結果時發生<br/> |



 

### <a name="interfaces"></a>介面

**InkRecognizerCoNtext** 類別會定義這些介面。



| 介面                 | 描述                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkRecognizerCoNtext** | 這個物件會實 **IInkRecognizerCoNtext** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkRecognizerCoNtext** 類別有這些方法。



| 方法                                                                                              | 描述                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | 指定辨識器應該在辨識完成時，辨識相關聯 [**的筆劃**](inkrecognizercontext-recognition.md) 並引發辨識事件。<br/>                                                                |
| [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | 指定辨識器應該在辨識完成時，辨識相關聯的筆劃並引發 [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) 事件。<br/>                                    |
| [**複製**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | 建立重複的 **InkRecognizerCoNtext**。<br/>                                                                                                                                                                                               |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | 結束筆墨輸入至 **InkRecognizerCoNtext**。<br/>                                                                                                                                                                                             |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | 指出系統字典、使用者字典或 [**單字清單**](inkwordlist-class.md) 是否包含指定的字串。<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | 在 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合上執行辨識，並傳回辨識結果。<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | 結束對 [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) 或 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)的呼叫所開始的背景識別。<br/> |



 

### <a name="properties"></a>屬性

**InkRecognizerCoNtext** 類別具有這些屬性。



| 屬性                                                                                   | 存取類型           | Description                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | 讀取/寫入<br/> | 取得或設定字元自動完成模式，這個模式會決定何時辨識字元或文字。<br/>                                         |
| [**標記**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | 讀取/寫入<br/> | 取得或設定 **InkRecognizerCoNtext** 物件所使用之模擬的字串名稱。<br/>                                                        |
| [**指南**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | 讀取/寫入<br/> | 取得或設定要用於筆墨輸入的 [**InkRecognizerGuide**](inkrecognizerguide-class.md) 。<br/>                                                   |
| [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | 讀取/寫入<br/> | 取得或設定 **InkRecognizerCoNtext** 物件中 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合之前的字元。<br/> |
| [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | 讀取/寫入<br/> | 取得或設定旗標，指定辨識器如何解讀筆墨並決定結果字串。<br/>                                     |
| [**識別**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | 讀取/寫入<br/> | 取得或設定 **InkRecognizerCoNtext** 物件所使用的 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)物件。<br/>                                   |
| [**中風**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | 讀取/寫入<br/> | 取得或設定與 **InkRecognizerCoNtext** 物件相關聯的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。<br/>                    |
| [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | 讀取/寫入<br/> | 取得或設定在 **InkRecognizerCoNtext** 物件中 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合之後的字元。<br/>  |
| [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | 讀取/寫入<br/> | 取得或設定用來改善辨識結果的 [**InkWordList**](inkwordlist-class.md) 物件。<br/>                               |



 

## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

有兩種類型的辨識：背景 (非同步) 或前景 (同步) 。 背景辨識是透過呼叫 [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) 或 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) 方法來啟動，在背景執行緒上發生，並透過事件機制將結果回報給應用程式。 在所有辨識完成之前都不會傳回前景辨識，因此可在呼叫執行緒中使用辨識結果，而不需接聽辨識事件。

筆墨會在背景中持續處理。 如果將 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)新增至 **InkRecognizerCoNtext** 所參考的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合，則會立即辨識該 **IInkStrokeDisp** 。 如需詳細資訊，請參閱 [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) 方法主題中的備註。

所有辨識都會透過辨識器內容進行。 內容會定義單一識別會話的設定。 它會接收必須辨識的筆墨，並且在筆跡輸入和辨識輸出上定義條件約束。 可以在內容上設定的條件約束，包括所使用的語言、字典和文法。

> [!Note]  
> 只有當 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合是 **Null** 時，才會成功設定 [**筆劃**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)或 [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)屬性以外的屬性。 您必須先設定其他屬性，才能將 InkStrokes 集合附加至 **InkRecognizerCoNtext**，或必須將 InkStrokes 集合設定為 **Null** ，然後再設定其他屬性。 如果您將 InkStrokes 集合設為 **Null** ，然後再設定其他屬性，您可能必須重新附加 InkStrokes 集合。 這是因為當您將 InkStrokes 指派給 **InkRecognizerCoNtext** 之後，就會開始進行辨識。 進行呼叫以 [**辨識方法 \[ InkRecognizeCoNtext 類別 \]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)或 [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)時，可能已經有呼叫結果可供使用。

 

若要改善應用程式的效能，請在不再需要時處置您的 **InkRecognizerCoNtext** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkRecognizer 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

