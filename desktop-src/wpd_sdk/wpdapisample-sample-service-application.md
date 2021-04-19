---
description: WpdServicesApiSample 應用程式
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: WpdServicesApiSample 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987549"
---
# <a name="wpdservicesapisample-application"></a><span data-ttu-id="c6870-103">WpdServicesApiSample 應用程式</span><span class="sxs-lookup"><span data-stu-id="c6870-103">WpdServicesApiSample Application</span></span>

<span data-ttu-id="c6870-104">裝置服務是功能物件的擴充功能：除了以邏輯方式分組裝置功能之外，裝置服務也提供應用程式以程式設計方式探索這些功能的能力。</span><span class="sxs-lookup"><span data-stu-id="c6870-104">A device service is an extension of a functional object: In addition to logically grouping device capabilities, a device service provides applications with the ability to programmatically discover those capabilities.</span></span>

<span data-ttu-id="c6870-105">WpdServicesApiSample 範例應用程式是一個命令列桌面應用程式，可讓您在連接到電腦的裝置上探索連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="c6870-105">The WpdServicesApiSample sample application is a command-line desktop application that you can use to explore Contacts services on devices attached to your computer.</span></span> <span data-ttu-id="c6870-106">您可以藉由列出支援的方式來探索這些服務：格式、事件、方法和抽象服務。</span><span class="sxs-lookup"><span data-stu-id="c6870-106">You can explore these services by listing supported: formats, events, methods, and abstract services.</span></span> <span data-ttu-id="c6870-107">您也可以使用此應用程式抓取指定連絡人服務上的屬性，並叫用該服務所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="c6870-107">You can also use this application retrieve the properties on a given Contact service and to invoke methods supported by that service.</span></span>

<span data-ttu-id="c6870-108">如果您還沒有支援「連絡人」服務的裝置，您仍然可以在第一次安裝 Windows 驅動程式套件中包含的 WpdServiceSampleDriver 時執行 WpdServicesApiSample。</span><span class="sxs-lookup"><span data-stu-id="c6870-108">If you don't yet have a device that supports Contacts services, you can still run the WpdServicesApiSample if you first install the WpdServiceSampleDriver that is included in the Windows Driver Kit.</span></span>

<span data-ttu-id="c6870-109">WpdServicesApiSample 範例應用程式包含下列檔案：</span><span class="sxs-lookup"><span data-stu-id="c6870-109">The WpdServicesApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="c6870-110">**檔案**</span><span class="sxs-lookup"><span data-stu-id="c6870-110">**File**</span></span>                | <span data-ttu-id="c6870-111">**說明**</span><span class="sxs-lookup"><span data-stu-id="c6870-111">**Description**</span></span>                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6870-112">ContentEnumeration .cpp</span><span class="sxs-lookup"><span data-stu-id="c6870-112">ContentEnumeration.cpp</span></span>  | <span data-ttu-id="c6870-113">包含列舉指定連絡人服務上之內容的方法。</span><span class="sxs-lookup"><span data-stu-id="c6870-113">Contains methods that enumerate the content on a given Contacts service.</span></span>                                                                                                                                  |
| <span data-ttu-id="c6870-114">ContentProperties .cpp</span><span class="sxs-lookup"><span data-stu-id="c6870-114">ContentProperties.cpp</span></span>   | <span data-ttu-id="c6870-115">包含在指定的連絡人服務上讀取和寫入屬性的方法。</span><span class="sxs-lookup"><span data-stu-id="c6870-115">Contains methods that read and write properties on a given Contacts service.</span></span>                                                                                                                              |
| <span data-ttu-id="c6870-116">ServiceCapabilities .cpp</span><span class="sxs-lookup"><span data-stu-id="c6870-116">ServiceCapabilities.cpp</span></span> | <span data-ttu-id="c6870-117">包含方法，這些方法會取得所指定連絡人服務所支援的支援格式、事件和抽象服務。</span><span class="sxs-lookup"><span data-stu-id="c6870-117">Contains the methods that retrieve the supported formats, events, and abstract services that are supported by a given Contacts service.</span></span>                                                                   |
| <span data-ttu-id="c6870-118">ServiceEnumeration .cpp</span><span class="sxs-lookup"><span data-stu-id="c6870-118">ServiceEnumeration.cpp</span></span>  | <span data-ttu-id="c6870-119">包含可抓取裝置資訊的 helper 函式，例如裝置易記名稱或支援的連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="c6870-119">Contains the helper functions that retrieve device information such as the device-friendly name or the supported Contacts services.</span></span>                                                                       |
| <span data-ttu-id="c6870-120">ServiceMethods .cpp</span><span class="sxs-lookup"><span data-stu-id="c6870-120">ServiceMethods.cpp</span></span>      | <span data-ttu-id="c6870-121">包含方法，這些方法會取出並叫用指定連絡人服務所支援的方法。</span><span class="sxs-lookup"><span data-stu-id="c6870-121">Contains the methods that retrieve and invoke methods supported by a given Contacts service.</span></span>                                                                                                              |
| <span data-ttu-id="c6870-122">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="c6870-122">Stdafx.cpp</span></span>              | <span data-ttu-id="c6870-123">包含標準檔案。</span><span class="sxs-lookup"><span data-stu-id="c6870-123">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="c6870-124">WpdServiceApiSample .cpp</span><span class="sxs-lookup"><span data-stu-id="c6870-124">WpdServiceApiSample.cpp</span></span> | <span data-ttu-id="c6870-125">裝載 **\_ tmain** 啟動函式，此函式會呼叫本機 **DoMenu** 函式，此函式會顯示可用裝置和工作的清單，並呼叫適用于使用者功能表選取的函式。</span><span class="sxs-lookup"><span data-stu-id="c6870-125">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 


## <a name="related-topics"></a><span data-ttu-id="c6870-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6870-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6870-127">範例</span><span class="sxs-lookup"><span data-stu-id="c6870-127">Samples</span></span>](sample.md)
</dt> </dl>

 

 



