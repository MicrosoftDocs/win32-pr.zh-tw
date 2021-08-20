---
description: 將新的 ICoNtextLink 加入至 ICoNtextNode 物件的內容連結集合。
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'ICoNtextNode：： AddCoNtextLink 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 515ade35baed591060e76818d2b3e00a3654a89a9d42dda21d170ee54b2773ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967437"
---
# <a name="icontextnodeaddcontextlink-method"></a>ICoNtextNode：： AddCoNtextLink 方法

將新的 [**ICoNtextLink**](icontextlink.md) 加入至 [**ICoNtextNode**](icontextnode.md) 物件的內容連結集合。

## <a name="syntax"></a>語法


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDestinationNode* \[在\]
</dt> <dd>

新 [**ICoNtextLink**](icontextlink.md)的目的地 [**ICoNtextNode**](icontextnode.md) 。

</dd> <dt>

*linkDirection* \[在\]
</dt> <dd>

要建立之 [**ICoNtextLink**](icontextlink.md) 物件的方向。

</dd> <dt>

*ppCoNtextLinkToAdd* \[擴展\]
</dt> <dd>

新 [**ICoNtextLink**](icontextlink.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容節點時，請在 *ppCoNtextLinkToAdd* 上呼叫 IUnknown：： Release。

 

這個 [**ICoNtextNode**](icontextnode.md) 物件是來源節點 (請參閱 [**ICoNtextLink：： GetSourceNode**](icontextlink-getsourcenode.md)) 以取得新的 [**ICoNtextLink**](icontextlink.md) 物件。

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

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**ICoNtextLinks**](icontextlinks.md)
</dt> <dt>

[**CoNtextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**ICoNtextNode：:D eleteCoNtextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**ICoNtextNode::GetCoNtextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

