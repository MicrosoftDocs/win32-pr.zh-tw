---
description: 裝置可能會產生許多事件，每個事件都可以選擇由許多不同處理常式的其中一個來處理。
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: 如何註冊事件處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973133"
---
# <a name="how-to-register-an-event-handler"></a><span data-ttu-id="c1b18-103">如何註冊事件處理常式</span><span class="sxs-lookup"><span data-stu-id="c1b18-103">How to Register an Event Handler</span></span>

<span data-ttu-id="c1b18-104">裝置可能會產生許多事件，每個事件都可以選擇由許多不同處理常式的其中一個來處理。</span><span class="sxs-lookup"><span data-stu-id="c1b18-104">A device can potentially generate many events, and each event has the option of being handled by one of a number of different handlers.</span></span> <span data-ttu-id="c1b18-105">在 Windows XP 中，會定義下列事件：</span><span class="sxs-lookup"><span data-stu-id="c1b18-105">In Windows XP, the following events are defined:</span></span>

-   <span data-ttu-id="c1b18-106">DeviceArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-106">DeviceArrival</span></span>
-   <span data-ttu-id="c1b18-107">DeviceRemoval</span><span class="sxs-lookup"><span data-stu-id="c1b18-107">DeviceRemoval</span></span>
-   <span data-ttu-id="c1b18-108">MediaArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-108">MediaArrival</span></span>
-   <span data-ttu-id="c1b18-109">MediaRemoval</span><span class="sxs-lookup"><span data-stu-id="c1b18-109">MediaRemoval</span></span>

## <a name="instructions"></a><span data-ttu-id="c1b18-110">指示</span><span class="sxs-lookup"><span data-stu-id="c1b18-110">Instructions</span></span>


<span data-ttu-id="c1b18-111">事件處理常式是在 **EventHandlers** 索引鍵下定義。</span><span class="sxs-lookup"><span data-stu-id="c1b18-111">Event handlers are defined under the **EventHandlers** key.</span></span> <span data-ttu-id="c1b18-112">事件處理常式索引鍵的值是使用者在偵測到事件時，必須從中選擇的每個處理常式的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1b18-112">An event handler key's values are the names of each handler that the user must choose from when the event is detected.</span></span> <span data-ttu-id="c1b18-113">沒有與這些專案相關聯的資料值。</span><span class="sxs-lookup"><span data-stu-id="c1b18-113">There is no data value associated with these entries.</span></span> <span data-ttu-id="c1b18-114">以下是自訂事件處理常式（稱為 **MyNewRemovalEventHandler**）的範例定義，其提供這些處理常式的可能性給使用者：</span><span class="sxs-lookup"><span data-stu-id="c1b18-114">Following is an example definition for a custom event handler called **MyNewRemovalEventHandler**, which presents these handler possibilities to the user:</span></span>

-   <span data-ttu-id="c1b18-115">當名為 Contoso，Inc. 的公司所建立的裝置上偵測到事件時，所要使用的處理常式。</span><span class="sxs-lookup"><span data-stu-id="c1b18-115">A handler to use if the event is detected on a device made by the company named Contoso, Inc.</span></span>
-   <span data-ttu-id="c1b18-116">如果在名稱為 Fabrikam，Inc. 的公司所建立的裝置上偵測到事件，要使用的處理常式。</span><span class="sxs-lookup"><span data-stu-id="c1b18-116">A handler to use if the event is detected on a device made by the company named Fabrikam, Inc.</span></span>
-   <span data-ttu-id="c1b18-117">要在所有其他情況下使用的處理常式。</span><span class="sxs-lookup"><span data-stu-id="c1b18-117">A handler to use in all other cases.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

<span data-ttu-id="c1b18-118">定義事件處理常式之後，它必須針對其中一個事件可能的裝置處理常式註冊： DeviceArrival、DeviceRemoval、MediaArrival 或 MediaRemoval。</span><span class="sxs-lookup"><span data-stu-id="c1b18-118">After an event handler is defined, it must be registered with a device handler for one of the event possibilities: DeviceArrival, DeviceRemoval, MediaArrival, or MediaRemoval.</span></span> <span data-ttu-id="c1b18-119">稍早定義的 MyNewRemovalEventHandler 會用來在名為 MyDeviceHandler 的自訂裝置處理常式下進行 DeviceRemoval，並在下列範例中針對該目的定義。</span><span class="sxs-lookup"><span data-stu-id="c1b18-119">MyNewRemovalEventHandler, defined earlier, is used for DeviceRemoval under a custom device handler named MyDeviceHandler and is defined for that purpose in the following example.</span></span> <span data-ttu-id="c1b18-120">同樣地，登錄值沒有資料元件。</span><span class="sxs-lookup"><span data-stu-id="c1b18-120">Again, the registry value has no data component.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

