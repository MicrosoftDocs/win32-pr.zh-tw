---
title: 關於映射主控 API
description: 本檔著重于 IMAPI.EXE for Microsoft (IMAPIv1) 的 Adaptec 實作為的說明。
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- 映射主控 API IMAPI.EXE，描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db1dc7846d2e47483abf2ca8856d593b874467f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104553277"
---
# <a name="about-the-image-mastering-api"></a><span data-ttu-id="907b7-104">關於映射主控 API</span><span class="sxs-lookup"><span data-stu-id="907b7-104">About the Image Mastering API</span></span>

<span data-ttu-id="907b7-105">本檔著重于 IMAPI.EXE for Microsoft (IMAPIv1) 的 Adaptec 實作為的說明。</span><span class="sxs-lookup"><span data-stu-id="907b7-105">This documentation focuses on a description of the Adaptec implementation of IMAPI for Microsoft (IMAPIv1).</span></span> <span data-ttu-id="907b7-106">因此，本檔包含四個主要 COM 物件及其介面的描述。</span><span class="sxs-lookup"><span data-stu-id="907b7-106">As such, descriptions of the four main COM objects and their interfaces are included in this document.</span></span> <span data-ttu-id="907b7-107">四個主要物件如下： **MSDiscMasterObj**、 **MSDiscRecorderObj**、 **MSDiscStashObj** 和 **MSBurnEngineObj**。</span><span class="sxs-lookup"><span data-stu-id="907b7-107">The four main objects are as follows: **MSDiscMasterObj**, **MSDiscRecorderObj**, **MSDiscStashObj**, and **MSBurnEngineObj**.</span></span>

<span data-ttu-id="907b7-108">系統上可能會有多個 **MSDiscMasterObj** 物件具現化，但是一次只能有一個應用程式可存取錄製器。</span><span class="sxs-lookup"><span data-stu-id="907b7-108">There can be multiple **MSDiscMasterObj** objects instantiated on a system, but only one application can access a recorder at a time.</span></span> <span data-ttu-id="907b7-109">**MSDiscMasterObj** 會實作為多個介面，如下列物件圖所示。</span><span class="sxs-lookup"><span data-stu-id="907b7-109">The **MSDiscMasterObj** implements multiple interfaces, as shown in the following object diagram.</span></span>

![msdiscmasterobj 會實作為多個介面](images/imapi.png)

<span data-ttu-id="907b7-111">應用程式會使用 [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) 介面來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="907b7-111">Applications use the [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) interface to perform the following tasks:</span></span>

-   <span data-ttu-id="907b7-112">開啟 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="907b7-112">Open IMAPI</span></span>
-   <span data-ttu-id="907b7-113">列舉支援的格式 (Joliet 和 Redbook) </span><span class="sxs-lookup"><span data-stu-id="907b7-113">Enumerate supported formats (Joliet and Redbook)</span></span>
-   <span data-ttu-id="907b7-114">選取格式</span><span class="sxs-lookup"><span data-stu-id="907b7-114">Select a format</span></span>
-   <span data-ttu-id="907b7-115">取得記錄器清單</span><span class="sxs-lookup"><span data-stu-id="907b7-115">Get a list of recorders</span></span>
-   <span data-ttu-id="907b7-116">選取錄製器</span><span class="sxs-lookup"><span data-stu-id="907b7-116">Select a recorder</span></span>
-   <span data-ttu-id="907b7-117">開始燒錄</span><span class="sxs-lookup"><span data-stu-id="907b7-117">Start a burn</span></span>

<span data-ttu-id="907b7-118">選取格式時， [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) 和 [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) 介面會透過 [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) 介面傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="907b7-118">The [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) and [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) interfaces are returned to an application through the [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) interface when a format is selected.</span></span> <span data-ttu-id="907b7-119">這些介面會分別控制資料或音訊光碟的內容。</span><span class="sxs-lookup"><span data-stu-id="907b7-119">These interfaces control the content of a data or audio disc, respectively.</span></span> <span data-ttu-id="907b7-120">每個應用程式都不應該瞭解特定的格式介面。</span><span class="sxs-lookup"><span data-stu-id="907b7-120">It is not expected that every application understand the specific format interfaces.</span></span> <span data-ttu-id="907b7-121">應用程式可以存取 **IJolietDiscMaster** 介面的一般屬性，例如磁片區名稱或舊版檔案名。</span><span class="sxs-lookup"><span data-stu-id="907b7-121">Applications can access generic properties of the **IJolietDiscMaster** interface, such as volume name or legacy file name.</span></span>

