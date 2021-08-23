---
description: 指出這個 ICoNtextNode 的已辨識字串來自系統字典、使用者字典或字組清單。
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'ICoNtextNode：： IsStringSupported 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2eef383f059897665c013e3575d452564295ccd9bd014ae8084fd1635892bd99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709108"
---
# <a name="icontextnodeisstringsupported-method"></a>ICoNtextNode：： IsStringSupported 方法

指出這個 [**ICoNtextNode**](icontextnode.md) 的已辨識字串來自系統字典、使用者字典或字組清單。

## <a name="syntax"></a>語法


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pfIsSupported* \[退出，retval\]
</dt> <dd>

**變異 \_** 如果 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)支援此 [**ICoNtextNode**](icontextnode.md)的可辨識字串值，且已套用任何對應的提示節點，則為 TRUE。否則， **VARIANT \_ FALSE**。

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

[**ICoNtextNode**](icontextnode.md)
</dt> </dl>

 

 




