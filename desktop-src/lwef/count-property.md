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
# <a name="count-property"></a><span data-ttu-id="bc7fb-103">Count 屬性</span><span class="sxs-lookup"><span data-stu-id="bc7fb-103">Count Property</span></span>

<span data-ttu-id="bc7fb-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bc7fb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bc7fb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="bc7fb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bc7fb-106">傳回 Long 整數 (唯讀屬性) ，以指定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的 [**命令**](/windows/desktop/lwef/the-command-object)物件計數。</span><span class="sxs-lookup"><span data-stu-id="bc7fb-106">Returns a Long integer (read-only property) that specifies the count of [**Command**](/windows/desktop/lwef/the-command-object) objects in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="bc7fb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="bc7fb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bc7fb-108">*代理程式 ***。 ( "*** CharacterID \* \* *" ) 的字元數**</span><span class="sxs-lookup"><span data-stu-id="bc7fb-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Count*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc7fb-109">備註</span><span class="sxs-lookup"><span data-stu-id="bc7fb-109">Remarks</span></span>

<span data-ttu-id="bc7fb-110">**計數** 只包含您在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中定義的 [**命令**](/windows/desktop/lwef/the-command-object)物件數目。</span><span class="sxs-lookup"><span data-stu-id="bc7fb-110">**Count** includes only the number of [**Command**](/windows/desktop/lwef/the-command-object) objects you define in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="bc7fb-111">不包含伺服器或其他用戶端專案。</span><span class="sxs-lookup"><span data-stu-id="bc7fb-111">Server or other client entries are not included.</span></span>

 

 