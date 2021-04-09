---
title: Count 屬性
description: Count 屬性
ms.assetid: a0375aa9-495d-47be-a3f7-4d5987688555
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 630817a8370a071851216ab03d43493e672b3e0a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842167"
---
# <a name="count-property"></a>Count 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回 Long 整數 (唯讀屬性) ，以指定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的 [**命令**](/windows/desktop/lwef/the-command-object)物件計數。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "*** CharacterID * * *" ) 的字元數**

</dd> </dl>

## <a name="remarks"></a>備註

**計數** 只包含您在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中定義的 [**命令**](/windows/desktop/lwef/the-command-object)物件數目。 不包含伺服器或其他用戶端專案。

 

 