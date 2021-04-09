---
title: Agent 控制項屬性
description: Agent 控制項屬性
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021007"
---
# <a name="agent-control-properties"></a><span data-ttu-id="e0bf9-103">Agent 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="e0bf9-103">Agent Control Properties</span></span>

<span data-ttu-id="e0bf9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e0bf9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e0bf9-105">下列屬性可直接從 Agent 控制項存取：</span><span class="sxs-lookup"><span data-stu-id="e0bf9-105">The following properties are directly accessed from the Agent control:</span></span>

-   [<span data-ttu-id="e0bf9-106">**連線**</span><span class="sxs-lookup"><span data-stu-id="e0bf9-106">**Connected**</span></span>](connected-property.md)
-   [<span data-ttu-id="e0bf9-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="e0bf9-107">**Name**</span></span>](name-property-a.md)
-   [<span data-ttu-id="e0bf9-108">**RaiseRequestErrors**</span><span class="sxs-lookup"><span data-stu-id="e0bf9-108">**RaiseRequestErrors**</span></span>](raiserequesterrors-property.md)

<span data-ttu-id="e0bf9-109">此外，某些程式設計環境可能會指派其他設計階段或執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="e0bf9-109">In addition, some programming environments may assign additional design-time or run-time properties.</span></span> <span data-ttu-id="e0bf9-110">例如，Visual Basic 會新增 Left、Index、Tag 和 Top 屬性，在表單上定義控制項的位置，即使控制項不會出現在執行時間的表單頁面上也一樣。</span><span class="sxs-lookup"><span data-stu-id="e0bf9-110">For example, Visual Basic adds Left, Index, Tag, and Top properties that define the location of the control on a form even though the control does not appear on the form's page at run time.</span></span>

<span data-ttu-id="e0bf9-111">暫止的屬性仍支援回溯相容性，但一律會傳回 **False** ，因為伺服器已不再支援暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="e0bf9-111">The Suspended property is still supported for backward compatibility, but always returns **False** because the server no longer supports a suspended state.</span></span>

 

 




