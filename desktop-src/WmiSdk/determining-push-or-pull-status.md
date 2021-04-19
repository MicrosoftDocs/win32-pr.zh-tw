---
description: 您可以將類別提供者模型為 push 或 pull 提供者，以指定提供者如何預期與 WMI 互動。
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: 判斷推送或提取狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986860"
---
# <a name="determining-push-or-pull-status"></a><span data-ttu-id="f7117-103">判斷推送或提取狀態</span><span class="sxs-lookup"><span data-stu-id="f7117-103">Determining Push or Pull Status</span></span>

<span data-ttu-id="f7117-104">您可以將類別提供者模型為 push 或 pull 提供者，以指定提供者如何預期與 WMI 互動。</span><span class="sxs-lookup"><span data-stu-id="f7117-104">You can model a class provider as a push or pull provider, which specifies how a provider expects to interact with WMI.</span></span> <span data-ttu-id="f7117-105">提取提供者會收到來自 WMI 的要求，並透過動態產生資料或從本機快取抓取來滿足要求。</span><span class="sxs-lookup"><span data-stu-id="f7117-105">Pull providers receive a request from WMI and satisfy the request either by generating the data dynamically or retrieving it from a local cache.</span></span> <span data-ttu-id="f7117-106">提取提供者也必須執行大量的介面。</span><span class="sxs-lookup"><span data-stu-id="f7117-106">Pull providers also must implement a large number of interfaces.</span></span>

<span data-ttu-id="f7117-107">提取提供者會動態產生類別定義。</span><span class="sxs-lookup"><span data-stu-id="f7117-107">A pull provider generates class definitions dynamically.</span></span> <span data-ttu-id="f7117-108">通常，提取提供者所管理的資料會經常變更，要求提供者必須動態產生類別，或在應用程式發出要求時，從本機快取取出類別。</span><span class="sxs-lookup"><span data-stu-id="f7117-108">Typically, the data managed by a pull provider changes frequently, requiring the provider to either generate the class dynamically or retrieve the class from a local cache whenever an application issues a request.</span></span> <span data-ttu-id="f7117-109">提取提供者必須執行自己的資料抓取、快取和事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="f7117-109">A pull provider must implement its own data retrieval, cache, and event notification mechanisms.</span></span> <span data-ttu-id="f7117-110">因為大部分的提供者都是提取提供者，所以此檔案中的檔會假設您要建立提取提供者，除非另行明確陳述。</span><span class="sxs-lookup"><span data-stu-id="f7117-110">Because most providers are pull providers, the documentation in this file assumes you are building a pull provider unless explicitly stated otherwise.</span></span>

<span data-ttu-id="f7117-111">相反地，WMI 會使用 WMI 儲存機制中的資料來處理推播提供者的所有應用程式要求。</span><span class="sxs-lookup"><span data-stu-id="f7117-111">In contrast, WMI uses data in the WMI repository to handle all application requests for push providers.</span></span> <span data-ttu-id="f7117-112">推播提供者也會使用較少的介面方法，因此更容易執行。</span><span class="sxs-lookup"><span data-stu-id="f7117-112">Push providers also use fewer interface methods, and thus are easier to implement.</span></span> <span data-ttu-id="f7117-113">推入提供者會使用 WMI 存放庫做為受管理物件資訊的儲存區域，而且只會在初始化期間更新該資訊。</span><span class="sxs-lookup"><span data-stu-id="f7117-113">A push provider uses the WMI repository as a storage area for information on the managed object, and updates that information only during initialization.</span></span> <span data-ttu-id="f7117-114">例如，Microsoft Windows 軟體開發套件 (SDK) 的 WMI 區段中所包含的 WDM 類別提供者，會模型化為推播提供者。</span><span class="sxs-lookup"><span data-stu-id="f7117-114">For example, the WDM class provider included in the WMI section of the Microsoft Windows Software Development Kit (SDK) is modeled as a push provider.</span></span>

<span data-ttu-id="f7117-115">藉由使用 WMI 儲存機制作為存放區域，推播提供者可以透過提取提供者獲得下列優點：</span><span class="sxs-lookup"><span data-stu-id="f7117-115">By using the WMI repository as a storage area, a push provider gains the following benefits over a pull provider:</span></span>

-   <span data-ttu-id="f7117-116">提供者不需要執行本機快取來儲存資料。</span><span class="sxs-lookup"><span data-stu-id="f7117-116">The provider does not need to implement a local cache to store data.</span></span>
-   <span data-ttu-id="f7117-117">提供者不需要支援資料抓取;相反地，提供者可以依賴 WMI 提供抓取支援。</span><span class="sxs-lookup"><span data-stu-id="f7117-117">The provider does not need to support data retrieval; instead, the provider can rely on WMI to provide retrieval support.</span></span>
-   <span data-ttu-id="f7117-118">當應用程式要求提供者提供的資料時，WMI 會滿足該要求。</span><span class="sxs-lookup"><span data-stu-id="f7117-118">When an application requests data supplied by the provider, WMI fulfills that request.</span></span>
-   <span data-ttu-id="f7117-119">提供者也可以依賴 WMI 來支援事件通知。</span><span class="sxs-lookup"><span data-stu-id="f7117-119">The provider can also rely on WMI to support event notification.</span></span>

<span data-ttu-id="f7117-120">不過，因為推播提供者只會在初始化期間更新，所以對類別所做的任何變更可能會有一段時間不會反映在 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="f7117-120">However, because a push provider updates only during initialization, any changes to a class may not be reflected in the WMI repository for some time.</span></span> <span data-ttu-id="f7117-121">因此，推播提供者模型最適合用於幾乎不會變更或完全靜態的類別。</span><span class="sxs-lookup"><span data-stu-id="f7117-121">Therefore, the push provider model works best with classes that change little or else are completely static.</span></span>

 

 



