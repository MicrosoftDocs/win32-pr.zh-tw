---
description: IWbemServices 介面會公開下列方法。
ms.assetid: B4A2048E-6C2F-43E0-97BD-E6D37D8E4657
ms.tgt_platform: multiple
title: IWbemServices 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a960ec223d16bd9258ba2d9d56518d88beab50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969395"
---
# <a name="iwbemservices-methods"></a><span data-ttu-id="499ad-103">IWbemServices 方法</span><span class="sxs-lookup"><span data-stu-id="499ad-103">IWbemServices Methods</span></span>

<span data-ttu-id="499ad-104">[**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="499ad-104">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="499ad-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="499ad-105">In this section</span></span>

-   [<span data-ttu-id="499ad-106">**CancelAsyncCall 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-106">**CancelAsyncCall method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)
-   [<span data-ttu-id="499ad-107">**CreateClassEnum 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-107">**CreateClassEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)
-   [<span data-ttu-id="499ad-108">**CreateClassEnumAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-108">**CreateClassEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="499ad-109">**CreateInstanceEnum 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-109">**CreateInstanceEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)
-   [<span data-ttu-id="499ad-110">**CreateInstanceEnumAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-110">**CreateInstanceEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="499ad-111">**DeleteClass 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-111">**DeleteClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass)
-   [<span data-ttu-id="499ad-112">**DeleteClassAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-112">**DeleteClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)
-   [<span data-ttu-id="499ad-113">**DeleteInstance 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-113">**DeleteInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance)
-   [<span data-ttu-id="499ad-114">**DeleteInstanceAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-114">**DeleteInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="499ad-115">**ExecMethod 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-115">**ExecMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
-   [<span data-ttu-id="499ad-116">**ExecMethodAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-116">**ExecMethodAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="499ad-117">**ExecNotificationQuery 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-117">**ExecNotificationQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
-   [<span data-ttu-id="499ad-118">**ExecNotificationQueryAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-118">**ExecNotificationQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="499ad-119">**ExecQuery 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-119">**ExecQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   [<span data-ttu-id="499ad-120">**ExecQueryAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-120">**ExecQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="499ad-121">**GetObject 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-121">**GetObject method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)
-   [<span data-ttu-id="499ad-122">**GetObjectAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-122">**GetObjectAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="499ad-123">**OpenNamespace 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-123">**OpenNamespace method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace)
-   [<span data-ttu-id="499ad-124">**PutClass 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-124">**PutClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
-   [<span data-ttu-id="499ad-125">**PutClassAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-125">**PutClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)
-   [<span data-ttu-id="499ad-126">**PutInstance 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-126">**PutInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)
-   [<span data-ttu-id="499ad-127">**PutInstanceAsync 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-127">**PutInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)
-   [<span data-ttu-id="499ad-128">**QueryObjectSink 方法**</span><span class="sxs-lookup"><span data-stu-id="499ad-128">**QueryObjectSink method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-queryobjectsink)

 

 



