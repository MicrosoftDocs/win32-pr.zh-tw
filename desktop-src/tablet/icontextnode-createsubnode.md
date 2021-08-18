---
description: 建立新的子 ICoNtextNode 物件。
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'ICoNtextNode：： CreateSubNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c7b4bc39431d6b4608586e60bdeffb7cd6c79bf95f944e436c16a683e24e634d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092309"
---
# <a name="icontextnodecreatesubnode-method"></a>ICoNtextNode：： CreateSubNode 方法

建立新的子 [**ICoNtextNode**](icontextnode.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNodeType* \[在\]
</dt> <dd>

**GUID** ，代表要建立的 [**ICoNtextNode**](icontextnode.md)類型。

</dd> <dt>

*ppCoNtextNodeCreated* \[擴展\]
</dt> <dd>

新 [**ICoNtextNode**](icontextnode.md)的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點時，請在 *ppCoNtextNodeCreated* 上呼叫 IUnknown：： Release。

 

新的 [**ICoNtextNode**](icontextnode.md) 會加入至此內容節點的子節點集合 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)) 。 當有現有的子節點時，新建立的 **ICoNtextNode** 會加入做為最後一個子節點。

如需內容節點類型的清單，請參閱 [內容節點類型](context-node-types.md)。

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

[**ICoNtextNode：:D eleteSubNode**](icontextnode-deletesubnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

