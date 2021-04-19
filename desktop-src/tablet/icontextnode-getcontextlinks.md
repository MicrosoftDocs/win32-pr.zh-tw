---
description: 抓取 ICoNtextLink 物件的集合，這些物件表示與其他 ICoNtextNode 物件的關聯性。
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'ICoNtextNode：： GetCoNtextLinks 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991745"
---
# <a name="icontextnodegetcontextlinks-method"></a>ICoNtextNode：： GetCoNtextLinks 方法

抓取 [**ICoNtextLink**](icontextlink.md) 物件的集合，這些物件表示與其他 [**ICoNtextNode**](icontextnode.md) 物件的關聯性。

## <a name="syntax"></a>語法


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppCoNtextLinks* \[擴展\]
</dt> <dd>

[**ICoNtextLink**](icontextlink.md)物件集合的指標，表示與其他 [**ICoNtextNode**](icontextnode.md)物件的關聯性。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要使用內容連結集合時，請在 *ppCoNtextLinks* 上呼叫 IUnknown：： Release。

 

若要取得父節點或子節點關聯性的相關資訊，請使用 [**ICoNtextNode：： GetParentNode**](icontextnode-getparentnode.md) 或 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md)。

如需連結所描述之關聯性類型的詳細資訊，請參閱 [**ICoNtextLink**](icontextlink.md) 和 [**CoNtextLinkDirection**](contextlinkdirection.md)。

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

[**CoNtextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**ICoNtextNode::AddCoNtextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

