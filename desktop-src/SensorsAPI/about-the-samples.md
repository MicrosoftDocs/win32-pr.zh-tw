---
description: Windows SDK 包含實用的程式碼範例和工具，可協助您瞭解及使用 Windows 感應器和位置平台，以及相關的 Api。
ms.assetid: e31174f6-1c2b-4d97-b6b6-e54825ff47f5
title: 關於範例和工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126ec5e07829cfd17c2b07313bb104140c6fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851503"
---
# <a name="about-the-samples-and-tools"></a><span data-ttu-id="72eaf-103">關於範例和工具</span><span class="sxs-lookup"><span data-stu-id="72eaf-103">About the Samples and Tools</span></span>

<span data-ttu-id="72eaf-104">Windows SDK 包含實用的程式碼範例和工具，可協助您瞭解及使用 Windows 感應器和位置平台，以及相關的 Api。</span><span class="sxs-lookup"><span data-stu-id="72eaf-104">The Windows SDK includes useful code samples and tools to help you understand and use the Windows Sensor and Location platform and related APIs.</span></span>

## <a name="samples"></a><span data-ttu-id="72eaf-105">範例</span><span class="sxs-lookup"><span data-stu-id="72eaf-105">Samples</span></span>

<span data-ttu-id="72eaf-106">Windows SDK 包含下列感應器 API 範例。</span><span class="sxs-lookup"><span data-stu-id="72eaf-106">The Windows SDK includes the following Sensor API samples.</span></span> <span data-ttu-id="72eaf-107">您可以在名為 samples winui 感應器的資料夾中 \\ \\ ，找到 \\ 您安裝 WINDOWS SDK 的感應器 API 範例。</span><span class="sxs-lookup"><span data-stu-id="72eaf-107">You can find the Sensor API samples in the folder named \\Samples\\winui\\Sensors, where you installed the Windows SDK.</span></span> <span data-ttu-id="72eaf-108">例如，如果您將 Windows SDK 安裝在 C 磁片磁碟機上，您會在下列資料夾中找到範例： C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ winui \\ 感應器。</span><span class="sxs-lookup"><span data-stu-id="72eaf-108">For example, if you installed the Windows SDK on drive C, you would find the samples in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\winui\\Sensors.</span></span>



