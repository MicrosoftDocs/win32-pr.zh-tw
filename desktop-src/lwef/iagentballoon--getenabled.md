---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311379"
---
# <a name="iagentballoongetenabled"></a><span data-ttu-id="0648b-103">IAgentBalloon：： GetEnabled</span><span class="sxs-lookup"><span data-stu-id="0648b-103">IAgentBalloon::GetEnabled</span></span>

<span data-ttu-id="0648b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0648b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

<span data-ttu-id="0648b-105">抓取文字氣球的 [**Enabled**](enabled-property.md) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="0648b-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a word balloon.</span></span>

-   <span data-ttu-id="0648b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0648b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0648b-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="0648b-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="0648b-108">在啟用文字批註時接收 **True** 的變數位址，以及停用時的 **False** 。</span><span class="sxs-lookup"><span data-stu-id="0648b-108">The address of a variable that receives **True** when the word balloon is enabled and **False** when it is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="0648b-109">除非已停用，否則 Microsoft 代理程式伺服器會自動顯示語音輸出的文字提示。</span><span class="sxs-lookup"><span data-stu-id="0648b-109">The Microsoft Agent server automatically displays the word balloon for spoken output, unless it is disabled.</span></span> <span data-ttu-id="0648b-110">您可以針對 Microsoft Agent 字元編輯器中的字元停用文字批註，或由使用者)  (Microsoft Agent 屬性工作表中的所有字元。</span><span class="sxs-lookup"><span data-stu-id="0648b-110">The word balloon can be disabled for a character in the Microsoft Agent Character Editor, or (by the user) for all characters in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="0648b-111">如果使用者停用文字提示，用戶端就無法將它還原。</span><span class="sxs-lookup"><span data-stu-id="0648b-111">If the user disables the word balloon, the client cannot restore it.</span></span>

 

 




