---
title: 關於 NPS 擴充功能
description: 本節說明如何執行 Dll 以擴充 NPS 的功能。 它描述 NPS 和 Dll 之間的互動，並提供有關 Dll 的一些設計考慮。
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106994964"
---
# <a name="about-nps-extensions"></a><span data-ttu-id="0cf89-104">關於 NPS 擴充功能</span><span class="sxs-lookup"><span data-stu-id="0cf89-104">About NPS Extensions</span></span>

> [!Note]  
> <span data-ttu-id="0cf89-105">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="0cf89-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="0cf89-106">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="0cf89-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="0cf89-107">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="0cf89-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="0cf89-108">本節說明如何執行 Dll 以擴充 NPS 的功能。</span><span class="sxs-lookup"><span data-stu-id="0cf89-108">This section describes how to implement DLLs to extend the functionality of NPS.</span></span> <span data-ttu-id="0cf89-109">它描述 NPS 和 Dll 之間的互動，並提供有關 Dll 的一些設計考慮。</span><span class="sxs-lookup"><span data-stu-id="0cf89-109">It describes the interaction between NPS and the DLLs, and presents some design considerations regarding the DLLs.</span></span>

<span data-ttu-id="0cf89-110">NPS 提供兩個擴充點，一個用於驗證，另一個用於授權。</span><span class="sxs-lookup"><span data-stu-id="0cf89-110">NPS provides two extension points, one for authentication and the other for authorization.</span></span> <span data-ttu-id="0cf89-111">驗證是指驗證使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0cf89-111">Authentication refers to verifying the identity of the user.</span></span> <span data-ttu-id="0cf89-112">授權是指決定網路應提供給使用者的服務。</span><span class="sxs-lookup"><span data-stu-id="0cf89-112">Authorization refers to determining what services the network should provide to the user.</span></span> <span data-ttu-id="0cf89-113">這兩個擴充點對應于驗證延伸模組 Dll 和授權延伸 Dll。</span><span class="sxs-lookup"><span data-stu-id="0cf89-113">The two extension points correspond to Authentication Extension DLLs and Authorization Extension DLLs.</span></span> <span data-ttu-id="0cf89-114">每個擴充點都可以支援多個 Dll。</span><span class="sxs-lookup"><span data-stu-id="0cf89-114">Each extension point can support multiple DLLs.</span></span>

<span data-ttu-id="0cf89-115">NPS 提供驗證和授權服務。</span><span class="sxs-lookup"><span data-stu-id="0cf89-115">NPS provides both authentication and authorization services.</span></span> <span data-ttu-id="0cf89-116">NPS 會在內建 NPS 驗證和授權之前呼叫驗證延伸模組 Dll。</span><span class="sxs-lookup"><span data-stu-id="0cf89-116">Authentication Extension DLLs are called by NPS prior to the built-in NPS authentication and authorization.</span></span> <span data-ttu-id="0cf89-117">在 NPS 驗證和授權之後，會呼叫授權延伸 Dll。</span><span class="sxs-lookup"><span data-stu-id="0cf89-117">Authorization Extension DLLs are called after NPS authentication and authorization.</span></span>

<span data-ttu-id="0cf89-118">下圖說明使用擴充 Dll 擴充的 NPS RADIUS 伺服器的封包流程。</span><span class="sxs-lookup"><span data-stu-id="0cf89-118">The following diagram illustrates the flow of packets through an NPS RADIUS server that is expanded using Extension DLLs.</span></span>

![nps 驗證與授權程式](images/ias03.png)

<span data-ttu-id="0cf89-120">如果驗證延伸模組 DLL 傳回 ACCEPT，封包會略過 NPS 驗證並直接前往 NPS 授權。</span><span class="sxs-lookup"><span data-stu-id="0cf89-120">If an Authentication Extension DLL returns ACCEPT, the packet skips the NPS authentication and goes directly to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="0cf89-121">當有多個驗證延伸模組 Dll 時，也會略過其餘的延伸模組 Dll。</span><span class="sxs-lookup"><span data-stu-id="0cf89-121">When multiple Authentication Extension DLLs are present, the rest of the Extension DLLs might be skipped as well.</span></span> <span data-ttu-id="0cf89-122">如需詳細資訊，請參閱 [設定擴充 dll](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) 。</span><span class="sxs-lookup"><span data-stu-id="0cf89-122">See [Setting Up the Extension DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) for more information.</span></span>

 

<span data-ttu-id="0cf89-123">如果驗證延伸模組 DLL 傳回 CONTINUE，封包會前往 NPS 驗證，然後傳送到 NPS 授權。</span><span class="sxs-lookup"><span data-stu-id="0cf89-123">If an Authentication Extension DLL returns CONTINUE, the packet goes to NPS authentication, and then to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="0cf89-124">當有多個驗證延伸模組 Dll 時，會在 NPS 驗證之前叫用其餘的驗證延伸模組 Dll。</span><span class="sxs-lookup"><span data-stu-id="0cf89-124">When multiple Authentication Extension DLLs are present, the rest of the Authentication Extension DLLs are invoked before NPS authentication.</span></span>

 

<span data-ttu-id="0cf89-125">下列主題會更詳細地說明擴充 Dll：</span><span class="sxs-lookup"><span data-stu-id="0cf89-125">The following topics describe the Extension DLLs in more detail:</span></span>

-   [<span data-ttu-id="0cf89-126">設定延伸模組 Dll</span><span class="sxs-lookup"><span data-stu-id="0cf89-126">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [<span data-ttu-id="0cf89-127">叫用擴充 Dll</span><span class="sxs-lookup"><span data-stu-id="0cf89-127">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [<span data-ttu-id="0cf89-128">使用者識別屬性</span><span class="sxs-lookup"><span data-stu-id="0cf89-128">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)

 

 