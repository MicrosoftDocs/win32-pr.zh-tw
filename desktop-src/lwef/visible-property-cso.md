---
title: 'Visible 屬性 (命令物件) '
description: Visible 屬性
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383738"
---
# <a name="visible-property-commands-object"></a>Visible 屬性 (命令物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定值，這個值會決定 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的標題是否出現在字元的快顯功能表中。

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法** 
</dt> <dd>

*代理程式 ***。 (**"* CharacterID *" * * ) 的字元。可見的* *  \[  =  *布林值*\]



| 部分      | 描述                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 布林運算式，指定您的 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件是否出現在字元的快顯功能表中。 <br/> **True** 標題隨即出現。<br/> **False** 標題不會出現。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

當您的應用程式不是輸入-主動用戶端時，標題會出現在字元的快顯功能表中，必須將這個屬性設定為 **True** ，並針對您的命令集合設定 [**caption**](caption-property.md) 屬性。 此外，當您的應用程式為輸入-主動時，您集合中的命令也必須將此屬性設定為 **True** ，才會出現在快顯功能表中。

 

