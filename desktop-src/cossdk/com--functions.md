---
description: 以下是 COM + 函式。
ms.assetid: fdeb70ff-17ae-4ee4-a8b1-7fffb65ba2b2
title: COM + 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f7ce33e729a12c37ff1f2dcef516ab13d9b69a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106976647"
---
# <a name="com-functions"></a><span data-ttu-id="967e9-103">COM + 函式</span><span class="sxs-lookup"><span data-stu-id="967e9-103">COM+ Functions</span></span>

<span data-ttu-id="967e9-104">以下是 COM + 函式。</span><span class="sxs-lookup"><span data-stu-id="967e9-104">The following are the COM+ functions.</span></span>



| <span data-ttu-id="967e9-105">函式</span><span class="sxs-lookup"><span data-stu-id="967e9-105">Function</span></span>                                                                 | <span data-ttu-id="967e9-106">描述</span><span class="sxs-lookup"><span data-stu-id="967e9-106">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="967e9-107">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="967e9-107">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)                             | <span data-ttu-id="967e9-108">建立活動來執行可以使用 COM+ 服務的同步或非同步 (Asynchronous) 批次工作，而不需建立 COM+ 元件。</span><span class="sxs-lookup"><span data-stu-id="967e9-108">Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.</span></span> |
| [<span data-ttu-id="967e9-109">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="967e9-109">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     | <span data-ttu-id="967e9-110">用來輸入可接著使用 COM + 服務的程式碼。</span><span class="sxs-lookup"><span data-stu-id="967e9-110">Used to enter code that can then use COM+ services.</span></span>                                                                                     |
| [<span data-ttu-id="967e9-111">**CoGetDefaultCoNtext**</span><span class="sxs-lookup"><span data-stu-id="967e9-111">**CoGetDefaultContext**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetdefaultcontext)                       | <span data-ttu-id="967e9-112">抓取指定之單元的預設內容參考。</span><span class="sxs-lookup"><span data-stu-id="967e9-112">Retrieves a reference to the default context of the specified apartment.</span></span>                                                                |
| [<span data-ttu-id="967e9-113">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="967e9-113">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)                     | <span data-ttu-id="967e9-114">用來離開使用 COM + 服務的程式碼。</span><span class="sxs-lookup"><span data-stu-id="967e9-114">Used to leave code that uses COM+ services.</span></span>                                                                                             |
| <span data-ttu-id="967e9-115">**ComPlusCompleteCbbSetup**</span><span class="sxs-lookup"><span data-stu-id="967e9-115">**ComPlusCompleteCbbSetup**</span></span>               | <span data-ttu-id="967e9-116">完成目的地電腦上的目錄遷移。</span><span class="sxs-lookup"><span data-stu-id="967e9-116">Completes a catalog migration on the destination computer.</span></span>                                                                              |
| <span data-ttu-id="967e9-117">**GetComPlusPackageInstallStatus**</span><span class="sxs-lookup"><span data-stu-id="967e9-117">**GetComPlusPackageInstallStatus**</span></span> | <span data-ttu-id="967e9-118">指出是否已安裝64位的 Common Language Runtime (CLR) 。</span><span class="sxs-lookup"><span data-stu-id="967e9-118">Indicates whether the 64-bit Common Language Runtime (CLR) is installed.</span></span>                                                                |
| [<span data-ttu-id="967e9-119">**GetDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="967e9-119">**GetDispenserManager**</span></span>](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager)                       | <span data-ttu-id="967e9-120">抓取分配器管理員的 [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="967e9-120">Retrieves the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>                                             |
| [<span data-ttu-id="967e9-121">**GetManagedExtensions**</span><span class="sxs-lookup"><span data-stu-id="967e9-121">**GetManagedExtensions**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getmanagedextensions)                     | <span data-ttu-id="967e9-122">判斷已安裝的 COM + 版本是否支援提供特殊功能來管理 (受控物件) 的服務元件。</span><span class="sxs-lookup"><span data-stu-id="967e9-122">Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).</span></span>    |
| [<span data-ttu-id="967e9-123">**GetObjectCoNtext**</span><span class="sxs-lookup"><span data-stu-id="967e9-123">**GetObjectContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)                             | <span data-ttu-id="967e9-124">捕獲與目前 COM + 物件相關聯之內容的參考。</span><span class="sxs-lookup"><span data-stu-id="967e9-124">Retrieves a reference to the context that is associated with the current COM+ object.</span></span>                                                   |
| [<span data-ttu-id="967e9-125">**MTSCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="967e9-125">**MTSCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-mtscreateactivity)                           | <span data-ttu-id="967e9-126">在單一執行緒的單元中建立活動，以執行同步或非同步批次工作。</span><span class="sxs-lookup"><span data-stu-id="967e9-126">Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.</span></span>                                        |
| [<span data-ttu-id="967e9-127">**RecycleSurrogate**</span><span class="sxs-lookup"><span data-stu-id="967e9-127">**RecycleSurrogate**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)                             | <span data-ttu-id="967e9-128">回收呼叫進程。</span><span class="sxs-lookup"><span data-stu-id="967e9-128">Recycles the calling process.</span></span>                                                                                                           |
| [<span data-ttu-id="967e9-129">**SafeRef**</span><span class="sxs-lookup"><span data-stu-id="967e9-129">**SafeRef**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)                                               | <span data-ttu-id="967e9-130">目前請勿使用。</span><span class="sxs-lookup"><span data-stu-id="967e9-130">Obsolete; do not use.</span></span>                                                                                                                   |



 

 

 



