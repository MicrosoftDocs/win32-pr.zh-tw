---
title: 使用 IProvideClassInfo
description: 使用 IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024165"
---
# <a name="using-iprovideclassinfo"></a><span data-ttu-id="d4051-103">使用 IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="d4051-103">Using IProvideClassInfo</span></span>

<span data-ttu-id="d4051-104">可連線物件可提供 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 和 [**iprovideclassinfo2.getguid**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) 介面，讓其用戶端可以輕鬆地檢查其類型資訊。</span><span class="sxs-lookup"><span data-stu-id="d4051-104">A connectable object can offer the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) interfaces so that its clients can easily examine its type information.</span></span> <span data-ttu-id="d4051-105">這項功能在處理輸出介面時很重要，因為定義是由物件定義，但由用戶端在其本身的接收物件上執行。</span><span class="sxs-lookup"><span data-stu-id="d4051-105">This capability is important when dealing with outgoing interfaces, which, by definition, are defined by an object but implemented by a client on its own sink object.</span></span> <span data-ttu-id="d4051-106">在某些情況下，在編譯時期，可連接的物件和接收物件都知道輸出介面;這就是 [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)的情況。</span><span class="sxs-lookup"><span data-stu-id="d4051-106">In some cases, an outgoing interface is known at compile time to both the connectable object and the sink object; such is the case with [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span></span>

<span data-ttu-id="d4051-107">不過，在其他情況下，只有可連接的物件會在編譯時期知道它的輸出介面定義。</span><span class="sxs-lookup"><span data-stu-id="d4051-107">In other cases, however, only the connectable object knows its outgoing interface definitions at compile time.</span></span> <span data-ttu-id="d4051-108">在這些情況下，用戶端必須取得輸出介面的型別資訊，讓它能夠動態提供支援正確進入點的接收，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d4051-108">In these cases, the client must obtain the type information for the outgoing interface so that it can dynamically provide a sink supporting the right entry points, as follows:</span></span>

1.  <span data-ttu-id="d4051-109">用戶端會列舉連接點，然後取得可連線物件所支援之輸出介面的 Iid，針對每個連接點呼叫 [**IConnectionPoint：： GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) 。</span><span class="sxs-lookup"><span data-stu-id="d4051-109">The client enumerates the connection points and then, to obtain the IIDs of outgoing interfaces supported by the connectable object, calls [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) for each connection point.</span></span>
2.  <span data-ttu-id="d4051-110">用戶端會查詢其中一個 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 介面的可連線物件。</span><span class="sxs-lookup"><span data-stu-id="d4051-110">The client queries the connectable object for one of the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces.</span></span>
3.  <span data-ttu-id="d4051-111">用戶端會呼叫 [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) 介面中的方法，以取得輸出介面的型別資訊。</span><span class="sxs-lookup"><span data-stu-id="d4051-111">The client calls methods in the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces to get the type information for the outgoing interface.</span></span>
4.  <span data-ttu-id="d4051-112">用戶端會建立支援輸出介面的接收物件。</span><span class="sxs-lookup"><span data-stu-id="d4051-112">The client creates a sink object supporting the outgoing interface.</span></span>
5.  <span data-ttu-id="d4051-113">此程式會繼續，且用戶端會呼叫 [**IConnectionPoint：： Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) 將其接收連接到連接點。</span><span class="sxs-lookup"><span data-stu-id="d4051-113">The process continues, and the client calls [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) to connect its sink to the connection point.</span></span>

<span data-ttu-id="d4051-114">在類型資訊中，屬性 [**來源**](/windows/desktop/Midl/source)會將 [**coclass**](/windows/desktop/Midl/coclass)底下所 [**列的**](/windows/desktop/Midl/dispinterface)[**介面**](/windows/desktop/Midl/interface)或介面介面標示為連出介面。</span><span class="sxs-lookup"><span data-stu-id="d4051-114">In the type information, the attribute [**source**](/windows/desktop/Midl/source) marks an [**interface**](/windows/desktop/Midl/interface) or [**dispinterface**](/windows/desktop/Midl/dispinterface) listed under a [**coclass**](/windows/desktop/Midl/coclass) as an outgoing interface.</span></span> <span data-ttu-id="d4051-115">如果未列出此屬性，則會將其視為傳入介面。</span><span class="sxs-lookup"><span data-stu-id="d4051-115">Those listed without this attribute are considered incoming interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4051-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4051-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4051-117">可連線物件介面</span><span class="sxs-lookup"><span data-stu-id="d4051-117">Connectable Object Interfaces</span></span>](connectable-object-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d4051-118">提供類別資訊</span><span class="sxs-lookup"><span data-stu-id="d4051-118">Providing Class Information</span></span>](providing-class-information.md)
</dt> </dl>

 

 