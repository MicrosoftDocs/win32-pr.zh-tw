---
description: 根據針對 Windows 通訊端2通訊協定獨立的 multipoint/多播配置所定義的分類，ATM 會落在根資料和根控制項平面的類別中。
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Winsock ATM 函數詳細資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114289"
---
# <a name="winsock-atm-function-details"></a><span data-ttu-id="b33ad-103">Winsock ATM 函數詳細資料</span><span class="sxs-lookup"><span data-stu-id="b33ad-103">Winsock ATM Function Details</span></span>

<span data-ttu-id="b33ad-104">根據針對 Windows 通訊端2通訊協定獨立的 multipoint/多播配置所定義的分類，ATM 會落在根資料和根控制項平面的類別中。</span><span class="sxs-lookup"><span data-stu-id="b33ad-104">Based on the taxonomy defined for Windows Sockets 2 protocol-independent multipoint/multicast schemes, ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="b33ad-105"> (如需詳細資訊，請參閱 Windows 通訊端 2 API 規格，附錄 D。 ) 作為根的應用程式會建立 c \_ 根通訊端，而分葉節點上執行的對應項會使用 c 分 \_ 葉通訊端。</span><span class="sxs-lookup"><span data-stu-id="b33ad-105">(See the Windows Sockets 2 API Specification, Appendix D for more information.) An application acting as the root would create c\_root sockets, and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="b33ad-106">根應用程式會使用 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 來加入新的分葉節點。</span><span class="sxs-lookup"><span data-stu-id="b33ad-106">The root application will use [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="b33ad-107">分葉節點上的對應應用程式，會將它們的 c \_ 分葉通訊端設定為接聽模式。</span><span class="sxs-lookup"><span data-stu-id="b33ad-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into the listening mode.</span></span> <span data-ttu-id="b33ad-108">指定了 c \_ 根通訊端的 WSAJoinLeaf，將會對應至第一個分葉) 的安裝訊息 (，或針對任何後續的離開) 新增合作物件訊息 (。</span><span class="sxs-lookup"><span data-stu-id="b33ad-108">**WSAJoinLeaf** with a c\_root socket specified will be mapped to the Q.2931 SETUP message (for the first leaf) or ADD PARTY message (for any subsequent leaves).</span></span>

> [!Note]  
> <span data-ttu-id="b33ad-109">針對任何後續的保留，在 **WSAJoinLeaf** 中指定的 QoS 參數，應該根據 ATM 論壇單向規格加以忽略。</span><span class="sxs-lookup"><span data-stu-id="b33ad-109">The QoS parameters specified in **WSAJoinLeaf** for any subsequent leaves should be ignored per the ATM Forum UNI specification.</span></span>

 

<span data-ttu-id="b33ad-110">分葉起始的聯結不是 ATM 單向3.1 的一部分，但在 ATM 單向4.0 中是支援的。</span><span class="sxs-lookup"><span data-stu-id="b33ad-110">The leaf-initiated join is not part of the ATM UNI 3.1, but is supported in the ATM UNI 4.0.</span></span> <span data-ttu-id="b33ad-111">因此[](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) ，使用指定的 c 分 \_ 葉通訊端 WSAJoinLeaf 可以對應到適當的 ATM 單向4.0 訊息。</span><span class="sxs-lookup"><span data-stu-id="b33ad-111">Thus [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) with a c\_leaf socket specified can be mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="b33ad-112">在 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)中指定的 condition 函式呼叫時，會在 *lpSQOS* 參數中修改對應的 LLI，以支援 AAL 參數和 B 協商。</span><span class="sxs-lookup"><span data-stu-id="b33ad-112">The AAL Parameter and B-LLI negotiation is supported through the modification of the corresponding IEs in the *lpSQOS* parameter upon the invocation of the condition function specified in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span></span>

> [!Note]  
> <span data-ttu-id="b33ad-113">只有這兩個中的特定欄位可以修改。</span><span class="sxs-lookup"><span data-stu-id="b33ad-113">Only certain fields in those two IEs can be modified.</span></span> <span data-ttu-id="b33ad-114">如需詳細資料，請參閱 ATM 論壇單向規格附錄 C 和附錄 F。</span><span class="sxs-lookup"><span data-stu-id="b33ad-114">See the ATM Forum UNI specification Appendix C and Appendix F for details.</span></span>

 

 

 



