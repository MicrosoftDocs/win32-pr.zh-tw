---
description: 抓取值，這個值會指出是否已在此 ICoNtextNode 上設定傳遞給這個方法的 ConfirmationType。
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'ICoNtextNode：： IsConfirmed 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2e378aaf344e177514115c82b1179f8d1ebe25faefa0d5d840d5a0af62ff1c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967357"
---
# <a name="icontextnodeisconfirmed-method"></a>ICoNtextNode：： IsConfirmed 方法

抓取值，這個值會指出是否已在此 ICoNtextNode 上設定傳遞給這個方法的 ConfirmationType。

## <a name="syntax"></a>語法


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*confirmedType* \[在\]
</dt> <dd>

要測試的確認類型。

</dd> <dt>

*pfTypeConfirmed* \[擴展\]
</dt> <dd>

**變異 \_** 如果已在這個 [**ICoNtextNode**](icontextnode.md)物件上設定 confirmedType 傳遞的型別，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

這個值是由 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md) 方法設定。

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
</dt> <dt>

[**ICoNtextNode：： Confirm**](icontextnode-confirm.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




