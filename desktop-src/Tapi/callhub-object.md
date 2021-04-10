---
description: CallHub 物件代表多方呼叫的協力廠商觀點。
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: CallHub 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944602"
---
# <a name="callhub-object"></a><span data-ttu-id="6d7cb-103">CallHub 物件</span><span class="sxs-lookup"><span data-stu-id="6d7cb-103">CallHub Object</span></span>

<span data-ttu-id="6d7cb-104">CallHub 物件代表多方呼叫的協力廠商觀點。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-104">The CallHub object represents a third-party view of a multiparty call.</span></span> <span data-ttu-id="6d7cb-105">相關聯的介面和方法會取得並設定中樞的相關資訊，例如其是否為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-105">The associated interfaces and methods get and set information concerning the hub, such as whether it is active.</span></span> <span data-ttu-id="6d7cb-106">使用 CallHub 物件時，具有必要安全性的使用者可以探索並可能控制呼叫中的其他參與者。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-106">Using the CallHub object, a user with the required security can discover and potentially control other participants in a call.</span></span>

<span data-ttu-id="6d7cb-107">應用程式無法直接建立 CallHub 物件。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-107">A CallHub object cannot be created directly by an application.</span></span> <span data-ttu-id="6d7cb-108">透過 TAPI 3 接收來電時，會間接建立 CallHub 物件。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-108">A CallHub object is created indirectly when an incoming call is received through TAPI 3.</span></span>

<span data-ttu-id="6d7cb-109">TAPI 3 依賴 TAPI 服務提供者，以提供使用 CallHub 物件執行之呼叫的必要資訊。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-109">TAPI 3 relies on TAPI service providers to provide the necessary information about calls to implement using the CallHub object.</span></span> <span data-ttu-id="6d7cb-110">因為並非所有服務提供者都提供此資訊，而且並非所有硬體都支援呼叫中樞追蹤，所以連線中其他使用者的可用資訊可能會受到限制或不存在。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-110">Because not all service providers provide this information, and not all hardware supports call hub tracking, the information available about the other users in the connection may be limited or nonexistent.</span></span>

<span data-ttu-id="6d7cb-111">[建立簡單的會議](create-a-simple-conference.md)程式碼範例示範如何使用 CallHub 物件。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-111">The [Create a Simple Conference](create-a-simple-conference.md) code example illustrates use of a CallHub object.</span></span>

<span data-ttu-id="6d7cb-112">如需與 CallHub 物件相關聯之所有介面的清單，請參閱 [CallHub 物件介面](callhub-object-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="6d7cb-112">See [CallHub Object Interfaces](callhub-object-interfaces.md) for a list of all interfaces associated with the CallHub object.</span></span>

 

 



