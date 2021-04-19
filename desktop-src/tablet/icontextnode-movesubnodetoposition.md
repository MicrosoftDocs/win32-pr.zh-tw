---
description: 將指定的子 ICoNtextNode 物件重新排序為指定的索引。
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'ICoNtextNode：： MoveSubNodeToPosition 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972869"
---
# <a name="icontextnodemovesubnodetoposition-method"></a>ICoNtextNode：： MoveSubNodeToPosition 方法

將指定的子 [**ICoNtextNode**](icontextnode.md) 物件重新排序為指定的索引。

## <a name="syntax"></a>語法


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSubnodeToMove* \[在\]
</dt> <dd>

要移動的 [**ICoNtextNode**](icontextnode.md) 物件。

</dd> <dt>

*ulNewIndex* \[在\]
</dt> <dd>

子節點新位置的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果 *pSubnodeToMove* 不是此 [**ICoNtextNode**](icontextnode.md)的子節點，則傳回 **E \_ INVALIDARG** 。

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

[**ICoNtextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




