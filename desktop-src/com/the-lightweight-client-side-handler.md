---
title: 輕量 Client-Side 處理常式
description: 輕量用戶端處理常式可讓您建立任何大小的一般用戶端處理常式，以協助您進行任何種類的標準工作。
ms.assetid: b712237c-55d7-4f52-9cf6-19c6e5fb3182
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e8df5be24e8773a660a4d0208b27a2f585e32
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683167"
---
# <a name="the-lightweight-client-side-handler"></a><span data-ttu-id="e8ab6-103">輕量 Client-Side 處理常式</span><span class="sxs-lookup"><span data-stu-id="e8ab6-103">The Lightweight Client-Side Handler</span></span>

<span data-ttu-id="e8ab6-104">輕量用戶端處理常式可讓您建立任何大小的一般用戶端處理常式，以協助您進行任何種類的標準工作。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-104">Lightweight client-side handlers allow you to create general client-side handlers of any size, to help you do any kind of standard task.</span></span> <span data-ttu-id="e8ab6-105">做為處理常式，這些都可供多個用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-105">As handlers, these are usable by more than one client.</span></span> <span data-ttu-id="e8ab6-106">它們與 OLE 處理常式不同之處在于，它們無法在啟動伺服器之前建立，而且其存留期會系結至 proxy 管理員的存留期，以防止可能發生競爭情況的情況下，處理常式可能會在其他情況下釋放。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-106">They differ from OLE handlers in that they cannot be created before the server is launched, and their lifetime is tied to that of the proxy manager, preventing a possible race condition in which the handler could otherwise be prematurely released.</span></span>

<span data-ttu-id="e8ab6-107">Proxy 管理員是系統建立的物件，它會執行 [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) 介面。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-107">The proxy manager is the system-created object that implements the [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) interface.</span></span> <span data-ttu-id="e8ab6-108">如果您使用標準封送處理，當您呼叫 [**CoGetStandardMarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (或 [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex)時，系統會為您建立它，以針對輕量處理常式建立匯總的封送處理器) 也會在物件上執行 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 和 [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) 介面。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-108">If you use standard marshaling, the system creates it for you when you call [**CoGetStandardMarshal**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstandardmarshal) (or [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), for creating an aggregated marshaler for lightweight handlers) and also implements the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) and [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) interfaces on the object.</span></span> <span data-ttu-id="e8ab6-109">在伺服器端，有一個對應的系統物件也會執行 **IMarshal**。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-109">On the server side, there is a corresponding system object that also implements **IMarshal**.</span></span> <span data-ttu-id="e8ab6-110">這些物件會以透明的方式處理封送處理。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-110">These objects handle marshaling for you transparently.</span></span>

<span data-ttu-id="e8ab6-111">這些處理常式有兩種您可能想要執行的一般類型：</span><span class="sxs-lookup"><span data-stu-id="e8ab6-111">There are two general types of these handlers that you may want to implement:</span></span>

-   <span data-ttu-id="e8ab6-112">執行服務的處理常式，此服務不需要伺服器的額外資料</span><span class="sxs-lookup"><span data-stu-id="e8ab6-112">A handler that performs a service that requires no extra data from the server</span></span>
-   <span data-ttu-id="e8ab6-113">使用來自伺服器之額外資料的處理常式</span><span class="sxs-lookup"><span data-stu-id="e8ab6-113">A handler that uses extra data from the server</span></span>

<span data-ttu-id="e8ab6-114">伺服器所提供之資料流程中的額外資料可能會用到，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e8ab6-114">Some potential uses of the extra data in the stream supplied by the server are as follows:</span></span>

-   <span data-ttu-id="e8ab6-115">來自伺服器的靜態資料。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-115">Static data from server.</span></span> <span data-ttu-id="e8ab6-116">無論正在封送處理的特定介面為何，伺服器都會將相同的資料寫入資料流程中。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-116">Regardless of the particular interface being marshaled, the server writes the same data into the stream.</span></span>
-   <span data-ttu-id="e8ab6-117">來自伺服器的每個介面資料。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-117">Per-interface data from server.</span></span> <span data-ttu-id="e8ab6-118">根據正在封送處理的特定介面，伺服器可能會將不同的資料寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-118">Depending on which particular interface is being marshaled, the server may write different data into the stream.</span></span>
-   <span data-ttu-id="e8ab6-119">每個介面的協助程式。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-119">Per-interface helpers.</span></span> <span data-ttu-id="e8ab6-120">匯總至用戶端處理常式並委派給標準 proxy 的每個介面 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-120">Per-interface COM components aggregated into the client handler and delegating to the standard proxy.</span></span> <span data-ttu-id="e8ab6-121">例如，若要改善網路效能， [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) 的 COM 元件可以執行資料的用戶端快取、預先讀取、寫入後端、op 鎖定等等。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-121">For example, to improve network performance, a COM component for [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) could do client-side caching of data, read-ahead, write-behind, op-locking, and so forth.</span></span>
-   <span data-ttu-id="e8ab6-122">介面的網路版本。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-122">Network version of an interface.</span></span> <span data-ttu-id="e8ab6-123">介面的網路版本與用戶端和伺服器應用程式程式碼所公開的介面不同。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-123">The network version of the interface is different from the interface exposed by the client and server application code.</span></span> <span data-ttu-id="e8ab6-124">例如，您可以透過相同的網路介面 INetAB，以內嵌伺服器處理常式的方式，將公開的介面 IA 和 IB 多工處理。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-124">It is possible, for example, to multiplex exposed interfaces IA and IB over the same network interface INetAB, the way the embedding server handler does.</span></span> <span data-ttu-id="e8ab6-125">例如，您可以將資料傳輸介面轉換成使用管道的網路介面，以有效率地傳輸資料。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-125">For example, one could convert a data transfer interface into a network interface that uses pipes for efficient data transfer.</span></span>

<span data-ttu-id="e8ab6-126">下層用戶端可能無法進行封送處理具有自訂處理常式的介面，原因有兩種：首先，它們可能不會在匯總伺服器處理常式且物件需要處理常式時，瞭解自訂封送封包中使用的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-126">Down-level clients may not have the capability of unmarshaling interfaces that have custom handlers, for two reasons: First, they may not understand the CLSID used in the custom marshaled packet when the server handler is aggregated and the object wants a handler.</span></span> <span data-ttu-id="e8ab6-127">其次，如果處理常式程式碼需要 COM 的新功能來建立匯總標準封送處理器，並執行遠端 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫，甚至可能不會在用戶端上執行。</span><span class="sxs-lookup"><span data-stu-id="e8ab6-127">Second, the handler code may not even run on the client side if it requires new functionality from COM to create the aggregated standard marshaler and to do remote [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8ab6-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="e8ab6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8ab6-129">OLE 處理常式</span><span class="sxs-lookup"><span data-stu-id="e8ab6-129">The OLE Handler</span></span>](the-ole-handler.md)
</dt> </dl>

 

 