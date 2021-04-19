---
description: 指定 IInkAnalysisRecognizer 的屬性。
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: 'RecognizerCapabilities 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971854"
---
# <a name="recognizercapabilities-enumeration"></a>RecognizerCapabilities 列舉

指定 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的屬性。

## <a name="syntax"></a>Syntax


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ 無**
</dt> <dd>

未指定任何功能。

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**
</dt> <dd>

忽略所有其他已設定的旗標。

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC \_ 物件**
</dt> <dd>

支持對象識別;否則，只會辨識文字。

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**
</dt> <dd>

支援自由輸入，其中輸入筆墨時，不需使用辨識指南，例如線條或方塊。

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**
</dt> <dd>

支援線條輸入，這類似于書寫線條紙。

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**
</dt> <dd>

支援在方塊中輸入每個字元或單字的已框輸入。

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**
</dt> <dd>

支援字元自動完成。 支援字元自動完成的辨識器需要有已裝箱的輸入。

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**
</dt> <dd>

支援向右和向下訂購的手寫輸入，例如西方語言和某些東亞語言。

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**
</dt> <dd>

支援以左方和向下順序書寫輸入，例如在希伯來文和阿拉伯文語言中。

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**
</dt> <dd>

支援以向下和向下順序書寫輸入，例如在某些東亞語言中。

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**
</dt> <dd>

支援以向下和向右書寫的手寫輸入，例如在某些東亞語言中。

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**
</dt> <dd>

支援以任意角度書寫的文字。

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC \_ >lattice**
</dt> <dd>

支援傳回 >lattice 做為手寫辨識結果的替代字串。

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**
</dt> <dd>

支援中斷背景識別，例如當筆墨變更時。

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**
</dt> <dd>

支援將筆劃順序（空間和時態性）視為辨識作業的一部分來處理。 在將筆墨傳送至 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)之前， [**IInkAnalyzer**](iinkanalyzer.md)不會重新排列筆劃的順序。

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC 可 \_ 個人化**
</dt> <dd>

支援個人化手寫，辨識器會在一段時間內公開給相同的手寫時，改善辨識。

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**
</dt> <dd>

在將筆墨傳送至 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)之前， [**IInkAnalyzer**](iinkanalyzer.md)不需要將手寫旋轉為水準方向。

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PrefersParagraphBreaking**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)應該將筆跡的整個段落傳送至 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)，讓 **IInkAnalysisRecognizer** 能夠進行斷詞和單字 (或字元) 中斷。

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**
</dt> <dd>

每次辨識作業只能辨識一個單字或字元。 [**IInkAnalyzer**](iinkanalyzer.md)會對手寫執行分割，並且一次只傳送一個區段給 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉允許其成員值的位元組合。 使用這個列舉來尋找已安裝的筆跡辨識器，以支援您需要的屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




