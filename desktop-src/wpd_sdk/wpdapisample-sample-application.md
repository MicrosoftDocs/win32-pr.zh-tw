---
description: WpdApiSample 應用程式
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: WpdApiSample 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690268"
---
# <a name="wpdapisample-application"></a><span data-ttu-id="6e276-103">WpdApiSample 應用程式</span><span class="sxs-lookup"><span data-stu-id="6e276-103">WpdApiSample Application</span></span>

<span data-ttu-id="6e276-104">WpdApiSample 範例應用程式是一個命令列桌面應用程式，可讓您列舉連線的裝置、探索裝置、查詢屬性和屬性的物件、傳送和取出物件等等。</span><span class="sxs-lookup"><span data-stu-id="6e276-104">The WpdApiSample sample application is a command-line desktop application that enables you to enumerate connected devices, explore devices, query objects for properties and attributes, send and retrieve objects, and so on.</span></span> <span data-ttu-id="6e276-105">在啟動時，應用程式會開啟一個命令視窗，其中會列出您可以執行的工作。</span><span class="sxs-lookup"><span data-stu-id="6e276-105">On startup, the application opens a command window that lists the tasks you can perform.</span></span>

<span data-ttu-id="6e276-106">WpdApiSample 範例應用程式包含下列檔案：</span><span class="sxs-lookup"><span data-stu-id="6e276-106">The WpdApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="6e276-107">**檔案**</span><span class="sxs-lookup"><span data-stu-id="6e276-107">**File**</span></span>               | <span data-ttu-id="6e276-108">**說明**</span><span class="sxs-lookup"><span data-stu-id="6e276-108">**Description**</span></span>                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e276-109">ContentEnumeration .cpp</span><span class="sxs-lookup"><span data-stu-id="6e276-109">ContentEnumeration.cpp</span></span> | <span data-ttu-id="6e276-110">包含列舉裝置上所有物件的函式。</span><span class="sxs-lookup"><span data-stu-id="6e276-110">Contains functions that enumerate all the objects on a device.</span></span>                                                                                                                                            |
| <span data-ttu-id="6e276-111">ContentProperties .cpp</span><span class="sxs-lookup"><span data-stu-id="6e276-111">ContentProperties.cpp</span></span>  | <span data-ttu-id="6e276-112">包含函式，這些函式會讀取和寫入物件屬性，並建立大量屬性集/get 要求。</span><span class="sxs-lookup"><span data-stu-id="6e276-112">Contains functions that read and write object properties and make bulk property set/get requests.</span></span>                                                                                                         |
| <span data-ttu-id="6e276-113">ContentTransfer .cpp</span><span class="sxs-lookup"><span data-stu-id="6e276-113">ContentTransfer.cpp</span></span>    | <span data-ttu-id="6e276-114">包含在裝置上傳送內容、讀取物件類型需求，以及在裝置上建立資料夾的函式。</span><span class="sxs-lookup"><span data-stu-id="6e276-114">Contains functions that transfer content to or from the device, read object type requirements, and create a folder on the device.</span></span>                                                                         |
| <span data-ttu-id="6e276-115">DeviceCapabilities .cpp</span><span class="sxs-lookup"><span data-stu-id="6e276-115">DeviceCapabilities.cpp</span></span> | <span data-ttu-id="6e276-116">包含函式，用來列出裝置上的功能物件類型、列出每個功能物件類型所支援的內容類型，以及顯示呈現物件設定檔。</span><span class="sxs-lookup"><span data-stu-id="6e276-116">Contains functions to list the functional object types on the device, list the content types supported by each functional object type, and display rendering object profiles.</span></span>                             |
| <span data-ttu-id="6e276-117">DeviceEnumeration .cpp</span><span class="sxs-lookup"><span data-stu-id="6e276-117">DeviceEnumeration.cpp</span></span>  | <span data-ttu-id="6e276-118">列出所有已連線裝置的易記名稱、製造商和描述。</span><span class="sxs-lookup"><span data-stu-id="6e276-118">Lists the friendly names, manufacturers, and descriptions of all connected devices.</span></span>                                                                                                                       |
| <span data-ttu-id="6e276-119">DeviceEvents .cpp</span><span class="sxs-lookup"><span data-stu-id="6e276-119">DeviceEvents.cpp</span></span>       | <span data-ttu-id="6e276-120">包含會在每次引發事件時記錄裝置事件及其參數的函式。</span><span class="sxs-lookup"><span data-stu-id="6e276-120">Contains functions that log device events and their parameters whenever events are fired.</span></span>                                                                                                                 |
| <span data-ttu-id="6e276-121">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="6e276-121">Stdafx.cpp</span></span>             | <span data-ttu-id="6e276-122">包含標準檔案。</span><span class="sxs-lookup"><span data-stu-id="6e276-122">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="6e276-123">WpdApiSample .cpp</span><span class="sxs-lookup"><span data-stu-id="6e276-123">WpdApiSample.cpp</span></span>       | <span data-ttu-id="6e276-124">裝載 **\_ tmain** 啟動函式，此函式會呼叫本機 **DoMenu** 函式，此函式會顯示可用裝置和工作的清單，並呼叫適用于使用者功能表選取的函式。</span><span class="sxs-lookup"><span data-stu-id="6e276-124">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6e276-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e276-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e276-126">範例</span><span class="sxs-lookup"><span data-stu-id="6e276-126">Sample</span></span>](sample.md)
</dt> </dl>

 

 



