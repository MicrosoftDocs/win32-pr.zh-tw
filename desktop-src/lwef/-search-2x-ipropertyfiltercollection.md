---
title: 'IPropertyFilterCollection 介面 (WdsSharedIDL .h) '
description: 根據提交的查詢，公開傳回之集合的屬性。
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- IPropertyFilterCollection 介面舊版 Windows 環境功能
- IPropertyFilterCollection 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69fb2f7ce6e100c74046f3402eee3385108723202fbaa6dce01e888bffef4b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349978"
---
# <a name="ipropertyfiltercollection-interface"></a>IPropertyFilterCollection 介面

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在更新版本中，請改用[Windows Search API](../search/-search-reference-entry-page.md) 。 

根據提交的查詢，公開傳回之集合的屬性。

## <a name="members"></a>成員

**IPropertyFilterCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPropertyFilterCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IPropertyFilterCollection** 介面具有這些屬性。



| 屬性                                                                         | 存取類型           | 描述                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**AddItem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | 唯讀<br/>  | 將新的篩選準則加入至集合。 <br/>             |
| [**清楚**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | 唯寫<br/> | 清除集合。 <br/>                           |
| [**計數**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | 唯讀<br/>  | 集合中的篩選數目。 <br/>             |
| [**GetITem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | 讀取/寫入<br/> | 傳回集合中的特定篩選。 <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | 唯寫<br/> | 移除集合中的特定篩選。 <br/>     |



 

## <a name="remarks"></a>備註

這些屬性是用來篩選查詢所傳回的集合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows只有 Server 2003 （含 SP1） \[ 桌面應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>                                               |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

