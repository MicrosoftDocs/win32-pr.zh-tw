---
description: 表示兩個 ICoNtextNode 物件之間的關聯性。
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: 'ICoNtextLink 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7dc9244fed59604a56817f15801de94b64c476762e186cc6f7c36186e8d0b26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719912"
---
# <a name="icontextlink-interface"></a>ICoNtextLink 介面

表示兩個 [**ICoNtextNode**](icontextnode.md) 物件之間的關聯性。

## <a name="members"></a>成員

**ICoNtextLink** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ICoNtextLink** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ICoNtextLink** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetCoNtextLinkDirection**](icontextlink-getcontextlinkdirection.md) | 抓取這個 **ICoNtextLink** 所代表的關聯性類型。<br/>                                         |
| [**GetDestinationNode**](icontextlink-getdestinationnode.md)           | 抓取 [**ICoNtextNode**](icontextnode.md) 物件，此物件為這個 **ICoNtextLink** 的目的地。<br/> |
| [**GetSourceNode**](icontextlink-getsourcenode.md)                     | 抓取 [**ICoNtextNode**](icontextnode.md) 物件，此物件為這個 **ICoNtextLink** 的來源。<br/>      |



 

## <a name="remarks"></a>備註

以下是 **ICoNtextLink** 物件所代表的關聯性範例：

-   在筆跡分析中使用 AnalysisHint 節點時，筆跡分析作業會在 [分析提示] 節點和包含在提示區域內寫入的節點之間，建立類型為 AnalysisHint 的 **ICoNtextLink** 物件。 來源節點是分析提示節點，而目的地節點則是包含寫入的節點。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode::GetCoNtextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[**ICoNtextLinks**](icontextlinks.md)
</dt> <dt>

[**CoNtextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
</dt> </dl>

 

