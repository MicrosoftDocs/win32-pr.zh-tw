---
description: 抓取辨識器 (GUID) 的全域唯一識別碼。
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'IInkAnalysisRecognizer：： GetGuid 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b5fbf2b07b2a63f2fdb088c38a5e03e4182c4e38528208c039f927b282755344
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596738"
---
# <a name="iinkanalysisrecognizergetguid-method"></a>IInkAnalysisRecognizer：： GetGuid 方法

抓取辨識器 (GUID) 的全域唯一識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pId* \[擴展\]
</dt> <dd>

識別此 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的 GUID。

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

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




