---
title: 不使用額外的伺服器資料來執行和啟用處理常式
description: 不使用額外的伺服器資料來執行和啟用處理常式
ms.assetid: 9d91260a-4cec-4a10-bb57-d02999efae47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6866b40e1257a865aa5068ffd46611c411498877
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "103945539"
---
# <a name="implementing-and-activating-a-handler-with-no-extra-server-data"></a><span data-ttu-id="9d66c-103">不使用額外的伺服器資料來執行和啟用處理常式</span><span class="sxs-lookup"><span data-stu-id="9d66c-103">Implementing and Activating a Handler with No Extra Server Data</span></span>

<span data-ttu-id="9d66c-104">若要建立處理常式的實例（如果它是未取得額外伺服器資料的實例），伺服器必須執行 [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) ，但不是 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)。</span><span class="sxs-lookup"><span data-stu-id="9d66c-104">To create an instance of your handler, if it is one that gets no extra server data, the server must implement [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) but not [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="9d66c-105">**IStdMarshalInfo** 有一個方法 [**GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler)，它會抓取要用於目的地進程的物件處理常式 CLSID。</span><span class="sxs-lookup"><span data-stu-id="9d66c-105">**IStdMarshalInfo** has one method, [**GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler), which retrieves the CLSID of the object handler to be used in the destination process.</span></span> <span data-ttu-id="9d66c-106">當 COM 呼叫 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) 並在用戶端上啟動處理常式時，會呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="9d66c-106">COM calls this when it calls [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) for you and activates the handler on the client side.</span></span>

<span data-ttu-id="9d66c-107">接下來，伺服器和處理常式的執行都必須呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) 函數。</span><span class="sxs-lookup"><span data-stu-id="9d66c-107">Next, both the server and handler implementations must call the [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) function.</span></span> <span data-ttu-id="9d66c-108">此函式會在每一端建立標準封送處理器， (在用戶端上呼叫 proxy 管理員和伺服器端上的存根管理員) 。</span><span class="sxs-lookup"><span data-stu-id="9d66c-108">This function creates a standard marshaler on each side (called a proxy manager on the client side and a stub manager on the server side).</span></span>

<span data-ttu-id="9d66c-109">伺服器會呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)，並在旗標 SMEXF \_ 伺服器中傳遞。</span><span class="sxs-lookup"><span data-stu-id="9d66c-109">The server calls [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passing in the flag SMEXF\_SERVER.</span></span> <span data-ttu-id="9d66c-110">這會建立伺服器端標準封送處理器 (存根管理員) 。</span><span class="sxs-lookup"><span data-stu-id="9d66c-110">This creates a server-side standard marshaler (stub manager).</span></span> <span data-ttu-id="9d66c-111">下圖顯示伺服器端結構：</span><span class="sxs-lookup"><span data-stu-id="9d66c-111">The server-side structure is shown in the following illustration:</span></span>

![顯示伺服器端結構的圖表。](images/b47b3bc0-3e7d-4be4-9767-7ae436bd1b21.png)

## <a name="server-side-structure"></a><span data-ttu-id="9d66c-113">Server-Side 結構</span><span class="sxs-lookup"><span data-stu-id="9d66c-113">Server-Side Structure</span></span>

<span data-ttu-id="9d66c-114">處理常式會呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)，並傳入旗標 SMEXF \_ 處理常式。</span><span class="sxs-lookup"><span data-stu-id="9d66c-114">The handler calls [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passing in the flag SMEXF\_HANDLER.</span></span> <span data-ttu-id="9d66c-115">這會建立用戶端標準封送處理器 (proxy 管理員) ，並使用用戶端上的處理常式進行匯總。</span><span class="sxs-lookup"><span data-stu-id="9d66c-115">This creates a client-side standard marshaler (proxy manager) and aggregates it with the handler on the client side.</span></span> <span data-ttu-id="9d66c-116">兩者的存留期都是由控制身分識別物件所管理， (在處理常式呼叫 **CoGetStdMarshalEx** 時，執行系統所執行的 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)) 。</span><span class="sxs-lookup"><span data-stu-id="9d66c-116">The lifetime of both are managed by the controlling identity object (implementing [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)) that the system implements when the handler calls **CoGetStdMarshalEx**.</span></span> <span data-ttu-id="9d66c-117">下圖顯示用戶端結構。</span><span class="sxs-lookup"><span data-stu-id="9d66c-117">The client-side structure is shown in the following illustration.</span></span>

![顯示用戶端結構的圖表。](images/24ae70ef-dfa8-4784-90ac-dc6cfb043ee5.png)

## <a name="client-side-structure"></a><span data-ttu-id="9d66c-119">Client-Side 結構</span><span class="sxs-lookup"><span data-stu-id="9d66c-119">Client-Side Structure</span></span>

<span data-ttu-id="9d66c-120">如上圖所示，此處理程式實際上是在 proxy 管理員和身分識別/控制未知之間 sandwiched。</span><span class="sxs-lookup"><span data-stu-id="9d66c-120">As shown in the preceding illustration, the handler is actually sandwiched between the proxy manager and the identity/controlling unknown.</span></span> <span data-ttu-id="9d66c-121">這可讓系統控制物件的存留期，同時讓處理常式控制公開的介面。</span><span class="sxs-lookup"><span data-stu-id="9d66c-121">This gives the system control over the lifetime of the object while giving the handler control over the exposed interfaces.</span></span> <span data-ttu-id="9d66c-122">身分識別和 Proxy 管理員之間的虛線表示這兩個共用會透過內部私用介面緊密整合。</span><span class="sxs-lookup"><span data-stu-id="9d66c-122">The dashed line between the Identity and Proxy Manager indicates that the two share tight integration through internal private interfaces.</span></span>

<span data-ttu-id="9d66c-123">當 COM 呼叫用戶端的 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) 時，它會建立處理常式實例，並使用身分識別進行匯總。</span><span class="sxs-lookup"><span data-stu-id="9d66c-123">When COM calls [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) for the client, it creates the handler instance, aggregating it with the Identity.</span></span> <span data-ttu-id="9d66c-124">此處理程式將會透過呼叫 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)來建立標準封送處理器 (，並在) 建立時傳入控制未知的 it 接收。</span><span class="sxs-lookup"><span data-stu-id="9d66c-124">The handler will create the standard marshaler (through the call to [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), passing in the controlling unknown it received when it was created).</span></span> <span data-ttu-id="9d66c-125">處理常式不會執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ，而只會從標準封送處理器傳回 **IMarshal** 。</span><span class="sxs-lookup"><span data-stu-id="9d66c-125">The handler does not implement [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) but just returns **IMarshal** from the standard marshaler.</span></span> <span data-ttu-id="9d66c-126">即使處理常式確實執行 **IMarshal**，在 unmarshal 期間也不會呼叫它。</span><span class="sxs-lookup"><span data-stu-id="9d66c-126">Even if the handler does implement **IMarshal**, it will not get called during an unmarshal.</span></span>

<span data-ttu-id="9d66c-127">如果兩個執行緒在第一次同時 unmarshal 相同的物件，則可能會暫時建立兩個處理常式。</span><span class="sxs-lookup"><span data-stu-id="9d66c-127">If two threads simultaneously unmarshal the same object for the first time, it is possible for two handlers to get created temporarily.</span></span> <span data-ttu-id="9d66c-128">接著會發行一個。</span><span class="sxs-lookup"><span data-stu-id="9d66c-128">One will subsequently be released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d66c-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d66c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d66c-130">輕量 Client-Side 處理常式</span><span class="sxs-lookup"><span data-stu-id="9d66c-130">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 