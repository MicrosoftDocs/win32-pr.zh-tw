---
description: 包含物件的集合，這些物件會執行 ICoNtextNode 介面，且為筆跡分析作業的結果。
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: 'ICoNtextNodes 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972052"
---
# <a name="icontextnodes-interface"></a>ICoNtextNodes 介面

包含物件的集合，這些物件會執行 [**ICoNtextNode**](icontextnode.md) 介面，且為筆跡分析作業的結果。

## <a name="members"></a>成員

**ICoNtextNodes** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ICoNtextNodes** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ICoNtextNodes** 介面具有這些方法。



| 方法                                                       | 描述                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**AddCoNtextNode**](icontextnodes-addcontextnode.md)       | 將 [**ICoNtextNode**](icontextnode.md) 物件加入至此集合。 <br/>                                  |
| [**GetCoNtextNode**](icontextnodes-getcontextnode.md)       | 在此集合中的指定索引處，抓取 [**ICoNtextNode**](icontextnode.md) 物件。 <br/> |
| [**GetCount**](icontextnodes-getcount.md)                   | 抓取此集合中包含的 [**ICoNtextNode**](icontextnode.md) 物件數目。 <br/>       |
| [**RemoveCoNtextNode**](icontextnodes-removecontextnode.md) | 從此集合移除 [**ICoNtextNode**](icontextnode.md) 物件。 <br/>                             |



 

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

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