<span data-ttu-id="c1b18-121">Windows XP 預先定義下列一組 EventHandlers。</span><span class="sxs-lookup"><span data-stu-id="c1b18-121">Windows XP predefines the following set of EventHandlers.</span></span> 

| <span data-ttu-id="c1b18-122">EventHandlers 索引鍵</span><span class="sxs-lookup"><span data-stu-id="c1b18-122">EventHandlers key</span></span>        | <span data-ttu-id="c1b18-123">媒體或檔案類型</span><span class="sxs-lookup"><span data-stu-id="c1b18-123">Media or file type</span></span>                             |
|--------------------------|------------------------------------------------|
| <span data-ttu-id="c1b18-124">HandleCDBurningOnArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-124">HandleCDBurningOnArrival</span></span> | <span data-ttu-id="c1b18-125">空白 CD-R/cd-rw</span><span class="sxs-lookup"><span data-stu-id="c1b18-125">Blank CD-R/CD-RW</span></span>                               |
| <span data-ttu-id="c1b18-126">ShowPicturesOnArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-126">ShowPicturesOnArrival</span></span>    | <span data-ttu-id="c1b18-127">圖片檔案</span><span class="sxs-lookup"><span data-stu-id="c1b18-127">Picture files</span></span>                                  |
| <span data-ttu-id="c1b18-128">PlayMusicFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-128">PlayMusicFilesOnArrival</span></span>  | <span data-ttu-id="c1b18-129">音樂檔案</span><span class="sxs-lookup"><span data-stu-id="c1b18-129">Music files</span></span>                                    |
| <span data-ttu-id="c1b18-130">PlayVideoFilesOnArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-130">PlayVideoFilesOnArrival</span></span>  | <span data-ttu-id="c1b18-131">影片檔案</span><span class="sxs-lookup"><span data-stu-id="c1b18-131">Video files</span></span>                                    |
| <span data-ttu-id="c1b18-132">PlayCDAudioOnArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-132">PlayCDAudioOnArrival</span></span>     | <span data-ttu-id="c1b18-133">音訊 CD (REDBOOK 格式 CD 與音訊曲目) </span><span class="sxs-lookup"><span data-stu-id="c1b18-133">Audio CD (REDBOOK format CD with Audio tracks)</span></span> |
| <span data-ttu-id="c1b18-134">PlayDVDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-134">PlayDVDMovieOnArrival</span></span>    | <span data-ttu-id="c1b18-135">DVD 電影</span><span class="sxs-lookup"><span data-stu-id="c1b18-135">DVD movies</span></span>                                     |



 

<span data-ttu-id="c1b18-136">除了上述的 EventHandlers 以外，Windows Vista 還預先定義了下列一組。</span><span class="sxs-lookup"><span data-stu-id="c1b18-136">Windows Vista predefines the following set of EventHandlers in addition to those above.</span></span> 

| <span data-ttu-id="c1b18-137">EventHandlers 索引鍵</span><span class="sxs-lookup"><span data-stu-id="c1b18-137">EventHandlers key</span></span>              | <span data-ttu-id="c1b18-138">媒體或檔案類型</span><span class="sxs-lookup"><span data-stu-id="c1b18-138">Media or file type</span></span>   |
|--------------------------------|----------------------|
| <span data-ttu-id="c1b18-139">PlaySuperVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-139">PlaySuperVideoCDMovieOnArrival</span></span> | <span data-ttu-id="c1b18-140">超級 VideoCD 電影</span><span class="sxs-lookup"><span data-stu-id="c1b18-140">Super VideoCD movies</span></span> |
| <span data-ttu-id="c1b18-141">PlayVideoCDMovieOnArrival</span><span class="sxs-lookup"><span data-stu-id="c1b18-141">PlayVideoCDMovieOnArrival</span></span>      | <span data-ttu-id="c1b18-142">VideoCD 電影</span><span class="sxs-lookup"><span data-stu-id="c1b18-142">VideoCD movies</span></span>       |



 

 

 



