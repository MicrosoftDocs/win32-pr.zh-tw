---
description: 管理文字輸入面板自動完成整合的應用程式端。
ms.assetid: 02601258-d867-4c01-b094-bf9ff96d2f6e
title: 'ITipAutocompleteProvider 介面 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 66c1e38c419e7eb37745864b447249d55b384b6c832293bd3fab4d0cc171e0fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031866"
---
# <a name="itipautocompleteprovider-interface"></a>ITipAutocompleteProvider 介面

管理文字輸入面板自動完成整合的應用程式端。

## <a name="members"></a>成員

**ITipAutocompleteProvider** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITipAutocompleteProvider** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITipAutocompleteProvider** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                                          |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**顯示**](itipautocompleteprovider-show.md)                           | 顯示或隱藏自動完成清單。<br/>                                                                 |
| [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md) | 由自動完成用戶端用來通知應用程式使用者已筆跡輸入面板中的文字。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                       |
| 標頭<br/>                   | <dl> <dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> <dt>

[**ITipAutocompleteClient 介面**](itipautocompleteclient.md)
</dt> </dl>

 

