---
title: WinRM c + + API
description: Windows 遠端管理介面可以用來取得資料或管理遠端電腦上的資源。 此 API 主要是供內部使用。 建議您盡可能使用 WinRM 用戶端 Shell API。
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932372"
---
# <a name="winrm-c-api"></a><span data-ttu-id="d220a-105">WinRM c + + API</span><span class="sxs-lookup"><span data-stu-id="d220a-105">WinRM C++ API</span></span>

<span data-ttu-id="d220a-106">Windows 遠端管理介面可以用來取得資料或管理遠端電腦上的 [*資源*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="d220a-106">The Windows Remote Management interfaces can be used to obtain data or manage [*resources*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="d220a-107">此 API 主要是供內部使用。</span><span class="sxs-lookup"><span data-stu-id="d220a-107">This API is intended primarily for internal use.</span></span> <span data-ttu-id="d220a-108">建議您盡可能使用 [WinRM 用戶端 SHELL API](client-shell-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="d220a-108">We recommend using the [WinRM Client Shell API](client-shell-api.md) instead whenever possible.</span></span> <span data-ttu-id="d220a-109">介面會緊密對應至 [WinRM 腳本 API](winrm-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d220a-109">The interfaces closely correspond to the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="d220a-110">直接從 **IDispatch** 繼承的 WinRM 介面具有對應的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="d220a-110">The WinRM interfaces that inherit directly from **IDispatch** each have a corresponding scripting object.</span></span> <span data-ttu-id="d220a-111">如需詳細資訊，請參閱 [WinRM 腳本 API](winrm-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d220a-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="d220a-112">針對多執行緒應用程式，WinRM 不支援存取相同 [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) 物件的個別執行緒。</span><span class="sxs-lookup"><span data-stu-id="d220a-112">For multithreaded applications, WinRM does not support separate threads accessing the same [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) object.</span></span>

<span data-ttu-id="d220a-113">下列是 WinRM 提供的介面。</span><span class="sxs-lookup"><span data-stu-id="d220a-113">The following interfaces are provided by WinRM.</span></span>

<dl> <dt>

<span data-ttu-id="d220a-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="d220a-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="d220a-115">提供用來建立新會話和管理已建立會話的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="d220a-115">Provides methods and properties used to create a new session and manage an established session.</span></span> <span data-ttu-id="d220a-116">[**WSMan**](wsman.md) 是對應的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="d220a-116">[**WSMan**](wsman.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d220a-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="d220a-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="d220a-118">提供用來建立新 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="d220a-118">Provides methods and properties used to create a new [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span> <span data-ttu-id="d220a-119">這種方法適用于 [**WSMan**](wsman.md) 腳本物件。</span><span class="sxs-lookup"><span data-stu-id="d220a-119">This method is available for the [**WSMan**](wsman.md) scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d220a-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span><span class="sxs-lookup"><span data-stu-id="d220a-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span></span>
</dt> <dd>

<span data-ttu-id="d220a-121">定義用於遠端連線的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="d220a-121">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="d220a-122">[**ConnectionOptions**](connectionoptions.md) 是對應的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="d220a-122">[**ConnectionOptions**](connectionoptions.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d220a-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**Iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="d220a-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span></span>
</dt> <dd>

<span data-ttu-id="d220a-124">定義會話可用的網路作業和屬性。</span><span class="sxs-lookup"><span data-stu-id="d220a-124">Defines the network operations and properties available for the session.</span></span> <span data-ttu-id="d220a-125">[**Session**](session.md) 是對應的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="d220a-125">[**Session**](session.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d220a-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span><span class="sxs-lookup"><span data-stu-id="d220a-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span></span>
</dt> <dd>

<span data-ttu-id="d220a-127">代表列舉資源時傳回的結果集合。</span><span class="sxs-lookup"><span data-stu-id="d220a-127">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="d220a-128">[**列舉**](enumerator.md) 值是對應的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="d220a-128">[**Enumerator**](enumerator.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d220a-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="d220a-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span></span>
</dt> <dd>

<span data-ttu-id="d220a-130">提供資源的路徑。</span><span class="sxs-lookup"><span data-stu-id="d220a-130">Supplies the path to a resource.</span></span> <span data-ttu-id="d220a-131">您可以使用 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)物件，而不是 [**會話**](session.md)物件作業中的 [*資源 URI*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="d220a-131">You can use an [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="d220a-132">[**ResourceLocator**](resourcelocator.md) 是對應的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="d220a-132">[**ResourceLocator**](resourcelocator.md) is the corresponding scripting object.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d220a-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="d220a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d220a-134">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="d220a-134">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




