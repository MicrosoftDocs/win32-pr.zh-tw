---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673292"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a><span data-ttu-id="ebabc-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span><span class="sxs-lookup"><span data-stu-id="ebabc-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span></span>

<span data-ttu-id="ebabc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ebabc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

<span data-ttu-id="ebabc-105">抓取值，指出是否已啟用音效效果輸出。</span><span class="sxs-lookup"><span data-stu-id="ebabc-105">Retrieves a value indicating whether sound effects output is enabled.</span></span>

-   <span data-ttu-id="ebabc-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="ebabc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ebabc-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span><span class="sxs-lookup"><span data-stu-id="ebabc-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span></span>
</dt> <dd>

<span data-ttu-id="ebabc-108">如果目前已啟用音效效果輸出，則為收到 **True** 之變數的位址，如果停用，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="ebabc-108">Address of a variable that receives **True** if the sound effects output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="ebabc-109">在 Microsoft 代理程式字元編輯器中，會指派字元動畫的音效效果。</span><span class="sxs-lookup"><span data-stu-id="ebabc-109">Sound effects for a character's animation are assigned in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="ebabc-110">因為這項設定會影響所有字元的音效效果輸出，所以只有使用者可以在 Microsoft Agent 屬性工作表中變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ebabc-110">Because this setting affects sound effects output for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




