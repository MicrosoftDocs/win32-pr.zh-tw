---
description: 對等基礎結構會使用下列通用結構。
ms.assetid: b8f290fb-ae0b-44de-87cc-d25f7e0e3ae6
title: 通用結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fb4afd791d42565202ef55779d1b4ee9260efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971803"
---
# <a name="common-structures"></a><span data-ttu-id="c11f1-103">通用結構</span><span class="sxs-lookup"><span data-stu-id="c11f1-103">Common Structures</span></span>

<span data-ttu-id="c11f1-104">對等基礎結構會使用下列通用結構。</span><span class="sxs-lookup"><span data-stu-id="c11f1-104">The Peer Infrastructure uses the following common structures.</span></span>



| <span data-ttu-id="c11f1-105">結構</span><span class="sxs-lookup"><span data-stu-id="c11f1-105">Structure</span></span>                                                                          | <span data-ttu-id="c11f1-106">Description</span><span class="sxs-lookup"><span data-stu-id="c11f1-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c11f1-107">**對等 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="c11f1-107">**PEER\_ADDRESS**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_address)                                              | <span data-ttu-id="c11f1-108">指定 IP 位址的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c11f1-108">Specifies the information about the IP address.</span></span>                                                                                     |
| [<span data-ttu-id="c11f1-109">**對等 \_ 連接 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="c11f1-109">**PEER\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_connection_info)                             | <span data-ttu-id="c11f1-110">包含連接的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c11f1-110">Contains information about a connection.</span></span> <span data-ttu-id="c11f1-111">當您列舉對等繪圖或群組連接時，會傳回這個結構。</span><span class="sxs-lookup"><span data-stu-id="c11f1-111">This structure is returned when you are enumerating peer graphing or grouping connections.</span></span> |
| [<span data-ttu-id="c11f1-112">**對等 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c11f1-112">**PEER\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_data)                                                    | <span data-ttu-id="c11f1-113">包含二進位資料。</span><span class="sxs-lookup"><span data-stu-id="c11f1-113">Contains binary data.</span></span>                                                                                                               |
| [<span data-ttu-id="c11f1-114">**對等 \_ 事件 \_ 連接 \_ 變更 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c11f1-114">**PEER\_EVENT\_CONNECTION\_CHANGE\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_connection_change_data) | <span data-ttu-id="c11f1-115">包含更新的資訊，其中包括鄰近或直接連線的變更。</span><span class="sxs-lookup"><span data-stu-id="c11f1-115">Contains updated information that includes changes to a neighbor or direct connection.</span></span>                                              |
| [<span data-ttu-id="c11f1-116">**對等 \_ 事件 \_ 傳入 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c11f1-116">**PEER\_EVENT\_INCOMING\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data)                    | <span data-ttu-id="c11f1-117">包含更新的資訊，其中包含節點從鄰近或直接連接接收的資料變更。</span><span class="sxs-lookup"><span data-stu-id="c11f1-117">Contains updated information that includes data changes a node receives from a neighbor or direct connection.</span></span>                       |
| [<span data-ttu-id="c11f1-118">**對等 \_ 事件 \_ 記錄 \_ 變更 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c11f1-118">**PEER\_EVENT\_RECORD\_CHANGE\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data)         | <span data-ttu-id="c11f1-119">包含應用程式要求對記錄或記錄類型進行資料變更的更新資訊。</span><span class="sxs-lookup"><span data-stu-id="c11f1-119">Contains updated information that an application requests for data changes to a record or record type.</span></span>                              |
| [<span data-ttu-id="c11f1-120">**對等 \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="c11f1-120">**PEER\_RECORD**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_record)                                                | <span data-ttu-id="c11f1-121">包含應用程式使用的記錄物件。</span><span class="sxs-lookup"><span data-stu-id="c11f1-121">Contains the record object that an application uses.</span></span>                                                                                |
| [<span data-ttu-id="c11f1-122">**對等 \_ 版本 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="c11f1-122">**PEER\_VERSION\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_version_data)                                   | <span data-ttu-id="c11f1-123">包含對等圖形和群組 Api 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="c11f1-123">Contains the version information about the Peer Graphing and Grouping APIs.</span></span>                                                         |



 

 

 



