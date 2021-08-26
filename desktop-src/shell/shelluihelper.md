---
description: 由 shell 所執行，以協助編寫腳本和 Microsoft Visual Basic 開發人員使用 shell 中提供的一些功能。 ShellUIHelper 物件沒有任何屬性或事件。 提供方法以將專案新增至 Shell。
title: 'ShellUIHelper 物件 (Exdisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f254bd218024b3d1df15a826da701b1f010ae616
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473324"
---
# <a name="shelluihelper-object"></a>ShellUIHelper 物件

由 shell 所執行，以協助編寫腳本和 Microsoft Visual Basic 開發人員使用 shell 中提供的一些功能。 **ShellUIHelper** 物件沒有任何屬性或事件。 提供方法以將專案新增至 Shell。

## <a name="members"></a>成員

**ShellUIHelper** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ShellUIHelper** 物件有這些方法。




| 方法 | 描述 | 
|--------|-------------|
| <a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a> | 將新通道新增至 [我 Internet Explorer 的最愛 <strong>]</strong> 功能表中的通道清單和桌面上的 <strong>頻道</strong> 列。<br /><blockquote>[!Note]<br />Windows Vista 下已不再支援此方法。 在該作業系統下，它會傳回 E_NOTIMPL。</blockquote><br /> | 
| <a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a> | 將專案加入至 Active Desktop。<br /> | 
| <a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a> | 顯示用來建立我的最愛專案的預設使用者介面。 使用者介面會初始化為指定的參數。<br /> | 
| <a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a> | 指出是否已訂閱指定的 URL。<br /> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Exdisp。h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




