---
description: 抓取此 IInkAnalysisRecognizer 支援之地區設定的識別碼。
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'IInkAnalysisRecognizer：： GetLanguages 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a94b85dfe9a6b5dbbd755ff1e0a4cf2d68dccd5178da6d0578d6f50e8b48936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350968"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>IInkAnalysisRecognizer：： GetLanguages 方法

抓取此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 支援之地區設定的識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulLanguagesCount* \[in、out\]
</dt> <dd>

*PpulLanguages* 中的識別碼數目。

</dd> <dt>

*ppulLanguages* \[擴展\]
</dt> <dd>

此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 支援之地區設定的識別碼指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppulLanguages* 的記憶體。

 

這個方法會傳回物件和手勢辨識器的空陣列。

如需語言識別項的詳細資訊，請參閱 [語言識別項常數和字串](/windows/desktop/Intl/language-identifier-constants-and-strings)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

