---
description: 將這個 ICoNtextNode 物件從其父內容節點的子節點集合移至指定的內容節點的子節點集合。
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'ICoNtextNode：：重做方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026254"
---
# <a name="icontextnodereparent-method"></a>ICoNtextNode：：重做方法

將這個 [**ICoNtextNode**](icontextnode.md) 物件從其父內容節點的子節點集合移至指定的內容節點的子節點集合。

## <a name="syntax"></a>語法


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNewParent* \[在\]
</dt> <dd>

這個 [**ICoNtextNode**](icontextnode.md) 物件的新父節點。

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

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ICoNtextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**ICoNtextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




