---
description: 取得 IAnalysisAlternate 物件的已識別字串值。
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'IAnalysisAlternate：： GetRecognizedString 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79d0967d2653a68145a9a50c34134d176d78674c5ea5729230035edd65a5e6b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008488"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a>IAnalysisAlternate：： GetRecognizedString 方法

取得 [**IAnalysisAlternate**](ianalysisalternate.md) 物件的已識別字串值。

## <a name="syntax"></a>語法


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbstrRecognizedString* \[擴展\]
</dt> <dd>

設為可辨識之字串值的 **BSTR** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer：： GetRecognizedString 方法**](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




