---
description: ATM 落在根資料和根控制項平面的類別中。
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: ATM 指向 Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973064"
---
# <a name="atm-point-to-multipoint"></a><span data-ttu-id="61286-103">ATM 指向 Multipoint</span><span class="sxs-lookup"><span data-stu-id="61286-103">ATM Point to Multipoint</span></span>

<span data-ttu-id="61286-104">ATM 落在根資料和根控制項平面的類別中。</span><span class="sxs-lookup"><span data-stu-id="61286-104">ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="61286-105">作為根的應用程式會建立 c \_ 根通訊端，而分葉節點上執行的對應項會使用 c 分 \_ 葉通訊端。</span><span class="sxs-lookup"><span data-stu-id="61286-105">An application acting as the root would create c\_root sockets and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="61286-106">根應用程式會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 來加入新的分葉節點。</span><span class="sxs-lookup"><span data-stu-id="61286-106">The root application uses [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="61286-107">分葉節點上的對應應用程式，會將它們的 c \_ 分葉通訊端設定為接聽模式。</span><span class="sxs-lookup"><span data-stu-id="61286-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into listen mode.</span></span> <span data-ttu-id="61286-108">具有指定之 c \_ 根通訊端的 WSAJoinLeaf 會對應至 2931 ADDPARTY 訊息。</span><span class="sxs-lookup"><span data-stu-id="61286-108">**WSAJoinLeaf** with a c\_root socket specified is mapped to the Q.2931 ADDPARTY message.</span></span> <span data-ttu-id="61286-109">在 ATM 的3.1 中不支援分葉起始的聯結，但在 ATM 單向4.0 中支援。</span><span class="sxs-lookup"><span data-stu-id="61286-109">The leaf-initiated join is not supported in ATM UNI 3.1, but is supported in ATM UNI 4.0.</span></span> <span data-ttu-id="61286-110">因此 ，使用指定的 c 分 \_ 葉通訊端 WSAJoinLeaf 會對應到適當的 ATM 單向4.0 訊息。</span><span class="sxs-lookup"><span data-stu-id="61286-110">Thus **WSAJoinLeaf** with a c\_leaf socket specified is mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="61286-111">針對 ATM 點對 multipoint，還有其他考慮要謹記：</span><span class="sxs-lookup"><span data-stu-id="61286-111">There are additional considerations to bear in mind for ATM point-to-multipoint:</span></span>

-   <span data-ttu-id="61286-112">將新的點新增至 ATM 點對 multipoint 會話只會以邀請為基礎。</span><span class="sxs-lookup"><span data-stu-id="61286-112">The addition of new leaves to the ATM point-to-multipoint session is invitation-based only.</span></span> <span data-ttu-id="61286-113">根邀請會藉由呼叫 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)函式來離開（已有 [**接受**](/windows/desktop/api/Winsock2/nf-winsock2-accept)函式呼叫）。</span><span class="sxs-lookup"><span data-stu-id="61286-113">The root invites leaves — which have already their [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function call — by calling the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="61286-114">在 ATM 點對 multipoint 會話中的資料流程程，只是從根目錄到離開;「離開」無法使用相同的會話將資訊傳送至根目錄。</span><span class="sxs-lookup"><span data-stu-id="61286-114">The flow of data in an ATM point-to-multipoint session is from root-to-leaves only; leaves cannot use the same session to send information to the root.</span></span>
-   <span data-ttu-id="61286-115">每個 ATM 介面卡只允許一個分葉。</span><span class="sxs-lookup"><span data-stu-id="61286-115">Only one leaf per ATM adapter is allowed.</span></span>

 

 



