---
description: 包含物件的集合，這些物件會執行 ICoNtextLink 介面。
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: 'ICoNtextLinks 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 44eb7117fe3b01b3e31829222c6ab3f601d5bbbec8ea0591a9f80d087dcaee22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008478"
---
# <a name="icontextlinks-interface"></a>ICoNtextLinks 介面

包含物件的集合，這些物件會執行 [**ICoNtextLink**](icontextlink.md) 介面。

## <a name="members"></a>成員

**ICoNtextLinks** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ICoNtextLinks** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ICoNtextLinks** 介面具有這些方法。



| 方法                                                 | 描述                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**GetCoNtextLink**](icontextlinks-getcontextlink.md) | 抓取位於指定之索引處的 [**ICoNtextLink**](icontextlink.md) 。<br/>               |
| [**GetCount**](icontextlinks-getcount.md)             | 抓取這個集合中的 [**ICoNtextLink**](icontextlink.md) 物件數目。<br/> |



 

## <a name="remarks"></a>備註

這通常是透過 [**ICoNtextNode：： GetCoNtextLinks**](icontextnode-getcontextlinks.md) 方法來存取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**ICoNtextNode::AddCoNtextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**ICoNtextNode：:D eleteCoNtextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**ICoNtextNode::GetCoNtextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

