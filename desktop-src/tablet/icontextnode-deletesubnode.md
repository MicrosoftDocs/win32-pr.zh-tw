---
description: 移除子 ICoNtextNode。
ms.assetid: ed1d7b35-f6ba-4eff-888d-5cc492f02832
title: 'ICoNtextNode：:D eleteSubNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0ebad42f02ccfad0db2d119832f3495819ac18ce321d72ede3aa8d7545b999be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057878"
---
# <a name="icontextnodedeletesubnode-method"></a>ICoNtextNode：:D eleteSubNode 方法

移除子 [**ICoNtextNode**](icontextnode.md)。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteSubNode(
  [in] IContextNode *pContextNodeToDelete
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtextNodeToDelete* \[在\]
</dt> <dd>

要移除的 [**ICoNtextNode**](icontextnode.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

\_如果 *pCoNtextNodeToDelete* 參數不是這個 [**ICoNtextNode**](icontextnode.md)物件的子系，則會傳回 E INVALIDARG。

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

[**ICoNtextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