<span data-ttu-id="907b7-122">**MSDiscRecorderObj** 物件是透過 [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) 介面進行存取。</span><span class="sxs-lookup"><span data-stu-id="907b7-122">**MSDiscRecorderObj** objects are accessed through the [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) interface.</span></span> <span data-ttu-id="907b7-123">每個與 IMAPI.EXE 相容的 CD-R 或 CD-RW 裝置都有對應的 **MSDiscRecorderObj** 物件。</span><span class="sxs-lookup"><span data-stu-id="907b7-123">Every CD-R or CD-RW device that is compatible with IMAPI has a corresponding **MSDiscRecorderObj** object.</span></span> <span data-ttu-id="907b7-124">應用程式會使用這些物件上 **IDiscRecorder** 介面的指標，來選取 imapi.exe 要用來錄製 CD 的裝置。</span><span class="sxs-lookup"><span data-stu-id="907b7-124">An application uses pointers to the **IDiscRecorder** interface on those objects to select which device will be used by IMAPI to record a CD.</span></span> <span data-ttu-id="907b7-125">此外，應用程式也可以透過 **IDiscRecorder** 存取錄製器的一般屬性。</span><span class="sxs-lookup"><span data-stu-id="907b7-125">In addition, applications can access generic properties of a recorder through **IDiscRecorder**.</span></span> <span data-ttu-id="907b7-126">這包括做為寫入器速度或其他燒錄參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="907b7-126">This includes such properties as writer speed or other burn parameters.</span></span>

<span data-ttu-id="907b7-127">其餘的物件（ **MSDiscStashObj** 和 **MSBURNENGINEOBJ**）是 imapi.exe 所存取的內建物件。</span><span class="sxs-lookup"><span data-stu-id="907b7-127">The remaining objects, **MSDiscStashObj** and **MSBurnEngineObj**, are internal objects accessed by IMAPI.</span></span> <span data-ttu-id="907b7-128">此處提及的只是用來闡明 IMAPI.EXE 架構。</span><span class="sxs-lookup"><span data-stu-id="907b7-128">They are mentioned here only to clarify the IMAPI architecture.</span></span> <span data-ttu-id="907b7-129">**MSDiscStashObj** 透過 **IDiscStash** 介面表示 (，) **MSDiscMasterObj** 用來建立要燒錄之音訊影像或資料光碟的大小（大小上限為 800 MB）。</span><span class="sxs-lookup"><span data-stu-id="907b7-129">The **MSDiscStashObj** represents (through the **IDiscStash** interface) a raw file up to 800 MB in size that is used by **MSDiscMasterObj** to create audio images or data discs to be burned.</span></span> <span data-ttu-id="907b7-130">當從較低層級的引擎要求燒錄時，會透過 **IMSBurnEngine** 介面將隱藏專案傳遞至 **MSBurnEngineObj** () 。</span><span class="sxs-lookup"><span data-stu-id="907b7-130">The stash is passed to the **MSBurnEngineObj** (through the **IMSBurnEngine** interface) when a burn is requested from the lower-level engine.</span></span> <span data-ttu-id="907b7-131">**MSBurnEngineObj** 物件預期隱藏內容的格式必須是已知的格式。</span><span class="sxs-lookup"><span data-stu-id="907b7-131">The **MSBurnEngineObj** object expects the contents of the stash to be in a known format.</span></span> <span data-ttu-id="907b7-132">在這方面， **MSDiscMasterObj** 和 **MSBurnEngineObj** 有關于隱藏專案內容的合約。</span><span class="sxs-lookup"><span data-stu-id="907b7-132">In this respect, **MSDiscMasterObj** and **MSBurnEngineObj** have a contract regarding the contents of the stash.</span></span>

 

 




