---
description: 可讓用戶端呼叫應用程式的文字輸入面板自動完成提供者物件。
ms.assetid: 448b8136-ebcb-4116-9a81-a77a37d69e24
title: 'ITipAutocompleteClient 介面 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: dac9b1a6c581be8a8fb19df4f812a5866403d949d19739bb8ae99a0fffbe5e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590288"
---
# <a name="itipautocompleteclient-interface"></a>ITipAutocompleteClient 介面

可讓用戶端呼叫應用程式的文字輸入面板自動完成提供者物件。

## <a name="members"></a>成員

**ITipAutocompleteClient** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITipAutocompleteClient** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITipAutocompleteClient** 介面具有這些方法。



| 方法                                                              | 描述                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdviseProvider**](itipautocompleteclient-adviseprovider.md)     | 向用戶端註冊提供者，以讓用戶端呼叫應用程式的自動完成提供者物件。<br/>                                      |
| [**PreferredRects**](itipautocompleteclient-preferredrects.md)     | 允許用戶端建議在何處放置自動完成清單，以避免重迭輸入面板。<br/>                                               |
| [**RequestShowUI**](itipautocompleteclient-requestshowui.md)       | 決定輸入面板是否已準備好顯示自動完成清單。<br/>                                                                             |
| [**UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) | 取消註冊相關聯的提供者。<br/>                                                                                                                      |
| [**UserSelection**](itipautocompleteclient-userselection.md)       | 通知輸入面板，使用者已在自動完成清單中選取某個內容，並捨棄尚未插入的所有剩餘文字。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                       |
| 標頭<br/>                   | <dl> <dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



 

