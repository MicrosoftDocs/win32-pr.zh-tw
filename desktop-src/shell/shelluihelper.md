---
description: 由 Shell 所執行，以協助編寫腳本和 Microsoft Visual Basic 開發人員使用 Shell 中提供的一些功能。 ShellUIHelper 物件沒有任何屬性或事件。 提供方法以將專案新增至 Shell。
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
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973732"
---
# <a name="shelluihelper-object"></a>ShellUIHelper 物件

由 Shell 所執行，以協助編寫腳本和 Microsoft Visual Basic 開發人員使用 Shell 中提供的一些功能。 **ShellUIHelper** 物件沒有任何屬性或事件。 提供方法以將專案新增至 Shell。

## <a name="members"></a>成員

**ShellUIHelper** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ShellUIHelper** 物件有這些方法。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">方法</th>
<th style="text-align: left;">描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></td>
<td style="text-align: left;">將新通道新增至 [我 Internet Explorer 的最愛 <strong>]</strong> 功能表中的通道清單和桌面上的 <strong>頻道</strong> 列。<br/>
<blockquote>
[!Note]<br />
Windows Vista 下已不再支援此方法。 在該作業系統下，它會傳回 E_NOTIMPL。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></td>
<td style="text-align: left;">將專案加入至 Active Desktop。<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></td>
<td style="text-align: left;">顯示用來建立我的最愛專案的預設使用者介面。 使用者介面會初始化為指定的參數。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">指出是否已訂閱指定的 URL。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Exdisp。h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




