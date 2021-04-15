---
title: 選擇驗證層級
description: 選擇驗證等級時，請使用下列指導方針。
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462161"
---
# <a name="choosing-an-authentication-level"></a><span data-ttu-id="4f4a4-103">選擇驗證層級</span><span class="sxs-lookup"><span data-stu-id="4f4a4-103">Choosing an Authentication Level</span></span>

<span data-ttu-id="4f4a4-104">選擇驗證等級時，請使用下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="4f4a4-104">When choosing an authentication level, use the following guideline.</span></span> <span data-ttu-id="4f4a4-105">如果所傳送的資料是否可以被攔截和修改，且接收的資料可以被攔截或修改，請使用 RPC \_ C \_ 驗證 \_ LEVEL \_ NONE （預設值）。</span><span class="sxs-lookup"><span data-stu-id="4f4a4-105">If it does not matter whether the data being sent can be intercepted and modified, and the data received can be intercepted or modified, use RPC\_C\_AUTHN\_LEVEL\_NONE, which is the default.</span></span> <span data-ttu-id="4f4a4-106">如果不應該修改資料，而且不會傳送或接收私人資料，請使用 RPC \_ C \_ 驗證 \_ 層級 \_ 的 PKT \_ 完整性。</span><span class="sxs-lookup"><span data-stu-id="4f4a4-106">If the data should not be modified, and private data is not being sent or received, use RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY.</span></span> <span data-ttu-id="4f4a4-107">在所有其他情況下，請使用 RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權。</span><span class="sxs-lookup"><span data-stu-id="4f4a4-107">In all other cases, use RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

<span data-ttu-id="4f4a4-108">請勿使用 RPC \_ c \_ 驗證 \_ 層級 \_ 的預設值、rpc \_ c \_ 驗證 \_ 層級 \_ CONNECT、rpc \_ c \_ 驗證 \_ 層級 \_ 呼叫或 rpc \_ c \_ 驗證 \_ 層級 \_ PKT。</span><span class="sxs-lookup"><span data-stu-id="4f4a4-108">Do not use RPC\_C\_AUTHN\_LEVEL\_DEFAULT, RPC\_C\_AUTHN\_LEVEL\_CONNECT, RPC\_C\_AUTHN\_LEVEL\_CALL or RPC\_C\_AUTHN\_LEVEL\_PKT.</span></span> <span data-ttu-id="4f4a4-109">複雜的攻擊者可以中斷這些驗證層級，並使其失效。</span><span class="sxs-lookup"><span data-stu-id="4f4a4-109">A sophisticated attacker can break these authentication levels and render them ineffective.</span></span> <span data-ttu-id="4f4a4-110">其中每個層級都會讓攻擊者稍微難以攔截和修改資料，並進行模擬，但無法真正達成安全性。</span><span class="sxs-lookup"><span data-stu-id="4f4a4-110">Each of these levels does make it slightly more difficult for an attacker to intercept and modify data, and to impersonate, but security is not really achieved.</span></span> <span data-ttu-id="4f4a4-111">由於攻擊者的複雜性層級很罕見，因此並非明智的選擇。</span><span class="sxs-lookup"><span data-stu-id="4f4a4-111">Since the sophistication level of an attacker is rarely known, these are not wise choices.</span></span>

 

 




