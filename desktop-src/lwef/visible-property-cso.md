---
title: 'Visible 屬性 (命令物件) '
description: 瞭解命令物件的 Visible 屬性，判斷命令集合的標題是否出現在字元的快顯功能表中。
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c742733d06f0a4c7ae2d10c7fb97a20e735b59370c61efa5f7204003f1cd81bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975468"
---
# <a name="visible-property-commands-object"></a>Visible 屬性 (命令物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

