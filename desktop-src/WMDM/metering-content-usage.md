---
title: 計量內容使用方式
description: 計量內容使用方式
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Media 裝置管理員，計量內容使用方式
- 裝置管理員，計量內容使用方式
- 程式設計指南，計量內容使用方式
- 桌面應用程式，計量內容使用方式
- 建立 Windows Media 裝置管理員應用程式、計量內容使用方式
- 計量內容使用方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649eee810e7bbdbc2ea93a32c6368ec345fa7364
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106983307"
---
# <a name="metering-content-usage"></a><span data-ttu-id="2e4fe-109">計量內容使用方式</span><span class="sxs-lookup"><span data-stu-id="2e4fe-109">Metering Content Usage</span></span>

<span data-ttu-id="2e4fe-110">使用 Windows Media 10 技術，您現在可以計量可攜式裝置上的內容使用方式。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-110">With Windows Media 10 technology, you can now meter content usage on a portable device.</span></span> <span data-ttu-id="2e4fe-111">如果 Windows Media 10 授權允許計量，則裝置可以儲存歌曲的播放次數，並透過網際網路將使用量上傳回授權簽發者。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-111">If a Windows Media 10 license allows metering, the device can store the play count for songs and upload usage back to the license issuer over the Internet.</span></span> <span data-ttu-id="2e4fe-112">此系統可讓內容提供者藉由精確地測量內容使用方式，來調整其特許費用。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-112">This system enables content providers to adjust their royalty fees by accurately measuring content usage.</span></span>

<span data-ttu-id="2e4fe-113">若要計量內容，應用程式必須具有以 Windows Media Rights Manager 10 SDK 為基礎的授權服務所提供的計量憑證。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-113">To meter content, the application must have a metering certificate provided by a licensing service built on the Windows Media Rights Manager 10 SDK.</span></span> <span data-ttu-id="2e4fe-114">只有這個相同服務所授權的內容可以進行計量。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-114">Only content licensed by this same service can be metered.</span></span> <span data-ttu-id="2e4fe-115">如需有關計量運作方式以及如何建立授權計量服務的詳細資訊，請參閱 MSDN 上的 [Windows Media Rights MANAGER SDK 檔](/previous-versions/ms986509(v=msdn.10)) 。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-115">For more information on how metering works, and how to build a license metering service, see the [Windows Media Rights Manager SDK documentation](/previous-versions/ms986509(v=msdn.10)) on MSDN.</span></span> <span data-ttu-id="2e4fe-116">您可以藉由填寫 [Windows Media 授權頁面](https://www.microsoft.com/licensing/default)上的必要資訊來取得 SDK。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-116">The SDK can be acquired by filling out the necessary information on the [Windows Media Licensing Page](https://www.microsoft.com/licensing/default).</span></span>

<span data-ttu-id="2e4fe-117">應用程式可以內建計量，或者，如果應用程式接受計量外掛程式，您可以為現有的應用程式（例如 Windows Media Player）建立 COM 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-117">An application can have metering built in to it, or you can build a COM plug-in for an existing application, such as the Windows Media Player, if the application accepts metering plug-ins.</span></span>

<span data-ttu-id="2e4fe-118">應用程式應該在內容使用方式會進行計量時警告使用者。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-118">An application should warn users if content usage will be metered.</span></span> <span data-ttu-id="2e4fe-119">如需詳細資訊，請參閱 [隱私權聲明](privacy-statement.md)中列出的 Microsoft 網頁。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-119">For more information, see the Microsoft Web pages listed in the [Privacy Statement](privacy-statement.md).</span></span>

<span data-ttu-id="2e4fe-120">從裝置取得計量資料可能很慢。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-120">Acquiring metering data from a device can be slow.</span></span> <span data-ttu-id="2e4fe-121">因此，如果應用程式計量使用量，則應該經常這麼做，以防止大量資料在裝置上累積，並減緩資料傳送速率。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-121">Therefore, if an application meters usage, it should do so frequently to prevent large amounts of data from accumulating on the device and slowing down the data transfer.</span></span> <span data-ttu-id="2e4fe-122">為了避免資料傳送速率太慢，裝置製造商可以傳送可用計量資料的子集。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-122">To prevent data transfers that would be too slow, device manufacturers can send subsets of available metering data.</span></span> <span data-ttu-id="2e4fe-123">應用程式應監視 [**IWMDRMDeviceApp：:P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md) 所抓取的旗標，以查看是否有任何其他計量資料仍保留在裝置上。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-123">The application should monitor the flags retrieved by [**IWMDRMDeviceApp::ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md) to see if any more metering data remains on the device.</span></span>

<span data-ttu-id="2e4fe-124">下列步驟顯示應用程式如何測量內容的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-124">The following steps show how an application can meter content usage.</span></span>

1.  <span data-ttu-id="2e4fe-125">由於計量僅適用于支援可攜式裝置之 Windows Media DRM 10 的裝置，因此您的應用程式應該在某個時間點呼叫 **QueryDeviceStatus**（如 [處理應用程式中受保護的內容](handling-protected-content-in-the-application.md)所述），以確保裝置有效且為最新狀態。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-125">Because metering is only available on devices that support Windows Media DRM 10 for Portable Devices, your application should at some point call **QueryDeviceStatus**, as described in [Handling Protected Content in the Application](handling-protected-content-in-the-application.md), to ensure that the device is valid and up to date.</span></span>
2.  <span data-ttu-id="2e4fe-126">藉由呼叫 [**IWMDRMDeviceApp：： GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md)，要求來自裝置的計量資訊。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-126">Request metering information from the device by calling [**IWMDRMDeviceApp::GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span></span>
3.  <span data-ttu-id="2e4fe-127">將已取出的計量資料傳送至 **GenerateMeterChallenge** 所抓取之 URL 的計量服務。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-127">Send the retrieved metering data to the metering service at the URL retrieved by **GenerateMeterChallenge**.</span></span> <span data-ttu-id="2e4fe-128">傳送至服務的資料格式取決於該特定服務的腳本。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-128">The format of data sent to the service depends on the scripting on that particular service.</span></span> <span data-ttu-id="2e4fe-129">例如，某些服務可能需要以 POST 命令形式傳送的資料做為名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-129">For example, some services might require the data sent as a POST command as a name/value pair.</span></span> <span data-ttu-id="2e4fe-130">服務提供者應可讓您知道其特定的格式需求。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-130">The service provider should let you know their particular formatting requirements.</span></span>
4.  <span data-ttu-id="2e4fe-131">取得計量服務的回應，並呼叫 [**IWMDRMDeviceApp：:P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md)將其傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-131">Get a response from the metering service, and send it to the device by calling [**IWMDRMDeviceApp::ProcessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md).</span></span> <span data-ttu-id="2e4fe-132">這會導致裝置重設播放次數，也會傳回一個值，指出裝置上是否有更多的計量資料，應該再次呼叫 **GenerateMeterChallenge** 來取出。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-132">This causes the device to reset play counts, and also returns a value indicating whether more metering data exists on the device that should be retrieved by calling **GenerateMeterChallenge** again.</span></span>

<span data-ttu-id="2e4fe-133">如需計量的詳細資訊和範例程式碼，請參閱 [Windows Media 網站](/previous-versions//bb614723(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2e4fe-133">For extensive information and sample code for metering, see the [Windows Media Web site](/previous-versions//bb614723(v=vs.85)).</span></span>

 

 