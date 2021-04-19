---
description: 指出指定的已辨識字串是否來自系統字典、使用者字典或字組清單。
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'ICoNtextNode：： IsAlternateStringSupported 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991744"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>ICoNtextNode：： IsAlternateStringSupported 方法

指出指定的已辨識字串是否來自系統字典、使用者字典或字組清單。 任何對應的提示節點中的任何限制資料（例如 wordlists、輔助線或 factoids），都將用來判斷是否支援字串。

## <a name="syntax"></a>語法


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrAlternateString* \[在\]
</dt> <dd>

已辨識要驗證的字串。

</dd> <dt>

*pfIsSupported* \[擴展\]
</dt> <dd>

**變異 \_** 如果 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)支援指定的字串，且已套用任何對應的提示節點，則為 TRUE;**變異 \_** 如果不支援，則為 FALSE。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> </dl>

 

 




