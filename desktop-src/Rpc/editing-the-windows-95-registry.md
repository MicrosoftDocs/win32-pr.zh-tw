---
title: 編輯 Windows 95 登錄
description: 您可以使用 REGEDIT 來編輯 Windows 95 登錄，以指定 NSP。
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840656"
---
# <a name="editing-the-windows-95-registry"></a><span data-ttu-id="5f315-103">編輯 Windows 95 登錄</span><span class="sxs-lookup"><span data-stu-id="5f315-103">Editing the Windows 95 Registry</span></span>

<span data-ttu-id="5f315-104">您可以使用 REGEDIT 來編輯 Windows 95 登錄，以指定 NSP。</span><span class="sxs-lookup"><span data-stu-id="5f315-104">You can use REGEDIT to edit the Windows 95 registry to designate an NSP.</span></span>

<span data-ttu-id="5f315-105">**為 Windows 95 指定 Microsoft 定位器名稱服務提供者**</span><span class="sxs-lookup"><span data-stu-id="5f315-105">**To designate a Microsoft Locator name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="5f315-106">選取</span><span class="sxs-lookup"><span data-stu-id="5f315-106">Select</span></span>

    <span data-ttu-id="5f315-107">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Rpc**</span><span class="sxs-lookup"><span data-stu-id="5f315-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="5f315-108">建立稱為的新機碼</span><span class="sxs-lookup"><span data-stu-id="5f315-108">Create a new key called</span></span>

    <span data-ttu-id="5f315-109">**NameService**</span><span class="sxs-lookup"><span data-stu-id="5f315-109">**NameService**</span></span>

3.  <span data-ttu-id="5f315-110">選取 **NameService** 索引鍵時，請建立新的 **StringValue** 名稱，並將其修改為包含下表所示的資料。</span><span class="sxs-lookup"><span data-stu-id="5f315-110">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="5f315-111">Name</span><span class="sxs-lookup"><span data-stu-id="5f315-111">Name</span></span>                     | <span data-ttu-id="5f315-112">資料</span><span class="sxs-lookup"><span data-stu-id="5f315-112">Data</span></span>                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="5f315-113">**DefaultSyntax**</span><span class="sxs-lookup"><span data-stu-id="5f315-113">**DefaultSyntax**</span></span>        | <span data-ttu-id="5f315-114">3</span><span class="sxs-lookup"><span data-stu-id="5f315-114">3</span></span><br/>                                                                |
    | <span data-ttu-id="5f315-115">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="5f315-115">**Protocol**</span></span>             | <span data-ttu-id="5f315-116">ncacn \_ np</span><span class="sxs-lookup"><span data-stu-id="5f315-116">ncacn\_np</span></span><br/>                                                        |
    | <span data-ttu-id="5f315-117">**端點**</span><span class="sxs-lookup"><span data-stu-id="5f315-117">**Endpoint**</span></span>             | <span data-ttu-id="5f315-118">\\管道 \\ 定位器</span><span class="sxs-lookup"><span data-stu-id="5f315-118">\\pipe\\locator</span></span><br/>                                                  |
    | <span data-ttu-id="5f315-119">**Networkaddress.cache.ttl**</span><span class="sxs-lookup"><span data-stu-id="5f315-119">**NetworkAddress**</span></span>       | <span data-ttu-id="5f315-120">myserver (其中 myserver 是 Windows NT 電腦的名稱) </span><span class="sxs-lookup"><span data-stu-id="5f315-120">myserver (where myserver is the name of the Windows NT computer)</span></span><br/> |
    | <span data-ttu-id="5f315-121">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="5f315-121">**ServerNetworkAddress**</span></span> | <span data-ttu-id="5f315-122">myserver</span><span class="sxs-lookup"><span data-stu-id="5f315-122">myserver</span></span><br/>                                                         |

    

     

<span data-ttu-id="5f315-123">您可以使用 REGEDIT 來編輯 Windows 95 登錄，以指定 DCE CD NSP。</span><span class="sxs-lookup"><span data-stu-id="5f315-123">You can use REGEDIT to edit the Windows 95 registry to designate a DCE CDS NSP.</span></span>

<span data-ttu-id="5f315-124">**為 Windows 95 指定 DCE CD 名稱服務提供者**</span><span class="sxs-lookup"><span data-stu-id="5f315-124">**To designate a DCE CDS name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="5f315-125">選取</span><span class="sxs-lookup"><span data-stu-id="5f315-125">Select</span></span>

    <span data-ttu-id="5f315-126">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Rpc**</span><span class="sxs-lookup"><span data-stu-id="5f315-126">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="5f315-127">建立稱為的新機碼</span><span class="sxs-lookup"><span data-stu-id="5f315-127">Create a new key called</span></span>

    <span data-ttu-id="5f315-128">**NameService**</span><span class="sxs-lookup"><span data-stu-id="5f315-128">**NameService**</span></span>

3.  <span data-ttu-id="5f315-129">選取 **NameService** 索引鍵時，請建立新的 **StringValue** 名稱，並將其修改為包含下表所示的資料。</span><span class="sxs-lookup"><span data-stu-id="5f315-129">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="5f315-130">Name</span><span class="sxs-lookup"><span data-stu-id="5f315-130">Name</span></span>                     | <span data-ttu-id="5f315-131">資料</span><span class="sxs-lookup"><span data-stu-id="5f315-131">Data</span></span>                                                             |
    |--------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="5f315-132">**DefaultSyntax**</span><span class="sxs-lookup"><span data-stu-id="5f315-132">**DefaultSyntax**</span></span>        | <span data-ttu-id="5f315-133">3</span><span class="sxs-lookup"><span data-stu-id="5f315-133">3</span></span><br/>                                                     |
    | <span data-ttu-id="5f315-134">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="5f315-134">**Protocol**</span></span>             | <span data-ttu-id="5f315-135">ncacn \_ ip \_ tcp</span><span class="sxs-lookup"><span data-stu-id="5f315-135">ncacn\_ip\_tcp</span></span><br/>                                        |
    | <span data-ttu-id="5f315-136">**端點**</span><span class="sxs-lookup"><span data-stu-id="5f315-136">**Endpoint**</span></span>             | <span data-ttu-id="5f315-137">"" (空字串) </span><span class="sxs-lookup"><span data-stu-id="5f315-137">"" (an empty string)</span></span><br/>                                  |
    | <span data-ttu-id="5f315-138">**Networkaddress.cache.ttl**</span><span class="sxs-lookup"><span data-stu-id="5f315-138">**NetworkAddress**</span></span>       | <span data-ttu-id="5f315-139">myserver (執行 nsid 的主電腦名稱稱) </span><span class="sxs-lookup"><span data-stu-id="5f315-139">myserver (the name of the host computer running nsid)</span></span><br/> |
    | <span data-ttu-id="5f315-140">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="5f315-140">**ServerNetworkAddress**</span></span> | <span data-ttu-id="5f315-141">myserver (執行 nsid 的主電腦名稱稱) </span><span class="sxs-lookup"><span data-stu-id="5f315-141">myserver (the name of the host computer running nsid)</span></span><br/> |

    

     

    > [!Note]  
    > <span data-ttu-id="5f315-142">您必須具有數位設備公司的 DCE Cell Directory 服務產品，才能將 DCE CD 設定為您的名稱服務提供者。</span><span class="sxs-lookup"><span data-stu-id="5f315-142">You must have the Digital Equipment Corporation DCE Cell Directory Service product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="5f315-143">請參閱數位設備公司提供的檔，以取得 DCE CD 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5f315-143">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

     

 

 





