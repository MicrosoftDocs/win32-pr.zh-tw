---
description: 抓取這個集合中的 IInkAnalysisRecognizer 物件數目。
ms.assetid: dfb5c530-b481-4c60-b7fe-87fe162de270
title: 'IInkAnalysisRecognizers：： GetCount 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e65f8399c661d551e805abe5f1c5db33eb0b154a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511668"
---
# <a name="iinkanalysisrecognizersgetcount-method"></a>IInkAnalysisRecognizers：： GetCount 方法

抓取這個集合中的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulCount* \[退出，retval\]
</dt> <dd>

這個集合中的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件數目。

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

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




