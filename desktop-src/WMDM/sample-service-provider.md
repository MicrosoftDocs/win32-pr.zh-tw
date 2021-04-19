---
title: 範例服務提供者
description: 範例服務提供者
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Media 裝置管理員，範例
- 裝置管理員，範例
- Windows Media 裝置管理員、服務提供者範例
- 裝置管理員，服務提供者範例
- 服務提供者，範例
- 範例，服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106991287"
---
# <a name="sample-service-provider"></a><span data-ttu-id="f6b05-109">範例服務提供者</span><span class="sxs-lookup"><span data-stu-id="f6b05-109">Sample Service Provider</span></span>

<span data-ttu-id="f6b05-110">Windows Media 裝置管理員 SDK 包含可供您使用的範例服務提供者。</span><span class="sxs-lookup"><span data-stu-id="f6b05-110">The Windows Media Device Manager SDK includes a sample service provider for you to use.</span></span> <span data-ttu-id="f6b05-111">此服務提供者包含的類別會報告電腦上的每個硬碟，就像是連接的裝置一樣。</span><span class="sxs-lookup"><span data-stu-id="f6b05-111">This service provider includes a class that reports each hard drive on the computer as if it were an attached device.</span></span> <span data-ttu-id="f6b05-112">將使用此服務提供者的唯一應用程式是範例應用程式;Windows 檔案總管將不會看到此服務提供者所報告的「裝置」。</span><span class="sxs-lookup"><span data-stu-id="f6b05-112">The only application that will use this service provider is the sample application; Windows Explorer will not see the "devices" reported by this service provider.</span></span> <span data-ttu-id="f6b05-113">服務提供者範例是以 ATL 建立的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="f6b05-113">The service provider sample is a COM object built on ATL.</span></span> <span data-ttu-id="f6b05-114">下列步驟說明如何使用範例服務提供者：</span><span class="sxs-lookup"><span data-stu-id="f6b05-114">The following steps explain how to use the sample service provider:</span></span>

> [!Note]  
> <span data-ttu-id="f6b05-115">範例服務提供者會執行很少的功能，因此不應該用於測試 Windows Media 裝置管理員應用程式。</span><span class="sxs-lookup"><span data-stu-id="f6b05-115">The sample service provider implements very few features, and so it should not be used for testing Windows Media Device Manager applications.</span></span> <span data-ttu-id="f6b05-116">若要測試應用程式，請使用完全執行的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="f6b05-116">To test an application, use a fully-implemented service provider.</span></span>

 

-   <span data-ttu-id="f6b05-117">此範例隨附的程式碼錯誤，會導致服務提供者無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f6b05-117">The sample was shipped with a coding error that will cause the service provider to malfunction.</span></span> <span data-ttu-id="f6b05-118">若要更正這個錯誤，請開啟安裝在 < *SDK 安裝路徑* WMFSDK95 WMDM mdsp mshdsp 資料夾中的 MDSPEnumStorage .cpp 檔案  > \\ \\ \\ \\ ，移至第185行，然後變更下行：</span><span class="sxs-lookup"><span data-stu-id="f6b05-118">To correct this error, open the MDSPEnumStorage.cpp file installed in the folder < *SDK installation path* >\\WMFSDK95\\WMDM\\mdsp\\mshdsp, go to line 185, and change the following line:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

<span data-ttu-id="f6b05-119">為此值：</span><span class="sxs-lookup"><span data-stu-id="f6b05-119">To this:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  <span data-ttu-id="f6b05-120">編譯 MsHDSP.dll 檔案。</span><span class="sxs-lookup"><span data-stu-id="f6b05-120">Compile the MsHDSP.dll file.</span></span> <span data-ttu-id="f6b05-121">您可以使用 NMAKE 或 Visual Studio 來進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="f6b05-121">You can do this using either NMAKE or Visual Studio.</span></span> <span data-ttu-id="f6b05-122">請參閱 [使用 NMAKE 編譯範例服務提供者](compiling-the-sample-service-provider-using-nmake.md) 或 [使用 Visual Studio 編譯範例服務提供者](compiling-the-sample-service-provider-using-visual-studio.md) ，以瞭解如何編譯應用程式。</span><span class="sxs-lookup"><span data-stu-id="f6b05-122">See [Compiling the Sample Service Provider Using NMAKE](compiling-the-sample-service-provider-using-nmake.md) or [Compiling the Sample Service Provider Using Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) to learn how to compile the application.</span></span>
2.  <span data-ttu-id="f6b05-123">使用 regsvr32 註冊 MsHDSP.dll。</span><span class="sxs-lookup"><span data-stu-id="f6b05-123">Register MsHDSP.dll using regsvr32.</span></span> <span data-ttu-id="f6b05-124">在與 MsHDSP.dll 相同的資料夾中，輸入至命令提示字元視窗的下列程式程式碼，將會註冊範例服務提供者：</span><span class="sxs-lookup"><span data-stu-id="f6b05-124">The following line, typed into a command-prompt window in the same folder as MsHDSP.dll, will register the sample service provider:</span></span>

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    <span data-ttu-id="f6b05-125">若要停止模擬裝置，請在命令提示字元中輸入下列程式程式碼：</span><span class="sxs-lookup"><span data-stu-id="f6b05-125">To stop impersonating a device, enter the following line at the command prompt:</span></span>

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  <span data-ttu-id="f6b05-126">此 DLL 所模擬的卸載式裝置只能由這個 SDK 隨附的範例應用程式查看。</span><span class="sxs-lookup"><span data-stu-id="f6b05-126">The removable devices impersonated by this DLL can only be seen by the sample application shipped with this SDK.</span></span> <span data-ttu-id="f6b05-127">使用 [範例桌面應用程式](sample-desktop-application.md)中所述的其中一種方法來編譯範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="f6b05-127">Compile the sample application using one of the methods described in [Sample Desktop Application](sample-desktop-application.md).</span></span>
4.  <span data-ttu-id="f6b05-128">若要使用 Visual Studio 來偵測服務提供者，請在 Visual Studio 中開啟服務提供者，然後選取 [**調試** 程式] 功能表上的 [**啟動**]。</span><span class="sxs-lookup"><span data-stu-id="f6b05-128">To debug the service provider with Visual Studio, open the service provider in Visual Studio and select **Start** on the **Debug** menu.</span></span> <span data-ttu-id="f6b05-129">在快顯對話方塊中，流覽至您在上一個步驟中建立的範例應用程式，然後按一下 **[確定]**，服務提供者就會開始在 [偵測] 模式下執行。</span><span class="sxs-lookup"><span data-stu-id="f6b05-129">In the popup dialog box, browse to the sample application you built in the preceding step, and click **OK**, and the service provider will begin running in debug mode.</span></span>

    <span data-ttu-id="f6b05-130">若要執行服務提供者，而不在 Visual Studio 中進行偵錯工具，只要註冊 msdhsp.dll，然後執行 SDK 隨附的範例桌面應用程式即可。</span><span class="sxs-lookup"><span data-stu-id="f6b05-130">To run the service provider without debugging in Visual Studio, simply register the msdhsp.dll and run the sample desktop application that ships with the SDK.</span></span> <span data-ttu-id="f6b05-131">範例桌面應用程式會自動執行範例服務提供者。</span><span class="sxs-lookup"><span data-stu-id="f6b05-131">The sample desktop application runs the sample service provider automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6b05-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6b05-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6b05-133">**範例**</span><span class="sxs-lookup"><span data-stu-id="f6b05-133">**Samples**</span></span>](samples.md)
</dt> </dl>

 

 




