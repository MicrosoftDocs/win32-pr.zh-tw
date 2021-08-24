---
description: 指定筆跡分析期間可能發生的可用警告集。
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: 'AnalysisWarningCode 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 48d03c0f4c479ddf6a3f1f9f371bc13b889641994f86df75b107b17ca081a97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660868"
---
# <a name="analysiswarningcode-enumeration"></a>AnalysisWarningCode 列舉

指定筆跡分析期間可能發生的可用警告集。

## <a name="syntax"></a>Syntax


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode 已 \_ 中止**
</dt> <dd>

分析作業已中止。

只有在呼叫同步分析作業時才會傳回。 中止非同步作業並不會引發 [**\_ IAnalysisEvents：： Results**](-ianalysisevents-results.md)事件。

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)找不到符合執行分析作業所需之語言或功能需求的筆墨辨識器。

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**
</dt> <dd>

筆墨辨識器無法遵循分析提示節點上指定的模擬程式集 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**
</dt> <dd>

筆墨辨識器無法將其結果強制轉換為分析提示節點上指定的模擬程式集 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**
</dt> <dd>

筆墨辨識器無法遵循分析提示節點上的指定指南集 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**
</dt> <dd>

筆墨辨識器無法遵循分析提示節點上指定的單字清單集 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**
</dt> <dd>

筆墨辨識器無法遵循在分析提示節點上設定的指定 word 模式 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [analysis 提示屬性](analysis-hint-properties.md)) 。

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**
</dt> <dd>

表示無法從 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)傳回部分字典詞彙。

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**
</dt> <dd>

指出文字辨識進程失敗。

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**
</dt> <dd>

無法將筆墨新增至 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)。 例如，在筆勢辨識器上將從滑鼠收集的筆劃新增至會失敗，因為手勢辨識器需要從數位板收集的筆觸。

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)無法遵守分析提示節點的指定前置詞或後置詞文字 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)和 [analysis 提示屬性](analysis-hint-properties.md)) 。

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)無法在 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)上具現化、複製或設定筆觸。

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**
</dt> <dd>

指出使用者已確認 [**ICoNtextNode**](icontextnode.md) 物件，但未針對該節點計算任何辨識值。

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**
</dt> <dd>

背景作業未完成，因為發生例外狀況。 這是嚴重的錯誤，需要重新具現化 [**IInkAnalyzer**](iinkanalyzer.md) ，然後再進一步使用。

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ CoNtextNodeLocationNotSet**
</dt> <dd>

指出 [**ICoNtextNode**](icontextnode.md) 物件沒有適當的位置集 (請參閱 [**ICoNtextNode：： SetLocation**](icontextnode-setlocation.md)) 。 除非 **ICoNtextNode** 物件標示為部分填入，否則 [**ICoNtextNode：： GetLocation**](icontextnode-getlocation.md)方法必須傳回非空白值。

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**
</dt> <dd>

在與自訂辨識器節點相關聯的筆劃上設定的語言識別項 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 不符合所使用之 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 的語言識別項。 具有指定 **IInkAnalysisRecognizer** 的筆墨仍能辨識。

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)不支援依照指定啟用 Unicode 字元範圍。

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)只會支援 TopInkBreaks，即使提示只包含 TopInkBreaks 的要求也是一樣。

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)已在執行背景分析。

</dd> </dl>

## <a name="remarks"></a>備註

**AnalysisWarningCode \_BackgroundException** 是唯一需要先重新具現化 [**IInkAnalyzer**](iinkanalyzer.md) 物件，再進一步使用的警告程式碼值。

其他警告程式碼值（例如 **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** 和 **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**）可能需要 [**IInkAnalyzer**](iinkanalyzer.md) 物件使用不同的辨識器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




