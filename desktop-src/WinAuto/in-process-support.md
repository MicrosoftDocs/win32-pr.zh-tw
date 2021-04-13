---
title: In-Process 支援
description: 動態注釋的目前執行完全是同進程，因此只允許擁有這些 UI 元素的進程標注 UI 專案。
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300352"
---
# <a name="in-process-support"></a><span data-ttu-id="f448d-103">In-Process 支援</span><span class="sxs-lookup"><span data-stu-id="f448d-103">In-Process Support</span></span>

<span data-ttu-id="f448d-104">動態注釋的目前執行完全是同進程，因此只允許擁有這些 UI 元素的進程標注 UI 專案。</span><span class="sxs-lookup"><span data-stu-id="f448d-104">The current implementation of Dynamic Annotation is entirely in-process and consequently allows only UI elements to be annotated by the process that owns those UI elements.</span></span> <span data-ttu-id="f448d-105">一個進程不可能對另一個進程的 UI 元素加上批註。</span><span class="sxs-lookup"><span data-stu-id="f448d-105">It is not possible for one process to annotate the UI elements of another process.</span></span>

<span data-ttu-id="f448d-106">請注意，這只會影響設定注釋的動作;它不會干擾用戶端存取屬性 (批註或其他進程中的 UI 元素) 的能力。</span><span class="sxs-lookup"><span data-stu-id="f448d-106">Note that this only affects the act of setting an annotation; it does not interfere with the ability of clients to access the properties (annotated or otherwise) of UI elements in other processes.</span></span>

 

 




