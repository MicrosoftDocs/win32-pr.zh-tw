---
description: 協同作業 API 列舉
ms.assetid: f72e372a-0d23-47f4-8518-1296ec81ce55
title: 協同作業 API 列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3504e36d96a920452aef1a8dfeb0724aea127c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944289"
---
# <a name="collaboration-api-enumerations"></a><span data-ttu-id="65e7b-103">協同作業 API 列舉</span><span class="sxs-lookup"><span data-stu-id="65e7b-103">Collaboration API Enumerations</span></span>

<span data-ttu-id="65e7b-104">下列列舉支援對等共同作業基礎結構函數。</span><span class="sxs-lookup"><span data-stu-id="65e7b-104">The following enumerations support the Peer Collaboration Infrastructure functions.</span></span>



| <span data-ttu-id="65e7b-105">列舉型別</span><span class="sxs-lookup"><span data-stu-id="65e7b-105">Enumeration</span></span>                                                                         | <span data-ttu-id="65e7b-106">描述</span><span class="sxs-lookup"><span data-stu-id="65e7b-106">Description</span></span>                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65e7b-107">**對等 \_ 應用程式 \_ 註冊 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="65e7b-107">**PEER\_APPLICATION\_REGISTRATION\_TYPE**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_application_registration_type) | <span data-ttu-id="65e7b-108">定義一組對等應用程式註冊旗標。</span><span class="sxs-lookup"><span data-stu-id="65e7b-108">Defines the set of peer application registration flags.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="65e7b-109">**對等 \_ 變更 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="65e7b-109">**PEER\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_change_type)                                      | <span data-ttu-id="65e7b-110">定義可以在對等物件、端點或應用程式上執行的一組變更。</span><span class="sxs-lookup"><span data-stu-id="65e7b-110">Defines the set of changes that can be performed on a peer object, endpoint, or application.</span></span>                                                                                                                                                                                  |
| [<span data-ttu-id="65e7b-111">**對等登入 \_ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="65e7b-111">**PEER\_SIGNIN\_FLAGS**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_signin_flags)                                    | <span data-ttu-id="65e7b-112">定義當對等登入對等共同作業網路時，可用的對等存在性發行集行為。</span><span class="sxs-lookup"><span data-stu-id="65e7b-112">Defines the set of peer presence publication behaviors available when the peer signs in to a peer collaboration network.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="65e7b-113">**對等 \_ 監看 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="65e7b-113">**PEER\_WATCH\_PERMISSION**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_watch_permission)                            | <span data-ttu-id="65e7b-114">定義一組許可權，這些許可權代表連絡人對監看對等的存在性。</span><span class="sxs-lookup"><span data-stu-id="65e7b-114">Defines the set of permissions that represent a contact's presence to a watching peer.</span></span>                                                                                                                                                                                        |
| [<span data-ttu-id="65e7b-115">**對等 \_ COLLABORATION \_ 事件 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="65e7b-115">**PEER\_COLLAB\_EVENT\_TYPE**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_collab_event_type)                         | <span data-ttu-id="65e7b-116">定義對等共同作業網路事件基礎結構可在對等上引發的事件集。</span><span class="sxs-lookup"><span data-stu-id="65e7b-116">Defines the set of events that can be raised on a peer by the peer collaboration network event infrastructure.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="65e7b-117">**對 \_ 等狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="65e7b-117">**PEER\_PRESENCE\_STATUS**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_presence_status)                              | <span data-ttu-id="65e7b-118">定義可供參與對等共同作業網路之對等的可能存在狀態設定集。</span><span class="sxs-lookup"><span data-stu-id="65e7b-118">Defines the set of possible presence status settings available to a peer that participates in a peer collaboration network.</span></span> <span data-ttu-id="65e7b-119">對等共同作業網路端點可以設定這些設定，以表示對等連絡人目前對其監看員的參與程度。</span><span class="sxs-lookup"><span data-stu-id="65e7b-119">These settings can be set by a peer collaboration network endpoint to indicate the peer contact's current level of participation to its watchers.</span></span> |
| [<span data-ttu-id="65e7b-120">**對等 \_ 邀請 \_ 回應 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="65e7b-120">**PEER\_INVITATION\_RESPONSE\_TYPE**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_invitation_response_type)           | <span data-ttu-id="65e7b-121">定義收到邀請以加入對等共同作業活動的回應集合。</span><span class="sxs-lookup"><span data-stu-id="65e7b-121">Defines the set of responses received to an invitation to join a Peer Collaboration activity.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="65e7b-122">**對等 \_ 發行 \_ 領域**</span><span class="sxs-lookup"><span data-stu-id="65e7b-122">**PEER\_PUBLICATION\_SCOPE**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_publication_scope)                          | <span data-ttu-id="65e7b-123">定義發行對等物件或資料的範圍集合。</span><span class="sxs-lookup"><span data-stu-id="65e7b-123">Defines the set of scopes for the publication of peer objects or data.</span></span>                                                                                                                                                                                                        |



 

 

 



