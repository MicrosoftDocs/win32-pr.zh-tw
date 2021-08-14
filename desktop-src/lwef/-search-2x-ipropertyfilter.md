---
title: 'IPropertyFilter 介面 (WdsSharedIDL .h) '
description: 公開用來篩選查詢的屬性。
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- IPropertyFilter 介面舊版 Windows 環境功能
- IPropertyFilter 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5bc406661492702e4a012cab58a2e0a3e08507aeaa13d10b010f14ce31e6fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481092"
---
# <a name="ipropertyfilter-interface"></a>IPropertyFilter 介面

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

公開用來篩選查詢的屬性。

## <a name="members"></a>成員

**IPropertyFilter** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPropertyFilter** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IPropertyFilter** 介面具有這些屬性。



| 屬性                                                                                      | 存取類型           | Description                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter::IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | 讀取/寫入<br/> | 要篩選之屬性的索引資料行名稱。 <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | 讀取/寫入<br/> | 套用篩選時要使用的邏輯運算子。 <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | 讀取/寫入<br/> | 篩選一組嵌套括弧內的深度。 <br/> |
| [**IPropertyFilter：： Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | 讀取/寫入<br/> | 篩選準則的文字。 <br/>                               |
| [**IPropertyFilter：： UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | 讀取/寫入<br/> | 要篩選之屬性的 UID。 <br/>                 |



 

## <a name="remarks"></a>備註

這些屬性是用來篩選查詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>                                               |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

