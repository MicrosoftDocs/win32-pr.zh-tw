---
description: IWbemPath 介面會公開下列方法。
ms.assetid: 36EC7EF6-5CCA-4D18-AB09-9EE41D1B9524
ms.tgt_platform: multiple
title: IWbemPath 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ae802fd7741e5b1317160991a50bd2a535a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192193"
---
# <a name="iwbempath-methods"></a><span data-ttu-id="23f9a-103">IWbemPath 方法</span><span class="sxs-lookup"><span data-stu-id="23f9a-103">IWbemPath Methods</span></span>

<span data-ttu-id="23f9a-104">[**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="23f9a-104">The [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="23f9a-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="23f9a-105">In this section</span></span>

-   [<span data-ttu-id="23f9a-106">**CreateClassPart 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-106">**CreateClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-createclasspart)
-   [<span data-ttu-id="23f9a-107">**DeleteClassPart 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-107">**DeleteClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-deleteclasspart)
-   [<span data-ttu-id="23f9a-108">**GetClassName 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-108">**GetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getclassname)
-   [<span data-ttu-id="23f9a-109">**GetInfo 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-109">**GetInfo method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getinfo)
-   [<span data-ttu-id="23f9a-110">**GetKeyList 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-110">**GetKeyList method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getkeylist)
-   [<span data-ttu-id="23f9a-111">**GetNamespaceAt 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-111">**GetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespaceat)
-   [<span data-ttu-id="23f9a-112">**GetNamespaceCount 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-112">**GetNamespaceCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespacecount)
-   [<span data-ttu-id="23f9a-113">**GetScope 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-113">**GetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscope)
-   [<span data-ttu-id="23f9a-114">**GetScopeAsText 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-114">**GetScopeAsText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopeastext)
-   [<span data-ttu-id="23f9a-115">**GetScopeCount 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-115">**GetScopeCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopecount)
-   [<span data-ttu-id="23f9a-116">**Teamfoundationserverfactory.getserver 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-116">**GetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getserver)
-   [<span data-ttu-id="23f9a-117">**GetText 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-117">**GetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-gettext)
-   [<span data-ttu-id="23f9a-118">**IsLocal 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-118">**IsLocal method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-islocal)
-   [<span data-ttu-id="23f9a-119">**IsRelative 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-119">**IsRelative method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelative)
-   [<span data-ttu-id="23f9a-120">**IsRelativeOrChild 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-120">**IsRelativeOrChild method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelativeorchild)
-   [<span data-ttu-id="23f9a-121">**IsSameClassName 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-121">**IsSameClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-issameclassname)
-   [<span data-ttu-id="23f9a-122">**RemoveAllNamespaces 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-122">**RemoveAllNamespaces method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallnamespaces)
-   [<span data-ttu-id="23f9a-123">**RemoveAllScopes 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-123">**RemoveAllScopes method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallscopes)
-   [<span data-ttu-id="23f9a-124">**RemoveNamespaceAt 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-124">**RemoveNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removenamespaceat)
-   [<span data-ttu-id="23f9a-125">**RemoveScope 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-125">**RemoveScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removescope)
-   [<span data-ttu-id="23f9a-126">**SetClassName 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-126">**SetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setclassname)
-   [<span data-ttu-id="23f9a-127">**SetNamespaceAt 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-127">**SetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setnamespaceat)
-   [<span data-ttu-id="23f9a-128">**SetScope 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-128">**SetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setscope)
-   [<span data-ttu-id="23f9a-129">**SetServer 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-129">**SetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setserver)
-   [<span data-ttu-id="23f9a-130">**SetText 方法**</span><span class="sxs-lookup"><span data-stu-id="23f9a-130">**SetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-settext)

 

 



