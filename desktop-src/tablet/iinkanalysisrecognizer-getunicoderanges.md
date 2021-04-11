---
description: 抓取字元範圍的陣列，表示支援的 Unicode 字元範圍。
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'IInkAnalysisRecognizer：： GetUnicodeRanges 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848085"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>IInkAnalysisRecognizer：： GetUnicodeRanges 方法

抓取字元範圍的陣列，表示支援的 Unicode 字元範圍。

## <a name="syntax"></a>語法


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulNumberOfRanges* \[in、out\]
</dt> <dd>

*PpulLowUnicode* 所指向的字元範圍數目。

</dd> <dt>

*ppulLowUnicode* \[擴展\]
</dt> <dd>

字元範圍陣列的指標，表示支援的 Unicode 字元範圍。

</dd> <dt>

*ppusUnicodeRangeLength* \[擴展\]
</dt> <dd>

值陣列的指標，指出每個陣列指向 *ppulLowUnicode* 的長度。

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
</dt> </dl>

 

 




