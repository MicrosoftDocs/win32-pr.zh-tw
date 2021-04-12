---
title: 如何使用遠端桌面連線代理人用戶端 API
description: 遠端桌面連線代理人用戶端 API 可讓協力廠商通訊協定廠商利用連線代理人，以加速處理使用其通訊協定的連線，以連接到伺服器陣列中的虛擬機器或遠端桌面伺服器。
ms.assetid: 05C2D6CA-C9C5-4783-B196-6A02918046EF
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c931245870cfb72aed54e5aaff24e12d03ddf9e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316186"
---
# <a name="how-to-use-the-remote-desktop-connection-broker-client-api"></a><span data-ttu-id="cf1bf-103">如何使用遠端桌面連線代理人用戶端 API</span><span class="sxs-lookup"><span data-stu-id="cf1bf-103">How to use the Remote Desktop Connection Broker client API</span></span>

<span data-ttu-id="cf1bf-104">遠端桌面連線代理人用戶端 API 可讓協力廠商通訊協定廠商利用連線代理人，以加速處理使用其通訊協定的連線，以連接到伺服器陣列中的虛擬機器或遠端桌面伺服器。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-104">The Remote Desktop Connection Broker client API allows third party protocol vendors to leverage the Connection Broker to expedite the handling of connections that use their protocol to connect to virtual machines or Remote Desktop servers in a farm.</span></span>

## <a name="instructions"></a><span data-ttu-id="cf1bf-105">指示</span><span class="sxs-lookup"><span data-stu-id="cf1bf-105">Instructions</span></span>

### <a name="step-1-obtain-the-iconnectionbrokerclient-interface"></a><span data-ttu-id="cf1bf-106">步驟1：取得 IConnectionBrokerClient 介面</span><span class="sxs-lookup"><span data-stu-id="cf1bf-106">Step 1: Obtain the IConnectionBrokerClient interface</span></span>

<span data-ttu-id="cf1bf-107">當您的應用程式或通訊協定提供者初始化時，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-107">When your application or protocol provider is initialized, perform the following steps.</span></span>

1.  <span data-ttu-id="cf1bf-108">呼叫 [**CBCreateClientInstance**](cbcreateclientinstance.md) 函數，以取得 [**IConnectionBrokerClient**](iconnectionbrokerclient.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-108">Call the [**CBCreateClientInstance**](cbcreateclientinstance.md) function to obtain the [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface.</span></span>
2.  <span data-ttu-id="cf1bf-109">只要您需要，請保留 [**IConnectionBrokerClient**](iconnectionbrokerclient.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-109">Keep the [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface as long as you need it.</span></span>
3.  <span data-ttu-id="cf1bf-110">當不再需要 [**IConnectionBrokerClient**](iconnectionbrokerclient.md) 介面時，請呼叫 [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-110">When the [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface is no longer needed, call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method.</span></span>

### <a name="step-2-request-the-target-information"></a><span data-ttu-id="cf1bf-111">步驟2：要求目標資訊</span><span class="sxs-lookup"><span data-stu-id="cf1bf-111">Step 2: Request the target information</span></span>

<span data-ttu-id="cf1bf-112">當您的通訊協定提供者收到連入連線要求時，請執行下列步驟來呼叫 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-112">When your protocol provider receives an incoming connection request, perform the following steps to call the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span> <span data-ttu-id="cf1bf-113">這個方法會從連接代理程式取得要將連接重新導向至的適當伺服器。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-113">This method obtains, from the Connection Broker, the appropriate server to redirect the connection to.</span></span>

1.  <span data-ttu-id="cf1bf-114">建立可使用 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)或類似函式來發出信號，以用於 *hStatusEvent* 參數的事件。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-114">Create an event that can be signaled using the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), or similar function, to use for the *hStatusEvent* parameter.</span></span>
2.  <span data-ttu-id="cf1bf-115">配置 *pTargetInfo* 和 *pResult* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-115">Allocate memory for the *pTargetInfo* and *pResult* parameters.</span></span> <span data-ttu-id="cf1bf-116">這些記憶體區塊必須保持在原處，直到整個順序完成為止。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-116">These memory blocks must remain in place until after this entire sequence is complete.</span></span>
3.  <span data-ttu-id="cf1bf-117">填寫 [**CB \_ 連接 \_ 資訊**](cb-connection-info.md) 結構，其中包含連入連線的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-117">Fill out a [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure that contains all of the information about the incoming connection.</span></span>
4.  <span data-ttu-id="cf1bf-118">呼叫 [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法，並傳遞所有必要的參數。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-118">Call the [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method, passing all of the required parameters.</span></span> <span data-ttu-id="cf1bf-119">這是會傳回 [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) 介面實例的非同步方法。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-119">This is an asynchronous method that will return an instance of the [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface.</span></span>
5.  <span data-ttu-id="cf1bf-120">等候 *hStatusEvent* 事件變成已設定。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-120">Wait for the *hStatusEvent* event to become set.</span></span>
6.  <span data-ttu-id="cf1bf-121">每當設定 *hStatusEvent* 事件時，請呼叫 [**IConnectionBrokerRequest：： CheckStatus**](iconnectionbrokerrequest-checkstatus.md) 方法來判斷要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-121">Whenever the *hStatusEvent* event is set, call the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method to determine the status of the request.</span></span>
7.  <span data-ttu-id="cf1bf-122">當 [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) 傳回 **CB \_ 狀態 \_ 要求 \_ 已完成** 時， *pTargetInfo* 和 *pResult* 參數會包含其資訊。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-122">When [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) returns **CB\_STATUS\_REQUEST\_COMPLETED**, the *pTargetInfo* and *pResult* parameters will contain their information.</span></span> <span data-ttu-id="cf1bf-123">您可以中斷等候迴圈，因為 *hStatusEvent* 參數將不再使用。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-123">You can break out of the wait loop because the *hStatusEvent* parameter will no longer be used.</span></span>
8.  <span data-ttu-id="cf1bf-124">使用 *pTargetInfo* 參數所代表的 [**CB \_ 目標 \_ 資訊**](cb-target-info.md)結構中的資訊，來決定要將傳入連接重新導向至何處。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-124">Use the information in the [**CB\_TARGET\_INFO**](cb-target-info.md) structure represented by the *pTargetInfo* parameter to determine where to redirect the incoming connection to.</span></span>
9.  <span data-ttu-id="cf1bf-125">釋放 [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-125">Release the [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface.</span></span>
10. <span data-ttu-id="cf1bf-126">關閉 *hStatusEvent* 事件控制碼，或將它重複用於後續的連接要求。</span><span class="sxs-lookup"><span data-stu-id="cf1bf-126">Close the *hStatusEvent* event handle, or you can reuse it for subsequent connection requests.</span></span>

 

 