| <span data-ttu-id="72eaf-109">範例名稱</span><span class="sxs-lookup"><span data-stu-id="72eaf-109">Sample name</span></span>       | <span data-ttu-id="72eaf-110">描述</span><span class="sxs-lookup"><span data-stu-id="72eaf-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72eaf-111">AmbientLightAware</span><span class="sxs-lookup"><span data-stu-id="72eaf-111">AmbientLightAware</span></span> | <span data-ttu-id="72eaf-112">此 MFC 範例示範如何使用感應器 API，方法是從電腦上的環境光線感應器讀取資料，並根據光源條件來變更文字大小。</span><span class="sxs-lookup"><span data-stu-id="72eaf-112">This MFC sample shows how to use the Sensor API by reading data from ambient light sensors on the computer and changing text size according to the lighting conditions.</span></span> <span data-ttu-id="72eaf-113">您可以看到顯示如何管理事件，以及如何要求使用者權限的程式碼。</span><span class="sxs-lookup"><span data-stu-id="72eaf-113">You can see code that shows how to manage events and how to request user permissions.</span></span> <span data-ttu-id="72eaf-114">您也可以看到一個範例，說明如何根據不同的光源條件來管理使用者介面。</span><span class="sxs-lookup"><span data-stu-id="72eaf-114">You can also see an example of how to manage the user interface based on varying lighting conditions.</span></span> <span data-ttu-id="72eaf-115">如需詳細資訊，請參閱 [建立 Light-Aware 使用者介面](creating-light-aware-user-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="72eaf-115">For more information, see [Creating Light-Aware User Interfaces](creating-light-aware-user-interfaces.md).</span></span><br/> <span data-ttu-id="72eaf-116">您必須安裝 Visual Studio 2008 才能建立此範例。</span><span class="sxs-lookup"><span data-stu-id="72eaf-116">You must have Visual Studio 2008 installed to build this sample.</span></span><br/> |



 

<span data-ttu-id="72eaf-117">如需詳細資訊，請參閱範例隨附的名稱為 ReadMe.txt 的檔案。</span><span class="sxs-lookup"><span data-stu-id="72eaf-117">For more information, see the file named ReadMe.txt that is included with the sample.</span></span>

<span data-ttu-id="72eaf-118">您也可以從程式碼庫下載 AmbientLightAware 範例。</span><span class="sxs-lookup"><span data-stu-id="72eaf-118">You can also download the AmbientLightAware sample from Code Gallery.</span></span> <span data-ttu-id="72eaf-119">如需詳細資訊，請參閱 [環境亮感知](/samples/browse/?redirectedfrom=MSDN-samples) 下載頁面。</span><span class="sxs-lookup"><span data-stu-id="72eaf-119">For more information, see the [Ambient Light Aware](/samples/browse/?redirectedfrom=MSDN-samples) download page.</span></span>

## <a name="tools"></a><span data-ttu-id="72eaf-120">工具</span><span class="sxs-lookup"><span data-stu-id="72eaf-120">Tools</span></span>

<span data-ttu-id="72eaf-121">Windows SDK 包含虛擬光線感應器，可用來模擬硬體型光線感應器裝置。</span><span class="sxs-lookup"><span data-stu-id="72eaf-121">The Windows SDK includes a virtual light sensor that you can use to simulate a hardware-based light sensor device.</span></span> <span data-ttu-id="72eaf-122">您可以使用此工具，將資料提供給 AmbientLightAware 範例，以查看範例中的程式碼如何運作。</span><span class="sxs-lookup"><span data-stu-id="72eaf-122">You can use this tool to provide data to the AmbientLightAware sample to see how the code in the sample works.</span></span>

<span data-ttu-id="72eaf-123">下表說明您必須用來執行虛擬光線感應器的檔案。</span><span class="sxs-lookup"><span data-stu-id="72eaf-123">The following table describes the files you must use to run the virtual light sensor.</span></span> <span data-ttu-id="72eaf-124">您可以在已安裝 Windows SDK 的名稱為 Bin 的資料夾中找到這些檔案。</span><span class="sxs-lookup"><span data-stu-id="72eaf-124">You can find these files in the folder named Bin, where you installed the Windows SDK.</span></span> <span data-ttu-id="72eaf-125">例如，如果您在32位電腦上將 Windows SDK 安裝在 C 磁片磁碟機上，您會在下列資料夾中找到虛擬光線感應器檔案： C： \\ Program files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ Bin。</span><span class="sxs-lookup"><span data-stu-id="72eaf-125">For example, if you installed the Windows SDK on drive C on a 32-bit computer, you would find the virtual light sensor files in the following folder: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Bin.</span></span> <span data-ttu-id="72eaf-126">在64位的電腦上，您必須使用64位版本的工具。</span><span class="sxs-lookup"><span data-stu-id="72eaf-126">On 64-bit computers, you must use the 64-bit version of the tool.</span></span> <span data-ttu-id="72eaf-127">在 Windows SDK 中，64位工具位於名為 x64 的子資料夾中。</span><span class="sxs-lookup"><span data-stu-id="72eaf-127">In the Windows SDK, 64-bit tools are located in the subfolder named x64.</span></span>



| <span data-ttu-id="72eaf-128">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="72eaf-128">File name</span></span>                    | <span data-ttu-id="72eaf-129">描述</span><span class="sxs-lookup"><span data-stu-id="72eaf-129">Description</span></span>                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72eaf-130">VirtualLightSensor.exe</span><span class="sxs-lookup"><span data-stu-id="72eaf-130">VirtualLightSensor.exe</span></span>       | <span data-ttu-id="72eaf-131">此程式提供滑杆控制項，可讓您變更虛擬感應器所報告的燈光資料層級。</span><span class="sxs-lookup"><span data-stu-id="72eaf-131">This program provides a slider control that enables you to change the level of the light data that the virtual sensor reports.</span></span> |
| <span data-ttu-id="72eaf-132">VirtualLightSensorDriver.dll</span><span class="sxs-lookup"><span data-stu-id="72eaf-132">VirtualLightSensorDriver.dll</span></span> | <span data-ttu-id="72eaf-133">模擬燈光感應器的邏輯感應器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="72eaf-133">The logical sensor driver that simulates a light sensor.</span></span>                                                                       |
| <span data-ttu-id="72eaf-134">VirtualLightSensorDriver .inf</span><span class="sxs-lookup"><span data-stu-id="72eaf-134">VirtualLightSensorDriver.inf</span></span> | <span data-ttu-id="72eaf-135">虛擬光線感應器驅動程式的 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="72eaf-135">The INF file for the virtual light sensor driver.</span></span>                                                                              |



 

### <a name="installing-the-virtual-light-sensor"></a><span data-ttu-id="72eaf-136">安裝虛擬光線感應器</span><span class="sxs-lookup"><span data-stu-id="72eaf-136">Installing the Virtual Light Sensor</span></span>

<span data-ttu-id="72eaf-137">使用虛擬光線感應器應用程式之前，您必須安裝邏輯感應器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="72eaf-137">Before you use the virtual light sensor application, you must install the logical sensor driver.</span></span> <span data-ttu-id="72eaf-138">請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="72eaf-138">Follow these steps:</span></span>

1.  <span data-ttu-id="72eaf-139">以系統管理員身分開啟命令視窗。</span><span class="sxs-lookup"><span data-stu-id="72eaf-139">Open a command window as an administrator.</span></span>
2.  <span data-ttu-id="72eaf-140">變更為 Windows SDK Bin 資料夾。</span><span class="sxs-lookup"><span data-stu-id="72eaf-140">Change to the Windows SDK Bin folder.</span></span>
3.  <span data-ttu-id="72eaf-141">輸入 **pnputil-VirtualLightSensorDriver .inf**。</span><span class="sxs-lookup"><span data-stu-id="72eaf-141">Type **pnputil -a VirtualLightSensorDriver.inf**.</span></span>
4.  <span data-ttu-id="72eaf-142">出現提示時，請按一下 [ **繼續安裝此驅動程式軟體**]。</span><span class="sxs-lookup"><span data-stu-id="72eaf-142">When prompted, click **Install this driver software anyway**.</span></span>
5.  <span data-ttu-id="72eaf-143">等候命令視窗報告驅動程式已順利安裝。</span><span class="sxs-lookup"><span data-stu-id="72eaf-143">Wait for the command window to report that the driver was successfully installed.</span></span>

### <a name="running-the-virtual-light-sensor"></a><span data-ttu-id="72eaf-144">正在執行虛擬光線感應器</span><span class="sxs-lookup"><span data-stu-id="72eaf-144">Running the Virtual Light Sensor</span></span>

<span data-ttu-id="72eaf-145">若要執行虛擬光線感應器，只要按兩下 .exe 檔案。</span><span class="sxs-lookup"><span data-stu-id="72eaf-145">To run the virtual light sensor, simply double-click the .exe file.</span></span> <span data-ttu-id="72eaf-146">當系統提示時，請務必啟用感應器。</span><span class="sxs-lookup"><span data-stu-id="72eaf-146">Be sure to enable the sensor, when prompted.</span></span>

<span data-ttu-id="72eaf-147">當您執行程式時，可能會注意到感應器變成可用之前會有延遲。</span><span class="sxs-lookup"><span data-stu-id="72eaf-147">When you run the program, you may notice that there is a delay before the sensor becomes available.</span></span> <span data-ttu-id="72eaf-148">虛擬光線感應器使用者介面會在標題列中顯示「等待中」的訊息，而邏輯感應器管理員會為邏輯感應器建立裝置節點。</span><span class="sxs-lookup"><span data-stu-id="72eaf-148">The virtual light sensor user interface will display the message "Waiting" in the title bar while the logical sensor manager creates a device node for the logical sensor.</span></span> <span data-ttu-id="72eaf-149">等候的訊息消失之後，您可以使用滑杆來設定虛擬光線感應器的 lux 輸出等級。</span><span class="sxs-lookup"><span data-stu-id="72eaf-149">After the waiting message goes away, you can use the slider to set the lux output level for the virtual light sensor.</span></span>

<span data-ttu-id="72eaf-150">下圖顯示虛擬光線感應器使用者介面處於 [就緒] 狀態。</span><span class="sxs-lookup"><span data-stu-id="72eaf-150">The following image shows the virtual light sensor user interface in its ready state.</span></span>

![虛擬光線感應器使用者介面](images/virtuallightsensor.png)

## <a name="related-topics"></a><span data-ttu-id="72eaf-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="72eaf-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72eaf-153">關於邏輯感應器</span><span class="sxs-lookup"><span data-stu-id="72eaf-153">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> <dt>

[<span data-ttu-id="72eaf-154">**感應器 \_ 類別 \_ 燈**</span><span class="sxs-lookup"><span data-stu-id="72eaf-154">**SENSOR\_CATEGORY\_LIGHT**</span></span>](sensor-category-light.md)
</dt> </dl>

 

