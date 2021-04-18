---
title: WinRM 腳本 API
description: Windows 遠端管理腳本物件會實作為 WS-Management 通訊協定之上的一層。
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965601"
---
# <a name="winrm-scripting-api"></a><span data-ttu-id="f2bb3-103">WinRM 腳本 API</span><span class="sxs-lookup"><span data-stu-id="f2bb3-103">WinRM Scripting API</span></span>

<span data-ttu-id="f2bb3-104">Windows 遠端管理腳本物件會實作為 [WS-Management 通訊協定](ws-management-protocol.md)之上的一層。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-104">Windows Remote Management scripting objects are implemented as a layer above the [WS-Management Protocol](ws-management-protocol.md).</span></span> <span data-ttu-id="f2bb3-105">腳本物件可讓您取得資料或管理本機和遠端電腦上的 [*資源*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-105">The scripting objects enable you to obtain data or manage [*resources*](windows-remote-management-glossary.md) on local and remote computers.</span></span>

## <a name="ws-management-objects"></a><span data-ttu-id="f2bb3-106">WS-Management 物件</span><span class="sxs-lookup"><span data-stu-id="f2bb3-106">WS-Management Objects</span></span>

<span data-ttu-id="f2bb3-107">每個腳本物件都有對應的 c + + 介面。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-107">Each scripting object has a corresponding C++ interface.</span></span> <span data-ttu-id="f2bb3-108">如需詳細資訊，請參閱 [WinRM c + + API](winrm-c---api.md) 和 [腳本（Windows 遠端管理](scripting-in-windows-remote-management.md)）。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-108">For more information, see [WinRM C++ API](winrm-c---api.md) and [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="f2bb3-109">以下是由 WinRM 腳本 API 提供的物件。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-109">The following objects are provided by the WinRM Scripting API.</span></span>

<dl> <dt>

<span data-ttu-id="f2bb3-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span><span class="sxs-lookup"><span data-stu-id="f2bb3-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span></span>
</dt> <dd>

<span data-ttu-id="f2bb3-111">定義用於遠端連線的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-111">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="f2bb3-112">呼叫 [**CreateConnectionOptions**](wsman-createconnectionoptions.md) 方法時，會傳遞使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-112">The user name and password are passed when calling the [**CreateConnectionOptions**](wsman-createconnectionoptions.md) method.</span></span> <span data-ttu-id="f2bb3-113">如需詳細資訊，請參閱 [從遠端電腦取得資料](obtaining-data-from-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-113">For more information, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="f2bb3-114">對應的 c + + 介面為 [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-114">The corresponding C++ interface is [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span></span>

</dd> <dt>

<span data-ttu-id="f2bb3-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**枚舉 數**](enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="f2bb3-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)</span></span>
</dt> <dd>

<span data-ttu-id="f2bb3-116">代表列舉資源時傳回的結果集合。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-116">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="f2bb3-117">如需詳細資訊，請參閱 [列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-117">For more information, see [Enumerating or Listing All the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span> <span data-ttu-id="f2bb3-118">對應的 c + + 介面為 [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-118">The corresponding C++ interface is [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="f2bb3-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span><span class="sxs-lookup"><span data-stu-id="f2bb3-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span></span>
</dt> <dd>

<span data-ttu-id="f2bb3-120">提供資源的路徑。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-120">Supplies the path to a resource.</span></span> <span data-ttu-id="f2bb3-121">您可以使用 [**ResourceLocator**](resourcelocator.md)物件，而不是 [**會話**](session.md)物件作業中的 [*資源 URI*](windows-remote-management-glossary.md) ，例如 [**session、Get**](session-get.md)、 [**session、Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-121">You can use a [**ResourceLocator**](resourcelocator.md) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations, such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="f2bb3-122">對應的 c + + 介面為 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-122">The corresponding C++ interface is [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span>

</dd> <dt>

<span data-ttu-id="f2bb3-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**會話**](session.md)</span><span class="sxs-lookup"><span data-stu-id="f2bb3-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)</span></span>
</dt> <dd>

<span data-ttu-id="f2bb3-124">定義會話可用的網路作業和屬性，例如 [**session. Get**](session-get.md)、 [**session. 列舉**](session-enumerate.md)、 [**session。 Invoke**](session-invoke.md)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-124">Defines the network operations and properties available for the session, such as [**Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md).</span></span> <span data-ttu-id="f2bb3-125">如需詳細資訊，請參閱 [從本機電腦取得資料](obtaining-data-from-the-local-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-125">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span> <span data-ttu-id="f2bb3-126">對應的 c + + 介面為 [**iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-126">The corresponding C++ interface is [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span></span>

</dd> <dt>

<span data-ttu-id="f2bb3-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span><span class="sxs-lookup"><span data-stu-id="f2bb3-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span></span>
</dt> <dd>

<span data-ttu-id="f2bb3-128">提供用來建立新會話或管理已建立會話的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-128">Provides methods and properties used to create a new session or manage an established session.</span></span> <span data-ttu-id="f2bb3-129">如需詳細資訊，請參閱 [使用 Windows 遠端管理](using-windows-remote-management.md)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-129">For more information see, [Using Windows Remote Management](using-windows-remote-management.md).</span></span> <span data-ttu-id="f2bb3-130">對應的 c + + 介面為 [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) 和 [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)。</span><span class="sxs-lookup"><span data-stu-id="f2bb3-130">The corresponding C++ interfaces are [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="f2bb3-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2bb3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2bb3-132">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="f2bb3-132">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="f2bb3-133">使用 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="f2bb3-133">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="f2bb3-134">Windows 遠端管理中的腳本</span><span class="sxs-lookup"><span data-stu-id="f2bb3-134">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="f2bb3-135">Windows 遠端管理參考</span><span class="sxs-lookup"><span data-stu-id="f2bb3-135">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




