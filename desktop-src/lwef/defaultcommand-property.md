---
title: DefaultCommand 屬性
description: DefaultCommand 屬性
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023401"
---
# <a name="defaultcommand-property"></a>DefaultCommand 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件的預設命令。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. * * * 字元* * **( "***CharacterID***" ) DefaultCommand** \[  =  *字串*\]



| 部分     | 描述                                                                         |
|----------|-------------------------------------------------------------------------------------|
| *string* | 字串值，識別 [**命令**](/windows/desktop/lwef/the-command-object) (識別碼) 的名稱。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性可 [**讓您將命令集合中**](/windows/desktop/lwef/the-commands-collection-object)的 [**命令**](/windows/desktop/lwef/the-command-object)設定為預設命令，並以粗體呈現。 這並不會實際變更命令處理或按兩下事件。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

 

 