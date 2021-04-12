---
title: IdleOn 屬性
description: IdleOn 屬性
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104299976"
---
# <a name="idleon-property"></a><span data-ttu-id="4bb03-103">IdleOn 屬性</span><span class="sxs-lookup"><span data-stu-id="4bb03-103">IdleOn Property</span></span>

<span data-ttu-id="4bb03-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="4bb03-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4bb03-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="4bb03-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4bb03-106">傳回或設定布林值，這個值會判斷伺服器是否管理指定字元的 **閒置** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="4bb03-106">Returns or sets a Boolean value that determines whether the server manages the specified character's **Idling** state animations.</span></span>

</dd> <dt>

<span data-ttu-id="4bb03-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="4bb03-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4bb03-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。IdleOn* \*  \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="4bb03-108">*agent ***.Characters ("*** CharacterID\*\*\*").IdleOn*\* \[ = *boolean*\]</span></span>

</dd> </dl> 

| <span data-ttu-id="4bb03-109">部分</span><span class="sxs-lookup"><span data-stu-id="4bb03-109">Part</span></span>      | <span data-ttu-id="4bb03-110">描述</span><span class="sxs-lookup"><span data-stu-id="4bb03-110">Description</span></span>                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb03-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="4bb03-111">*boolean*</span></span> | <span data-ttu-id="4bb03-112">布林運算式，指定伺服器是否管理閒置模式。</span><span class="sxs-lookup"><span data-stu-id="4bb03-112">A Boolean expression specifying whether the server manages idle mode.</span></span> <span data-ttu-id="4bb03-113">**True** (預設為啟用閒置狀態的) 伺服器處理。</span><span class="sxs-lookup"><span data-stu-id="4bb03-113">**True** (Default) Server handling of the idle state is enabled.</span></span> <br/> <span data-ttu-id="4bb03-114">**False** 閒置狀態的伺服器處理已停用。</span><span class="sxs-lookup"><span data-stu-id="4bb03-114">**False** Server handling of the idle state is disabled.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4bb03-115">備註</span><span class="sxs-lookup"><span data-stu-id="4bb03-115">Remarks</span></span>

<span data-ttu-id="4bb03-116">伺服器會在最後一次播放字元的動畫之後自動設定超時時間。</span><span class="sxs-lookup"><span data-stu-id="4bb03-116">The server automatically sets a time-out after the last animation played for a character.</span></span> <span data-ttu-id="4bb03-117">當此計時器的間隔完成時，伺服器會開始一個字元的 **閒置** 狀態，並定期播放其相關聯的 **閒置** 動畫。</span><span class="sxs-lookup"><span data-stu-id="4bb03-117">When this timer's interval is complete, the server begins the **Idling** state for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="4bb03-118">如果您想要停用伺服器，使其無法自動播放 **閒置** 狀態動畫，請將屬性設定為 **False** ，然後播放動畫或呼叫 [**Stop**](stop-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4bb03-118">If you want to disable the server from automatically playing the **Idling** state animations, set the property to **False** and play an animation or call the [**Stop**](stop-method.md) method.</span></span> <span data-ttu-id="4bb03-119">設定這個值並不會影響目前字元的動畫狀態。</span><span class="sxs-lookup"><span data-stu-id="4bb03-119">Setting this value does not affect the current animation state of the character.</span></span>

<span data-ttu-id="4bb03-120">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="4bb03-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 





