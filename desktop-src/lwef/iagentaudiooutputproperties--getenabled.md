---
title: IAgentAudioOutputProperties GetEnabled
description: IAgentAudioOutputProperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021406"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a><span data-ttu-id="cea32-103">IAgentAudioOutputProperties：： GetEnabled</span><span class="sxs-lookup"><span data-stu-id="cea32-103">IAgentAudioOutputProperties::GetEnabled</span></span>

<span data-ttu-id="cea32-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="cea32-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

<span data-ttu-id="cea32-105">抓取值，指出是否已啟用字元語音輸出。</span><span class="sxs-lookup"><span data-stu-id="cea32-105">Retrieves a value indicating whether character speech output is enabled.</span></span>

-   <span data-ttu-id="cea32-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="cea32-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cea32-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="cea32-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="cea32-108">如果目前已啟用語音輸出，則為收到 **True** 之變數的位址，如果停用，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="cea32-108">Address of a variable that receives **True** if the speech output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="cea32-109">因為此設定會影響所有字元的 (TTS 和音效檔) 的語音輸出，所以只有使用者可以在 Microsoft Agent 屬性工作表中變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="cea32-109">Because this setting affects spoken output (TTS and sound file) for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




