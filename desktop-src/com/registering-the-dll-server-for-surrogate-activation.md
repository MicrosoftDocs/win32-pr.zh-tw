---
title: 註冊 DLL 伺服器以進行代理程式啟用
description: 註冊 DLL 伺服器以進行代理程式啟用
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683149"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a><span data-ttu-id="e2f34-103">註冊 DLL 伺服器以進行代理程式啟用</span><span class="sxs-lookup"><span data-stu-id="e2f34-103">Registering the DLL Server for Surrogate Activation</span></span>

<span data-ttu-id="e2f34-104">在下列情況下，將會在代理程式中載入 DLL 伺服器：</span><span class="sxs-lookup"><span data-stu-id="e2f34-104">A DLL server will be loaded into a surrogate process under the following conditions:</span></span>

-   <span data-ttu-id="e2f34-105">登錄中的 CLSID 機碼底下必須指定 AppID 值，以及對應的 [appid](appid-key.md) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="e2f34-105">There must be an AppID value specified under the CLSID key in the registry, and a corresponding [AppID](appid-key.md) key.</span></span>
-   <span data-ttu-id="e2f34-106">在啟用呼叫中，會 [**設定 \_ CLSCTX \_ 本機伺服器**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) 位，而且 CLSID 機碼不會指定 [LocalServer32](localserver32.md)、 [LocalServer](localserver.md)或 [LocalService](localservice.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f34-106">In an activation call, the [**CLSCTX\_LOCAL\_SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) bit is set and the CLSID key does not specify [LocalServer32](localserver32.md), [LocalServer](localserver.md), or [LocalService](localservice.md).</span></span> <span data-ttu-id="e2f34-107">如果設定了其他 **CLSCTX** 位，則會遵循同進程、本機或遠端執行旗標的 [**處理演算法**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)。</span><span class="sxs-lookup"><span data-stu-id="e2f34-107">If other **CLSCTX** bits are set, the [**processing algorithm**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)for the in-process, local, or remote execution flags is followed.</span></span>
-   <span data-ttu-id="e2f34-108">CLSID 機碼包含 [InprocServer32](inprocserver32.md) 子機碼。</span><span class="sxs-lookup"><span data-stu-id="e2f34-108">The CLSID key contains the [InprocServer32](inprocserver32.md) subkey.</span></span>
-   <span data-ttu-id="e2f34-109">**InprocServer32** 索引鍵中指定的 proxy/stub DLL 存在。</span><span class="sxs-lookup"><span data-stu-id="e2f34-109">The proxy/stub DLL specified in the **InprocServer32** key exists.</span></span>
-   <span data-ttu-id="e2f34-110">[DllSurrogate](dllsurrogate.md)值存在於 **AppID** 索引鍵下。</span><span class="sxs-lookup"><span data-stu-id="e2f34-110">The [DllSurrogate](dllsurrogate.md) value exists under the **AppID** key.</span></span>

<span data-ttu-id="e2f34-111">如果有 **LocalServer**、 **LocalServer32** 或 **LocalService**，指出 exe 是否存在，exe 伺服器或服務將一律會依喜好啟動，以將 DLL 伺服器載入至代理程式。</span><span class="sxs-lookup"><span data-stu-id="e2f34-111">If there is a **LocalServer**, **LocalServer32**, or **LocalService**, indicating the existence of an EXE, the EXE server or service will always be launched in preference to loading a DLL server into a surrogate process.</span></span>

<span data-ttu-id="e2f34-112">必須指定 **DllSurrogate** 的命名值，才能進行代理程式啟用。</span><span class="sxs-lookup"><span data-stu-id="e2f34-112">The **DllSurrogate** named-value must be specified for surrogate activation to occur.</span></span> <span data-ttu-id="e2f34-113">啟用指的是對下列任何啟用函數的呼叫：</span><span class="sxs-lookup"><span data-stu-id="e2f34-113">Activation refers to calls to any of the following activation functions:</span></span>

-   [<span data-ttu-id="e2f34-114">**CoGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="e2f34-114">**CoGetClassObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [<span data-ttu-id="e2f34-115">**CoCreateInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="e2f34-115">**CoCreateInstanceEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [<span data-ttu-id="e2f34-116">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="e2f34-116">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [<span data-ttu-id="e2f34-117">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="e2f34-117">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [<span data-ttu-id="e2f34-118">**IMoniker：： BindToObject**</span><span class="sxs-lookup"><span data-stu-id="e2f34-118">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

<span data-ttu-id="e2f34-119">若要啟動系統提供的代理程式實例，請將 **DllSurrogate** 的值設為空字串或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e2f34-119">To launch an instance of the system-supplied surrogate, set the value of **DllSurrogate** either to an empty string or to **NULL**.</span></span> <span data-ttu-id="e2f34-120">若要指定啟動自訂代理，請將值設定為代理的路徑。</span><span class="sxs-lookup"><span data-stu-id="e2f34-120">To specify the launch of a custom surrogate, set the value to the path of the surrogate.</span></span>

<span data-ttu-id="e2f34-121">如果 [RemoteServerName](remoteservername.md) 和 **DllSurrogate** 都指定給相同的 AppID，則會忽略 **RemoteServerName** 值，而且 **DllSurrogate** 值會導致本機電腦啟用。</span><span class="sxs-lookup"><span data-stu-id="e2f34-121">If both [RemoteServerName](remoteservername.md) and **DllSurrogate** are specified for the same AppID, the **RemoteServerName** value is ignored and the **DllSurrogate** value causes an activation on the local computer.</span></span> <span data-ttu-id="e2f34-122">若為遠端代理啟用，請在用戶端上指定 **RemoteServerName** 但不指定 **DllSurrogate** ，並在伺服器上指定 **DllSurrogate** 。</span><span class="sxs-lookup"><span data-stu-id="e2f34-122">For remote surrogate activation, specify **RemoteServerName** but not **DllSurrogate** on the client, and specify **DllSurrogate** on the server.</span></span>

<span data-ttu-id="e2f34-123">設計為一律在本身的代理程式中單獨執行的 DLL 伺服器，最好是以 AppID 等於其 CLSID 來設定。</span><span class="sxs-lookup"><span data-stu-id="e2f34-123">A DLL server that is designed to always run alone in its own surrogate process is best configured with an AppID equal its CLSID.</span></span> <span data-ttu-id="e2f34-124">在 **AppID** 下，只要以空字串值指定 **DllSurrogate** 。</span><span class="sxs-lookup"><span data-stu-id="e2f34-124">Under **AppID**, simply specify a **DllSurrogate** named-value with an empty string value.</span></span>

<span data-ttu-id="e2f34-125">最好是設定 DLL 伺服器，其設計目的是要在自己的代理程式中單獨執行，並使用 **AppID** 登錄機碼下指定的 [RunAs](runas.md)值，為網路上的多個用戶端提供服務。</span><span class="sxs-lookup"><span data-stu-id="e2f34-125">It is best to configure a DLL server that is designed to run alone in its own surrogate process and to service multiple clients across a network with a [RunAs](runas.md) value specified under the **AppID** registry key.</span></span> <span data-ttu-id="e2f34-126">**RunAs** 是否指定「互動式使用者」或特定使用者身分識別，取決於使用者介面、安全性和其他伺服器需求。</span><span class="sxs-lookup"><span data-stu-id="e2f34-126">Whether the **RunAs** specifies "Interactive User" or a specific user identity depends upon the user interface, security, and other server requirements.</span></span> <span data-ttu-id="e2f34-127">如果指定了 **RunAs** 值，不論用戶端的身分識別為何，都只會載入一個伺服器實例來服務所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="e2f34-127">When a **RunAs** value is specified, only one instance of the server is loaded to service all of the clients, regardless of the identity of the client.</span></span> <span data-ttu-id="e2f34-128">另一方面，如果目的是要在代理中執行一個 DLL 伺服器實例，以服務每個遠端用戶端身分識別，請勿使用 **RunAs** 設定伺服器。</span><span class="sxs-lookup"><span data-stu-id="e2f34-128">On the other hand, do not configure the server with **RunAs** if the intention is to have one instance of the DLL server running in surrogate to service each remote client identity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2f34-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e2f34-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2f34-130">DLL 伺服器需求</span><span class="sxs-lookup"><span data-stu-id="e2f34-130">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="e2f34-131">代理共用</span><span class="sxs-lookup"><span data-stu-id="e2f34-131">Surrogate Sharing</span></span>](surrogate-sharing.md)
</dt> </dl>

 

 