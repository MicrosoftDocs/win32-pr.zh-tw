---
description: Windows 通訊端2提供一組擴充的作業，可在建立通訊端連線時一致。 下列說明執行這些功能的服務提供者需求。
ms.assetid: fbc7055e-ea25-4d17-8039-f0fef300353c
title: 連線時間的增強功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33c6d7ee928fe7e97f535363e9e842285eef7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113084"
---
# <a name="enhanced-functionality-at-connect-time"></a><span data-ttu-id="98497-104">連線時間的增強功能</span><span class="sxs-lookup"><span data-stu-id="98497-104">Enhanced Functionality at Connect Time</span></span>

<span data-ttu-id="98497-105">Windows 通訊端2提供一組擴充的作業，可在建立通訊端連線時一致。</span><span class="sxs-lookup"><span data-stu-id="98497-105">Windows Sockets 2 offers an expanded set of operations that can occur coincident to establishing a socket connection.</span></span> <span data-ttu-id="98497-106">下列說明執行這些功能的服務提供者需求。</span><span class="sxs-lookup"><span data-stu-id="98497-106">The service provider requirements for implementing these features are described below.</span></span>

## <a name="conditional-acceptance"></a><span data-ttu-id="98497-107">條件式接受</span><span class="sxs-lookup"><span data-stu-id="98497-107">Conditional Acceptance</span></span>

<span data-ttu-id="98497-108">如先前所述， [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) 會叫用用戶端提供的條件函式，該函式會使用輸入參數來提供擱置連接要求的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98497-108">As described previously, [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) invokes a client-supplied condition function that uses input parameters to supply information about the pending connection request.</span></span> <span data-ttu-id="98497-109">用戶端可以使用此資訊，根據呼叫端資訊（例如呼叫端識別碼、QoS 等）來接受或拒絕連接要求。如果條件函式傳回 CF \_ ACCEPT，則會使用與接聽通訊端相同的屬性來建立新的通訊端，並傳回新通訊端的控制碼。</span><span class="sxs-lookup"><span data-stu-id="98497-109">This information can be used by the client to accept or reject a connection request based on caller information such as caller identifier, QoS, etc. If the condition function returns CF\_ACCEPT, a new socket is created with the same properties as the listening socket, and a handle to the new socket is returned.</span></span> <span data-ttu-id="98497-110">如果條件函數傳回 CF \_ 拒絕，則應該拒絕連線要求。</span><span class="sxs-lookup"><span data-stu-id="98497-110">If the condition function returns CF\_REJECT, the connection request should be rejected.</span></span> <span data-ttu-id="98497-111">如果條件函式傳回 CF \_ 延遲，即無法立即進行接受/拒絕決策，且服務提供者必須在待處理專案佇列中保留連接要求。</span><span class="sxs-lookup"><span data-stu-id="98497-111">If the condition function returns CF\_DEFER, the accept/reject decision cannot be made immediately, and the service provider must leave the connection request on the backlog queue.</span></span> <span data-ttu-id="98497-112">用戶端必須重新呼叫 **WSPAccept** （當它準備好進行決策時），並排列條件函式以傳回 cf \_ ACCEPT 或 cf \_ 拒絕。</span><span class="sxs-lookup"><span data-stu-id="98497-112">The client must call **WSPAccept** again, when it is ready to make a decision, and arrange for the condition function to return either CF\_ACCEPT or CF\_REJECT.</span></span> <span data-ttu-id="98497-113">當延遲的連接要求位於待處理專案佇列的最上方時，服務提供者不會針對擱置的連接要求發出任何進一步的指示。</span><span class="sxs-lookup"><span data-stu-id="98497-113">While a deferred connection request is at the top of the backlog queue, the service provider does not issue any further indications for pending connection requests.</span></span>

## <a name="exchanging-user-data-at-connect-time"></a><span data-ttu-id="98497-114">在連線時間交換使用者資料</span><span class="sxs-lookup"><span data-stu-id="98497-114">Exchanging User Data at Connect Time</span></span>

<span data-ttu-id="98497-115">某些通訊協定允許在連接時交換少量的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="98497-115">Some protocols allow a small amount of user data to be exchanged at connect time.</span></span> <span data-ttu-id="98497-116">如果已從連線的主機接收這類資料，則會將它放在服務提供者緩衝區中，而這個緩衝區的指標和長度值會透過輸入參數提供給 Winsock SPI 用戶端，以供 [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) 條件函數使用。</span><span class="sxs-lookup"><span data-stu-id="98497-116">If such data has been received from the connecting host, it is placed in a service provider buffer, and a pointer to this buffer along with a length value are supplied to the Winsock SPI client through input parameters to the [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) condition function.</span></span> <span data-ttu-id="98497-117">如果 Winsock SPI 用戶端具有回應資料以傳回連線的主機，它可能會將它複製到服務提供者所提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="98497-117">If the Winsock SPI client has response data to return to the connecting host, it may copy this into a buffer that is supplied by the service provider.</span></span> <span data-ttu-id="98497-118">此緩衝區的指標和表示緩衝區大小的整數，也會以條件函數輸入參數的形式提供， (如果通訊協定) 支援的話。</span><span class="sxs-lookup"><span data-stu-id="98497-118">A pointer to this buffer and an integer indicating buffer size are also supplied as condition function input parameters (if supported by the protocol).</span></span>

## <a name="establishing-socket-groups"></a><span data-ttu-id="98497-119">建立通訊端群組</span><span class="sxs-lookup"><span data-stu-id="98497-119">Establishing Socket Groups</span></span>

<span data-ttu-id="98497-120">通訊端群組的所有使用都是保留的。</span><span class="sxs-lookup"><span data-stu-id="98497-120">All use of socket groups is reserved.</span></span>

 

 



