---
description: 抓取 IInkAnalysisRecognizer 的廠商名稱。
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'IInkAnalysisRecognizer：： GetVendor 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113357"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a>IInkAnalysisRecognizer：： GetVendor 方法

抓取 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的廠商名稱。

## <a name="syntax"></a>語法


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbstrVendor* \[擴展\]
</dt> <dd>

廠商的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) \* 當您不再需要使用字串時，請在 *pbstrVendor* 上呼叫 SysFreeString。

 

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

 

