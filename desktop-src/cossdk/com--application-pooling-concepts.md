---
description: COM + 應用程式共用允許單一執行緒進程進行調整，類似于執行緒共用允許單一執行緒物件的調整方式。
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: COM + 應用程式共用概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847169"
---
# <a name="com-application-pooling-concepts"></a><span data-ttu-id="d280f-103">COM + 應用程式共用概念</span><span class="sxs-lookup"><span data-stu-id="d280f-103">COM+ Application Pooling Concepts</span></span>

<span data-ttu-id="d280f-104">COM + 應用程式共用允許單一執行緒進程進行調整，類似于執行緒共用允許單一執行緒物件的調整方式。</span><span class="sxs-lookup"><span data-stu-id="d280f-104">COM+ application pooling allows single-threaded processes to scale, similar to the way that thread pooling allows single-threaded objects to scale.</span></span> <span data-ttu-id="d280f-105">應用程式共用也可以藉由提供可處理啟用的其他執行中進程，協助從單一進程的失敗中復原。</span><span class="sxs-lookup"><span data-stu-id="d280f-105">Application pooling can also help recover from failures in single processes by providing other running processes able to handle activations.</span></span>

> [!Note]  
> <span data-ttu-id="d280f-106">程式庫應用程式具有其主機進程的回收和共用屬性。</span><span class="sxs-lookup"><span data-stu-id="d280f-106">Library applications have the recycling and pooling properties of their host process.</span></span>

 

<span data-ttu-id="d280f-107">[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)介面的所有方法都支援應用程式共用。</span><span class="sxs-lookup"><span data-stu-id="d280f-107">All methods of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface support application pooling.</span></span>

<span data-ttu-id="d280f-108">使用 [**應用**](applications.md)程式集合中 [**COMAdminCatalogObject**](comadmincatalogobject.md)物件的 ConcurrentApps 屬性，可設定每個應用程式的 com + 應用程式共用。</span><span class="sxs-lookup"><span data-stu-id="d280f-108">COM+ application pooling is configurable per application by using the ConcurrentApps property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="d280f-109">ConcurrentApps 是一個整數值，這個值會指定應用程式的啟動服務時，應該啟動的同時 Dllhost.exe 進程數目上限。</span><span class="sxs-lookup"><span data-stu-id="d280f-109">ConcurrentApps is an integer value that specifies the maximum number of simultaneous Dllhost processes that should be started to service activations for an application.</span></span> <span data-ttu-id="d280f-110">您可以使用 [元件服務] 系統管理工具或以程式設計方式來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d280f-110">This property can be set by using the Component Services administration tool or programmatically.</span></span>

<span data-ttu-id="d280f-111">如果 ConcurrentApps 屬性設定為1（預設值），則會停用 COM + 應用程式共用服務。</span><span class="sxs-lookup"><span data-stu-id="d280f-111">If the ConcurrentApps property is set to 1, which is the default value, the COM+ Application Pooling service is disabled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d280f-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="d280f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d280f-113">COM + 應用程式共用工作</span><span class="sxs-lookup"><span data-stu-id="d280f-113">COM+ Application Pooling Tasks</span></span>](com--application-pooling-tasks.md)
</dt> <dt>

[<span data-ttu-id="d280f-114">COM + 應用程式回收概念</span><span class="sxs-lookup"><span data-stu-id="d280f-114">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



