---
description: 抓取 ICoNtextNode 物件內筆劃的識別碼陣列。
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'ICoNtextNode：： GetStrokeIds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113384"
---
# <a name="icontextnodegetstrokeids-method"></a>ICoNtextNode：： GetStrokeIds 方法

抓取 [**ICoNtextNode**](icontextnode.md) 物件內筆劃的識別碼陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulStrokeIdsCount* \[in、out\]
</dt> <dd>

筆劃的數目。 未使用傳入的值。

</dd> <dt>

*pplStrokes* \[擴展\]
</dt> <dd>

這個 [**ICoNtextNode**](icontextnode.md) 物件之筆觸識別碼陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *pplStrokes* 的記憶體。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ICoNtextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**ICoNtextNode::GetStrokeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

