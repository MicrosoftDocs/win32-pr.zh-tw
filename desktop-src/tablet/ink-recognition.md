---
description: 並非所有應用程式都需要使用辨識，但因為大部分的應用程式都是以文字作為其主要資料類型來設計，所以將筆墨轉換成文字的能力非常重要。
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: 筆跡辨識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550706"
---
# <a name="ink-recognition"></a>筆跡辨識

並非所有應用程式都需要使用辨識，但因為大部分的應用程式都是以文字作為其主要資料類型來設計，所以將筆墨轉換成文字的能力非常重要。 您可以使用 Tablet PC 平臺 API 的辨識功能來查詢可用辨識引擎的相關資訊，例如它們所辨識的語言。 然後，您可以從 [**筆墨**](inkdisp-class.md)物件將 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合傳送到辨識引擎，並讓它傳回 [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)物件。

## <a name="recognizercontext-object"></a>RecognizerCoNtext 物件

[**RecognizerCoNtext**](inkrecognizercontext-class.md)物件是指定辨識器的具現化。 **RecognizerCoNtext** 物件可讓您以同步或非同步方式辨識指定的筆劃集合。 以非同步方式辨識時， **RecognizerCoNtext** 物件會將事件回呼中的 [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件傳回給應用程式。

## <a name="recognizers-and-recognizer-objects"></a>辨識器和辨識器物件

單一 Tablet PC 可能會有一或多個辨識器可用。 您可以查詢辨識器的集合，以判斷要使用哪一個辨識器。 辨識器提供有關其功能的特定資訊，例如可辨識的語言和製造商。

若要判斷是否至少安裝了一個辨識器，請將 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件具現化，如下列 c + + 和 c 程式 \# 代碼範例所示。 如果找不到辨識器，則這個對 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 的呼叫會失敗。


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a>RecognitionResult 和 RecognitionAlternate 物件

辨識的結果會在 [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) 物件中傳回。 結果包含 [TopString](/previous-versions/ms829602(v=msdn.10)) 屬性中的最佳結果字串，以及 [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) 集合中替代結果的集合。 **RecognitionResult** 物件可以使用產生它的原始 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合來保存。

## <a name="recognizerguide-structure"></a>RecognizerGuide 結構

辨識器指南可以包含資料列和資料行，並為辨識器提供較佳的內容以執行辨識。 例如，您可以在使用者畫面上繪製水平線，就像是一段紙紙，顯示手寫的出現位置 (這種類型的指南只會包含資料列，而且沒有任何資料行) 。 如果使用者在行上進行寫入，而不是使用某些任意空間，則辨識精確度會有所改善。

下圖顯示具有兩行輸入的 [**RecognizerGuide**](inkrecognizerguide-class.md) 結構。

![顯示兩行辨識器指南的圖例](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

下圖顯示具有四個數據行和三個數據列的 [**RecognizerGuide**](inkrecognizerguide-class.md) 結構。

![顯示三四個辨識器指南的圖例](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

如需有關使用 [**RecognizerGuide**](inkrecognizerguide-class.md) 結構的詳細資訊，請參閱 **RecognizerGuide** 參考主題。

 

 
