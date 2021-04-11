---
description: 卸載或中斷會話的連線會終止通訊。 如果服務提供者支援，則應用程式可以選擇在中斷連接時傳送使用者的資訊。
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: 卸除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943312"
---
# <a name="drop"></a><span data-ttu-id="0e5fb-104">卸除</span><span class="sxs-lookup"><span data-stu-id="0e5fb-104">Drop</span></span>

<span data-ttu-id="0e5fb-105">卸載或中斷會話的連線會終止通訊。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-105">Dropping or disconnecting a session terminates communication.</span></span> <span data-ttu-id="0e5fb-106">如果服務提供者支援，則應用程式可以選擇在中斷連接時傳送使用者的資訊。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-106">The application has the option of sending user-user information at the time of the disconnect, if the service provider supports it.</span></span>

<span data-ttu-id="0e5fb-107">卸載會話的常見原因是使用者已要求中斷連線，或已捨棄會話的另一端。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-107">The usual reasons for dropping a session is a user has requested a disconnect or the other end of the session has dropped.</span></span> <span data-ttu-id="0e5fb-108">當 TAPI 提供應用程式的會話時，也可以呼叫 drop 作業。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-108">A drop operation may also be called when TAPI offers a session to the application.</span></span> <span data-ttu-id="0e5fb-109">如果服務提供者支援這種情況，就會影響應用程式拒絕呼叫。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-109">If the service provider supports this, the effect is that the application rejects the call.</span></span>

<span data-ttu-id="0e5fb-110">叫用卸載作業時，相關的會話有時也會受到影響。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-110">When invoking a drop operation, related sessions can sometimes be affected as well.</span></span> <span data-ttu-id="0e5fb-111">例如，卸載會議電話可以捨棄所有個別的參與者。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-111">For example, dropping a conference call can drop all individual participants.</span></span> <span data-ttu-id="0e5fb-112">狀態變更訊息會傳送至應用程式，以取得其狀態會受到影響的所有呼叫。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-112">State change messages are sent to the application for all calls whose state is affected.</span></span>

<span data-ttu-id="0e5fb-113">當有多個合作物件在呼叫時，會在不同的橋接或合作物件的設定中，捨棄作業可能不會實際清除呼叫。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-113">In various bridged or party-line configurations when multiple parties are on the call, a drop operation may not actually clear the call.</span></span> <span data-ttu-id="0e5fb-114">例如，在橋接的情況下，呼叫可能不會被捨棄，因為來電中其他工作站的狀態可能會受到控制。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-114">For example, in a bridged situation, the call may not be dropped because the status of other stations on the call may govern.</span></span> <span data-ttu-id="0e5fb-115">相反地，呼叫可以直接變更為非使用中狀態，而在其他工作站上保持連線。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-115">Instead, the call may simply be changed to the inactive state while remaining connected at other stations.</span></span>

<span data-ttu-id="0e5fb-116">在卸載作業之後，與會話相關聯的會話識別碼和大部分資源仍可供大部分的查詢作業使用。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-116">Following a drop operation, the session identifier and most resources associated with the session will remain usable for most query operations.</span></span> <span data-ttu-id="0e5fb-117">當應用程式不再需要這些資源時，它必須 [終止會話](terminate-a-session-ovr.md) ，以避免記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-117">When an application no longer requires these resources, it must [terminate the session](terminate-a-session-ovr.md) in order to avoid memory leaks.</span></span>

<span data-ttu-id="0e5fb-118">**TAPI 2.x：** 請參閱 [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop)。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-118">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span></span>

<span data-ttu-id="0e5fb-119">**TAPI 3.x：** 請參閱 [**ITBasicCallControl：:D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)。</span><span class="sxs-lookup"><span data-stu-id="0e5fb-119">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
