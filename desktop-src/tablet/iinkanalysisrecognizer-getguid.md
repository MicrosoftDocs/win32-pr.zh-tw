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
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848087"
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
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




