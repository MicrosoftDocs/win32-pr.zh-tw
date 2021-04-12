---
title: 音調屬性
description: 音調屬性
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372643"
---
# <a name="pitch-property"></a><span data-ttu-id="a50e0-103">音調屬性</span><span class="sxs-lookup"><span data-stu-id="a50e0-103">Pitch Property</span></span>

<span data-ttu-id="a50e0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="a50e0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a50e0-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="a50e0-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Description**</span></span> 
</dt> <dd>

<span data-ttu-id="a50e0-106">傳回指定字元的語音輸出 (TTS) 音調設定的長整數。</span><span class="sxs-lookup"><span data-stu-id="a50e0-106">Returns a Long integer for the specified character's speech output (TTS) pitch setting.</span></span>

</dd> <dt>

<span data-ttu-id="a50e0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="a50e0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a50e0-108">*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。瀝青**</span><span class="sxs-lookup"><span data-stu-id="a50e0-108">*agent ***.Characters ("*** CharacterID\*\*\*").Pitch*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a50e0-109">備註</span><span class="sxs-lookup"><span data-stu-id="a50e0-109">Remarks</span></span>

<span data-ttu-id="a50e0-110">這個屬性只適用于為 TTS 輸出設定的字元。</span><span class="sxs-lookup"><span data-stu-id="a50e0-110">This property applies only to characters configured for TTS output.</span></span> <span data-ttu-id="a50e0-111">如果字元不支援 TTS 輸出，則這個屬性會傳回零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="a50e0-111">If the character does not support TTS output, this property returns zero (0).</span></span>

<span data-ttu-id="a50e0-112">雖然您的應用程式無法寫入此值，但您可以在輸出文字中包含 **Pit** (音調) 標記，以暫時增加特定語句的間距。</span><span class="sxs-lookup"><span data-stu-id="a50e0-112">Although your application cannot write this value, you can include **Pit** (pitch) tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="a50e0-113">不過，使用 **Pit** 標籤來變更間距，並不會變更 [ **音調** ] 屬性設定。</span><span class="sxs-lookup"><span data-stu-id="a50e0-113">However, using the **Pit** tag to change the pitch will not change the **Pitch** property setting.</span></span> <span data-ttu-id="a50e0-114">如需詳細資訊，請參閱 [語音輸出標記](pit-tag.md)。</span><span class="sxs-lookup"><span data-stu-id="a50e0-114">For further information, see [Speech Output Tags](pit-tag.md).</span></span>

 

 




