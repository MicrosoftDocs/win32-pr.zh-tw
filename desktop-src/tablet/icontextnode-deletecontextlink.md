---
description: 從 ICoNtextNode 物件的連結集合中刪除 ICoNtextLink 物件。
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: 'ICoNtextNode：:D eleteCoNtextLink 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973858"
---
# <a name="icontextnodedeletecontextlink-method"></a>ICoNtextNode：:D eleteCoNtextLink 方法

從 [**ICoNtextNode**](icontextnode.md)物件的連結集合中刪除 [**ICoNtextLink**](icontextlink.md)物件。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtextLinkToDelete* \[在\]
</dt> <dd>

要刪除的 [**ICoNtextLink**](icontextlink.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

內容連結具有來源節點和目的地節點 (請參閱 [**ICoNtextLink：： GetSourceNode**](icontextlink-getsourcenode.md) 和 [**ICoNtextLink：： GetDestinationNode**](icontextlink-getdestinationnode.md)) 。 這個方法會從來源和目的地節點的內容連結集合中移除 [**ICoNtextLink**](icontextlink.md) ， (參閱 [**ICoNtextNode：： GetCoNtextLinks**](icontextnode-getcontextlinks.md)) 。

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

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**ICoNtextNode::AddCoNtextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**ICoNtextNode::GetCoNtextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




