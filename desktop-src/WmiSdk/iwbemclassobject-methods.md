---
description: IWbemClassObject 介面會公開下列方法。
ms.assetid: 20BF7775-89D9-4851-8561-EEBA398A0584
ms.tgt_platform: multiple
title: IWbemClassObject 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825b3f15f17dca6dd0871bbcae3f531a90c90f1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321011"
---
# <a name="iwbemclassobject-methods"></a><span data-ttu-id="6b416-103">IWbemClassObject 方法</span><span class="sxs-lookup"><span data-stu-id="6b416-103">IWbemClassObject Methods</span></span>

<span data-ttu-id="6b416-104">[**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="6b416-104">The [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b416-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="6b416-105">In this section</span></span>

-   [<span data-ttu-id="6b416-106">**BeginEnumeration 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-106">**BeginEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration)
-   [<span data-ttu-id="6b416-107">**BeginMethodEnumeration 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-107">**BeginMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginmethodenumeration)
-   [<span data-ttu-id="6b416-108">**Clone 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-108">**Clone method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone)
-   [<span data-ttu-id="6b416-109">**CompareTo 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-109">**CompareTo method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-compareto)
-   [<span data-ttu-id="6b416-110">**Delete 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-110">**Delete method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)
-   [<span data-ttu-id="6b416-111">**DeleteMethod 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-111">**DeleteMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-deletemethod)
-   [<span data-ttu-id="6b416-112">**EndEnumeration 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-112">**EndEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration)
-   [<span data-ttu-id="6b416-113">**EndMethodEnumeration 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-113">**EndMethodEnumeration method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endmethodenumeration)
-   [<span data-ttu-id="6b416-114">**Get 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-114">**Get method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)
-   [<span data-ttu-id="6b416-115">**GetMethod 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-115">**GetMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)
-   [<span data-ttu-id="6b416-116">**GetMethodOrigin 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-116">**GetMethodOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodorigin)
-   [<span data-ttu-id="6b416-117">**GetMethodQualifierSet 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-117">**GetMethodQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)
-   [<span data-ttu-id="6b416-118">**GetNames 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-118">**GetNames method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getnames)
-   [<span data-ttu-id="6b416-119">**GetObjectText 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-119">**GetObjectText method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext)
-   [<span data-ttu-id="6b416-120">**GetPropertyOrigin 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-120">**GetPropertyOrigin method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyorigin)
-   [<span data-ttu-id="6b416-121">**GetPropertyQualifierSet 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-121">**GetPropertyQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset)
-   [<span data-ttu-id="6b416-122">**GetQualifierSet 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-122">**GetQualifierSet method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset)
-   [<span data-ttu-id="6b416-123">**InheritsFrom 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-123">**InheritsFrom method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-inheritsfrom)
-   [<span data-ttu-id="6b416-124">**Next 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-124">**Next method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-next)
-   [<span data-ttu-id="6b416-125">**NextMethod 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-125">**NextMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-nextmethod)
-   [<span data-ttu-id="6b416-126">**Put 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-126">**Put method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
-   [<span data-ttu-id="6b416-127">**PutMethod 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-127">**PutMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)
-   [<span data-ttu-id="6b416-128">**SpawnDerivedClass 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-128">**SpawnDerivedClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass)
-   [<span data-ttu-id="6b416-129">**SpawnInstance 方法**</span><span class="sxs-lookup"><span data-stu-id="6b416-129">**SpawnInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)

 

 



