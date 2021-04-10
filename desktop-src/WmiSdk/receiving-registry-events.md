---
description: 系統登錄提供者會嘗試針對每個發生的事件傳送一個通知。
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: 接收登錄事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026493"
---
# <a name="receiving-registry-events"></a><span data-ttu-id="55eff-103">接收登錄事件</span><span class="sxs-lookup"><span data-stu-id="55eff-103">Receiving Registry Events</span></span>

<span data-ttu-id="55eff-104">系統登錄提供者會嘗試針對每個發生的事件傳送一個通知。</span><span class="sxs-lookup"><span data-stu-id="55eff-104">The System Registry provider attempts to send one notification for every event that occurs.</span></span> <span data-ttu-id="55eff-105">不過，系統登錄提供者不保證取用者會收到任何或所有事件。</span><span class="sxs-lookup"><span data-stu-id="55eff-105">However, the System Registry provider does not guarantee that the consumer will receive any or all events.</span></span> <span data-ttu-id="55eff-106">例外狀況是系統登錄提供者會確保取用者每個事件註冊都會收到一個通知。</span><span class="sxs-lookup"><span data-stu-id="55eff-106">The exception is that the System Registry provider does ensure that a consumer will receive one notification for each event registration.</span></span>

<span data-ttu-id="55eff-107">例如，假設取用者註冊了兩個樹狀變更事件，要求 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) 實例的通知。</span><span class="sxs-lookup"><span data-stu-id="55eff-107">For example, suppose a consumer registers for two tree change events, requesting notification for [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) instances.</span></span> <span data-ttu-id="55eff-108">每個註冊都有相同的 Hive (子樹) 值，但有不同的 RootPath 值。</span><span class="sxs-lookup"><span data-stu-id="55eff-108">Each registration has the same Hive (subtree) value but a different RootPath value.</span></span> <span data-ttu-id="55eff-109">如果這兩個路徑中的金鑰多次變更，系統登錄提供者會保證取用者會收到每個路徑的通知。</span><span class="sxs-lookup"><span data-stu-id="55eff-109">If keys in both paths change multiple times, the System Registry provider guarantees that the consumer will receive a notification for each path.</span></span> <span data-ttu-id="55eff-110">視登錄和系統登錄提供者的回應時間而定，取用者可能會收到與事件發生次數一樣多的通知。</span><span class="sxs-lookup"><span data-stu-id="55eff-110">Depending on the response time of the registry and the System Registry provider, the consumer may receive as many notifications as there were occurrences of events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55eff-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="55eff-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55eff-112">註冊系統登錄事件</span><span class="sxs-lookup"><span data-stu-id="55eff-112">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> </dl>

 

 
