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
# <a name="defaultcommand-property"></a><span data-ttu-id="a127d-103">DefaultCommand 屬性</span><span class="sxs-lookup"><span data-stu-id="a127d-103">DefaultCommand Property</span></span>

<span data-ttu-id="a127d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a127d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a127d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="a127d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a127d-106">傳回或設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件的預設命令。</span><span class="sxs-lookup"><span data-stu-id="a127d-106">Returns or sets the default command of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span>

</dd> <dt>

<span data-ttu-id="a127d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="a127d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a127d-108">*agent. \* \* \* 字元* \* **( "***CharacterID***" ) DefaultCommand** \[  =  *字串*\]</span><span class="sxs-lookup"><span data-stu-id="a127d-108">*agent.\*\*\*Characters*\* **("***CharacterID***").Commands.DefaultCommand** \[ = *string*\]</span></span>



| <span data-ttu-id="a127d-109">部分</span><span class="sxs-lookup"><span data-stu-id="a127d-109">Part</span></span>     | <span data-ttu-id="a127d-110">描述</span><span class="sxs-lookup"><span data-stu-id="a127d-110">Description</span></span>                                                                         |
|----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a127d-111">*string*</span><span class="sxs-lookup"><span data-stu-id="a127d-111">*string*</span></span> | <span data-ttu-id="a127d-112">字串值，識別 [**命令**](/windows/desktop/lwef/the-command-object) (識別碼) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a127d-112">A string value identifying the name (ID) of the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a127d-113">備註</span><span class="sxs-lookup"><span data-stu-id="a127d-113">Remarks</span></span>

<span data-ttu-id="a127d-114">這個屬性可 [**讓您將命令集合中**](/windows/desktop/lwef/the-commands-collection-object)的 [**命令**](/windows/desktop/lwef/the-command-object)設定為預設命令，並以粗體呈現。</span><span class="sxs-lookup"><span data-stu-id="a127d-114">This property enables you to set a [**Command**](/windows/desktop/lwef/the-command-object) in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection as the default command, rendering it bold.</span></span> <span data-ttu-id="a127d-115">這並不會實際變更命令處理或按兩下事件。</span><span class="sxs-lookup"><span data-stu-id="a127d-115">This does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="a127d-116">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="a127d-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 