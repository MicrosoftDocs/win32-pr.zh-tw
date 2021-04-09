---
title: 使用 QueryService 來取出 IAccessible 物件的原生介面
description: 伺服器開發人員可以使用這項技術，將指標公開給 IAccessible 物件的自訂檔節點。 這假設您已經公開 IAccessible 物件。 這項技術可讓用戶端從 IAccessible 物件取得自訂物件。
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d971462154eb12789a74e8cc6edb5aed68c84b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023772"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a><span data-ttu-id="0839c-105">使用 QueryService 來取出 IAccessible 物件的原生介面</span><span class="sxs-lookup"><span data-stu-id="0839c-105">Use QueryService to retrieve a native interface for an IAccessible object</span></span>

<span data-ttu-id="0839c-106">伺服器開發人員可以使用這項技術，將指標公開給 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件的自訂檔節點。</span><span class="sxs-lookup"><span data-stu-id="0839c-106">Server developers can use this technique to expose a pointer to a custom document node for an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span> <span data-ttu-id="0839c-107">這假設您已經公開 **IAccessible** 物件。</span><span class="sxs-lookup"><span data-stu-id="0839c-107">This assumes that you already expose **IAccessible** objects.</span></span> <span data-ttu-id="0839c-108">這項技術可讓用戶端從 **IAccessible** 物件取得自訂物件。</span><span class="sxs-lookup"><span data-stu-id="0839c-108">This technique allows clients to get a custom object from an **IAccessible** object.</span></span>

<span data-ttu-id="0839c-109">**若要公開 IAccessible (伺服器的原生物件模型)**</span><span class="sxs-lookup"><span data-stu-id="0839c-109">**To expose a native object model for an IAccessible (servers)**</span></span>

1.  <span data-ttu-id="0839c-110">在 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件上加入 **IServiceProvider** 介面的支援。</span><span class="sxs-lookup"><span data-stu-id="0839c-110">Add support for the **IServiceProvider** interface on your [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>
2.  <span data-ttu-id="0839c-111">定義 GUID，代表從 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件取得自訂介面的功能。</span><span class="sxs-lookup"><span data-stu-id="0839c-111">Define a GUID that represents the functionality of obtaining the custom interface from an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) objects.</span></span> <span data-ttu-id="0839c-112">這稱為服務識別碼。</span><span class="sxs-lookup"><span data-stu-id="0839c-112">This is called a service ID.</span></span> <span data-ttu-id="0839c-113">如果您有自訂介面，您可以使用 GUIDGEN.EXE 來產生服務識別碼，或重複使用介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="0839c-113">You can use GUIDGEN.EXE to generate a service ID, or reuse the interface ID if you have a custom interface.</span></span>
3.  <span data-ttu-id="0839c-114">執行 **IServiceProvider：： QueryService** 方法，如此一來，當使用此程式稍早定義的服務識別碼呼叫自訂介面時，它就會傳回該介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0839c-114">Implement the **IServiceProvider::QueryService** method so that it returns a pointer to the custom interface when called with the service ID defined earlier in this procedure.</span></span> <span data-ttu-id="0839c-115">**QueryService** 應該針對所有其他服務識別碼值傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0839c-115">**QueryService** should return **NULL** for all other service ID values.</span></span>
4.  <span data-ttu-id="0839c-116">發佈服務識別碼，讓用戶端可以使用它。</span><span class="sxs-lookup"><span data-stu-id="0839c-116">Publish the service ID so that clients can use it.</span></span>

<span data-ttu-id="0839c-117">用戶端可以使用此功能，從 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件取得自訂物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0839c-117">Clients can use this functionality to obtain a pointer to the custom object from an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>

<span data-ttu-id="0839c-118">**從 IAccessible (用戶端取得自訂物件的指標)**</span><span class="sxs-lookup"><span data-stu-id="0839c-118">**To obtain a pointer to a custom object from an IAccessible (clients)**</span></span>

1.  <span data-ttu-id="0839c-119">[](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) \_ 在 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標上呼叫 QueryInterface (IID IServiceProvider) ，以取得 **IServiceProvider** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0839c-119">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(IID\_IServiceProvider) on an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to obtain an **IServiceProvider** interface pointer.</span></span>
2.  <span data-ttu-id="0839c-120">使用已發佈的服務識別碼呼叫 **IServiceProvider：： QueryService** ，以取得 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)之自訂物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0839c-120">Call **IServiceProvider::QueryService** with the published service ID to obtain a pointer to the custom object for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>
3.  <span data-ttu-id="0839c-121">如果不再需要，請釋放 **IServiceProvider** 介面。</span><span class="sxs-lookup"><span data-stu-id="0839c-121">Release the **IServiceProvider** interface if it is no longer needed.</span></span>

<span data-ttu-id="0839c-122">若要跨進程使用，伺服器可能需要向元件物件模型註冊傳回的介面 (COM) 。</span><span class="sxs-lookup"><span data-stu-id="0839c-122">To be usable across processes, servers might need to register the returned interface with Component Object Model (COM).</span></span>

<span data-ttu-id="0839c-123">Microsoft Internet Explorer 4.0 和更新版本使用此技術。</span><span class="sxs-lookup"><span data-stu-id="0839c-123">This technique is used by Microsoft Internet Explorer 4.0 and later.</span></span> <span data-ttu-id="0839c-124">它可讓用戶端取得對應至 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件的 **IHTMLElement2** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0839c-124">It allows clients to obtain an **IHTMLElement2** interface pointer that corresponds to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>

 

 