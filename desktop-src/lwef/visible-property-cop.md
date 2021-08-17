---
title: 'Visible 屬性 (Command 物件) '
description: 瞭解 Command 物件的 Visible 屬性，它會傳回或設定命令是否顯示在字元的快顯功能表中。
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ebc5dee52ff3ab388674bd844e476f0bcc768595b1ba5e69d3c3be5435553f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975458"
---
# <a name="visible-property-command-object"></a>Visible 屬性 (Command 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定 [**命令**](/windows/desktop/lwef/the-command-object) 是否顯示在字元的快顯功能表中。

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法** 
</dt> <dd>

*代理程式 ***。字元 (**"* CharacterID *"**) . 命令 (**"* name *" * * ) 。可見* 的 *  \[  =  *布林值*\]



| 部分      | 描述                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 布林運算式，指定是否要在字元的快顯功能表中出現 [**命令**](/windows/desktop/lwef/the-command-object)的標題。<br/> **True** (預設) 標題隨即出現。<br/> **False** 標題不會出現。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

當您想要包含自己介面的語音輸入，而不將其顯示在字元的快顯功能表中時，請將此屬性設定為 **False** 。 如果您將 [**命令**](/windows/desktop/lwef/the-command-object) 物件的 [**Caption**](caption-property.md) 屬性設為空字串 ( "" ) ，標題文字就不會出現在快顯功能表中 (例如，不論它的 [**Visible**](visible-property.md) 屬性設定為何，都不會出現在快顯功能表中例如空白行) 。

[**命令**](/windows/desktop/lwef/the-command-object)物件之父 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**visible**](visible-property.md)屬性設定，不會影響 **命令** 的 **visible** 屬性設定。

 

