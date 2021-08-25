---
description: 抓取辨識器的名稱。
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'IInkAnalysisRecognizer：： GetName 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df86f5526a6b28f8a7f383ddfb49ca999875b8aa08c66e07a9ac95c41acd13cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773618"
---
# <a name="iinkanalysisrecognizergetname-method"></a>IInkAnalysisRecognizer：： GetName 方法

抓取辨識器的名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbstrName* \[擴展\]
</dt> <dd>

辨識器的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) \* 當您不再需要使用字串時，請在 *pbstrName* 上呼叫 SysFreeString。

 

此名稱會針對辨識器所支援的區域中立語言進行當地語系化。

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

 

