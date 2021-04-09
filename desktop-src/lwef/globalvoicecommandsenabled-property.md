---
title: GlobalVoiceCommandsEnabled 屬性
description: GlobalVoiceCommandsEnabled 屬性
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933249"
---
# <a name="globalvoicecommandsenabled-property"></a><span data-ttu-id="d4c3c-103">GlobalVoiceCommandsEnabled 屬性</span><span class="sxs-lookup"><span data-stu-id="d4c3c-103">GlobalVoiceCommandsEnabled Property</span></span>

<span data-ttu-id="d4c3c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d4c3c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d4c3c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="d4c3c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d4c3c-106">傳回或設定是否已啟用代理程式全域命令的語音。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-106">Returns or sets whether voice is enabled for Agent's global commands.</span></span>

</dd> <dt>

<span data-ttu-id="d4c3c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="d4c3c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d4c3c-108">*代理。\*\*\*字元 (*\*\* 」CharacterID \* \* \* ") GlobalVoiceCommandsEnabled\*\*</span><span class="sxs-lookup"><span data-stu-id="d4c3c-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Commands.GlobalVoiceCommandsEnabled**</span></span>

<span data-ttu-id="d4c3c-109">\[ = *布林*\]</span><span class="sxs-lookup"><span data-stu-id="d4c3c-109">\[ = *boolean*\]</span></span>



| <span data-ttu-id="d4c3c-110">部分</span><span class="sxs-lookup"><span data-stu-id="d4c3c-110">Part</span></span>      | <span data-ttu-id="d4c3c-111">描述</span><span class="sxs-lookup"><span data-stu-id="d4c3c-111">Description</span></span>                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c3c-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="d4c3c-112">*boolean*</span></span> | <span data-ttu-id="d4c3c-113">指出是否已啟用代理程式全域命令之語音參數的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-113">A Boolean expression that indicates whether voice parameters for Agent's global commands are enabled.</span></span> <span data-ttu-id="d4c3c-114">**True** (預設值) 啟用語音參數。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-114">**True** (Default) Voice parameters are enabled.</span></span> <br/> <span data-ttu-id="d4c3c-115">**False** 語音參數已停用。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-115">**False** Voice parameters are disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4c3c-116">備註</span><span class="sxs-lookup"><span data-stu-id="d4c3c-116">Remarks</span></span>

<span data-ttu-id="d4c3c-117">Microsoft 代理程式會自動新增語音參數 (文法) 來開啟和關閉 [語音命令] 視窗，以及顯示和隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-117">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="d4c3c-118">如果您將 **GlobalVoiceCommandsEnabled** 設定為 **False**，Agent 會停用這些命令的任何語音參數，以及其他用戶端 [**命令**](/windows/desktop/lwef/the-commands-collection-object)物件的 [**標題**](caption-property.md)的語音參數。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-118">If you set **GlobalVoiceCommandsEnabled** to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Commands**](/windows/desktop/lwef/the-commands-collection-object) objects.</span></span> <span data-ttu-id="d4c3c-119">這可讓您從用戶端目前的活動文法中排除這些。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-119">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="d4c3c-120">不過，因為這可能會封鎖其他用戶端的語音存取，所以在處理使用者的語音輸入之後，請將此屬性重設為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-120">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="d4c3c-121">停用此屬性並不會影響該字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-121">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="d4c3c-122">伺服器所加入的全域命令仍會出現。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-122">The global commands added by the server will still appear.</span></span> <span data-ttu-id="d4c3c-123">您無法從快顯功能表中移除它們。</span><span class="sxs-lookup"><span data-stu-id="d4c3c-123">You cannot remove them from the pop-up menu.</span></span>

 

