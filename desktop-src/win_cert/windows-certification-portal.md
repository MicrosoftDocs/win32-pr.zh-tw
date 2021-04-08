---
title: 認證您的桌面應用程式
description: 請遵循下列步驟，讓您的桌面應用程式通過 Windows 7、Windows 8、Windows 8.1 和 Windows 10 的認證。如果您想要轉換您的傳統型應用程式，使其與通用 Windows 平臺和 Windows Store 相容，您將使用 Windows 傳統型橋接器，在這種情況下，您應該遵循認證步驟的傳統型橋接器指導方針。如果您要從一開始就開發和驗證 UWP 應用程式，請參閱 UWP 中的 Windows 應用程式認證指引以取得認證資訊。
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684172"
---
# <a name="certify-your-desktop-application"></a><span data-ttu-id="e5743-103">認證您的桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="e5743-103">Certify your desktop application</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5743-104">Win32 桌面應用程式的憑證已 [淘汰](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920)。</span><span class="sxs-lookup"><span data-stu-id="e5743-104">Certification for Win32 desktop apps is [deprecated](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span></span> <span data-ttu-id="e5743-105">相反地，請 [在此提交檔](https://www.microsoft.com/wdsi/filesubmission/)。</span><span class="sxs-lookup"><span data-stu-id="e5743-105">Instead, [submit files here](https://www.microsoft.com/wdsi/filesubmission/).</span></span>

<span data-ttu-id="e5743-106">請遵循下列步驟，讓您的桌面應用程式通過 Windows 7、Windows 8、Windows 8.1 和 Windows 10 的認證。</span><span class="sxs-lookup"><span data-stu-id="e5743-106">Follow these steps to get your desktop app certified for Windows 7, Windows 8, Windows 8.1, and Windows 10.</span></span>

<span data-ttu-id="e5743-107">如果您想要轉換您的傳統型應用程式，使其與通用 Windows 平臺和 Windows Store 相容，您將使用 [Windows 傳統型橋接器](https://developer.microsoft.com/windows/bridges/desktop)，在這種情況下，您應該遵循認證步驟的 [傳統型橋接器](/windows/uwp/porting/desktop-to-uwp-root) 指導方針。</span><span class="sxs-lookup"><span data-stu-id="e5743-107">If you wish to convert your desktop app to be compatible with the Universal Windows Platform and Windows Store, you will use the [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop), in which case you should follow the [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) guidance for certification steps.</span></span>

<span data-ttu-id="e5743-108">如果您要從一開始就開發和驗證 UWP 應用程式，請參閱 [UWP 中的 Windows 應用程式認證指引](/windows/uwp/debug-test-perf/windows-app-certification-kit) 以取得認證資訊。</span><span class="sxs-lookup"><span data-stu-id="e5743-108">If you are developing and certifying a UWP app from the start, see [Guidance for Windows App Certification in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) for info on certification.</span></span>

## <a name="step-1-prepare-for-certification"></a><span data-ttu-id="e5743-109">步驟1：準備認證</span><span class="sxs-lookup"><span data-stu-id="e5743-109">Step 1: Prepare for certification</span></span>



| <span data-ttu-id="e5743-110">主題</span><span class="sxs-lookup"><span data-stu-id="e5743-110">Topic</span></span>                                                                                       | <span data-ttu-id="e5743-111">描述</span><span class="sxs-lookup"><span data-stu-id="e5743-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5743-112">有哪些優點？</span><span class="sxs-lookup"><span data-stu-id="e5743-112">What are the benefits?</span></span>](what-are-the-benefits-.md)<br/>                             | <span data-ttu-id="e5743-113">認證您的桌面應用程式可為您和您的客戶提供數個優點。</span><span class="sxs-lookup"><span data-stu-id="e5743-113">Certifying your desktop app provides several benefits for you and your customers.</span></span>              |
| [<span data-ttu-id="e5743-114">閱讀需求</span><span class="sxs-lookup"><span data-stu-id="e5743-114">Read the requirements</span></span>](certification-requirements-for-windows-desktop-apps.md)<br/> | <span data-ttu-id="e5743-115">查看傳統型應用程式必須滿足的技術需求和資格資格。</span><span class="sxs-lookup"><span data-stu-id="e5743-115">Review the technical requirements and eligibility qualifications that a desktop app must meet.</span></span> |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a><span data-ttu-id="e5743-116">步驟2：使用 Windows 應用程式認證套件測試您的應用程式</span><span class="sxs-lookup"><span data-stu-id="e5743-116">Step 2: Test your app with the Windows App Certification Kit</span></span>



| <span data-ttu-id="e5743-117">主題</span><span class="sxs-lookup"><span data-stu-id="e5743-117">Topic</span></span>                                                          | <span data-ttu-id="e5743-118">描述</span><span class="sxs-lookup"><span data-stu-id="e5743-118">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5743-119">取得套件</span><span class="sxs-lookup"><span data-stu-id="e5743-119">Get the Kit</span></span>](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | <span data-ttu-id="e5743-120">若要認證您的應用程式，您必須安裝並執行 Windows SDK) 中包含的 Windows 應用程式認證套件 (。</span><span class="sxs-lookup"><span data-stu-id="e5743-120">To certify your app, you have to install and run the Windows App Certification Kit (included in the Windows SDK).</span></span>                                                                     |
| [<span data-ttu-id="e5743-121">使用套件</span><span class="sxs-lookup"><span data-stu-id="e5743-121">Using the Kit</span></span>](using-the-windows-app-certification-kit.md)   | <span data-ttu-id="e5743-122">在您可以提交應用程式之前，您必須先測試應用程式是否就緒。</span><span class="sxs-lookup"><span data-stu-id="e5743-122">Before you can submit your app, you must test it for readiness.</span></span> <span data-ttu-id="e5743-123">您也可以下載一份 [應用程式認證白皮書](https://www.microsoft.com/download/details.aspx?id=27414)。</span><span class="sxs-lookup"><span data-stu-id="e5743-123">You can also download a copy of the [app certification white paper](https://www.microsoft.com/download/details.aspx?id=27414).</span></span> |
| [<span data-ttu-id="e5743-124">審核測試詳細資料</span><span class="sxs-lookup"><span data-stu-id="e5743-124">Review test details</span></span>](windows-app-certification-kit-tests.md) | <span data-ttu-id="e5743-125">取得您的應用程式必須傳遞的測試清單，以符合最新 Windows 作業系統的相容性。</span><span class="sxs-lookup"><span data-stu-id="e5743-125">Get the list of the tests your app needs to pass to qualify for compatibility with the latest Windows operating system.</span></span>                                                               |



 

<span data-ttu-id="e5743-126">注意：篩選器驅動程式也必須通過 [硬體認證套件](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe)。</span><span class="sxs-lookup"><span data-stu-id="e5743-126">Note: Filter drivers must also pass the [Hardware Certification Kit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span></span> <span data-ttu-id="e5743-127"> (參閱 [Windows 傳統型應用程式的認證需求，第6.2 節](certification-requirements-for-windows-desktop-apps.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="e5743-127">(See [Certification requirements for Windows desktop apps, section 6.2](certification-requirements-for-windows-desktop-apps.md).)</span></span>

## <a name="step-3-use-the-windows-certification-dashboard"></a><span data-ttu-id="e5743-128">步驟3：使用 Windows 認證儀表板</span><span class="sxs-lookup"><span data-stu-id="e5743-128">Step 3: Use the Windows Certification Dashboard</span></span>

<span data-ttu-id="e5743-129">若要提交認證的應用程式，您必須在 [Windows 認證儀表板](/previous-versions/hh833792(v=msdn.10))上登入或註冊公司帳戶。</span><span class="sxs-lookup"><span data-stu-id="e5743-129">To submit your app for certification, you'll need to log in or register a company account on the [Windows Certification Dashboard](/previous-versions/hh833792(v=msdn.10)).</span></span> <span data-ttu-id="e5743-130">一旦您這樣做，不僅能讓您的應用程式通過認證，還可以存取工具，在程式的所有階段檢查及管理您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e5743-130">Once you do, not only will you be able to get your app certified, but you'll also gain access to tools to review and manage your app at all stages of the process.</span></span>



| <span data-ttu-id="e5743-131">主題</span><span class="sxs-lookup"><span data-stu-id="e5743-131">Topic</span></span>                                                                                                                   | <span data-ttu-id="e5743-132">描述</span><span class="sxs-lookup"><span data-stu-id="e5743-132">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5743-133">設定帳戶</span><span class="sxs-lookup"><span data-stu-id="e5743-133">Set up your account</span></span>](/windows-hardware/drivers/dashboard/)                 | <span data-ttu-id="e5743-134">如果您的公司尚未註冊，您必須透過 Windows 認證儀表板註冊。</span><span class="sxs-lookup"><span data-stu-id="e5743-134">If your company isn't already registered, you must register it through the Windows Certification Dashboard.</span></span>                                        |
| [<span data-ttu-id="e5743-135">取得程式碼簽署憑證</span><span class="sxs-lookup"><span data-stu-id="e5743-135">Get a code signing certificate</span></span>](/windows-hardware/drivers/dashboard/)      | <span data-ttu-id="e5743-136">建立 Windows 認證儀表板帳戶之前，您必須先取得程式碼簽署憑證來保護您的數位資訊。</span><span class="sxs-lookup"><span data-stu-id="e5743-136">Before you can establish a Windows Certification Dashboard account, you need to get a code signing certificate to secure your digital information.</span></span> |
| [<span data-ttu-id="e5743-137">在本機測試並上傳結果</span><span class="sxs-lookup"><span data-stu-id="e5743-137">Test locally and upload the results</span></span>](/windows-hardware/drivers/dashboard/) | <span data-ttu-id="e5743-138">在您執行 Windows 應用程式認證套件測試之後，請將結果上傳至 Windows 認證儀表板。</span><span class="sxs-lookup"><span data-stu-id="e5743-138">After your run the Windows App Certification Kit tests, upload the results to the Windows Certification Dashboard.</span></span>                                 |
| [<span data-ttu-id="e5743-139">管理您的提交內容</span><span class="sxs-lookup"><span data-stu-id="e5743-139">Manage your submission</span></span>](/windows-hardware/drivers/dashboard/)              | <span data-ttu-id="e5743-140">提交您的應用程式以進行認證之後，您可以透過 Windows 認證儀表板審查您的提交內容。</span><span class="sxs-lookup"><span data-stu-id="e5743-140">After you submit your app for certification, you can review your submission through the Windows Certification Dashboard.</span></span>                           |



 

## <a name="step-4-promote-your-desktop-app"></a><span data-ttu-id="e5743-141">步驟4：升級您的桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="e5743-141">Step 4: Promote your desktop app</span></span>



| <span data-ttu-id="e5743-142">主題</span><span class="sxs-lookup"><span data-stu-id="e5743-142">Topic</span></span>                                                                      | <span data-ttu-id="e5743-143">描述</span><span class="sxs-lookup"><span data-stu-id="e5743-143">Description</span></span>                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5743-144">檢查應用程式相容性</span><span class="sxs-lookup"><span data-stu-id="e5743-144">Check app compatibility</span></span>](/windows/compatibility/windows-8-1-introduction) | <span data-ttu-id="e5743-145">如果您正在建立 Windows 8.1 的應用程式，請調查相容性問題。</span><span class="sxs-lookup"><span data-stu-id="e5743-145">If you are building an app for Windows 8.1, investigate compatibility concerns.</span></span>                                           |
| [<span data-ttu-id="e5743-146">搭配您的應用程式使用標誌</span><span class="sxs-lookup"><span data-stu-id="e5743-146">Use the logo with your app</span></span>](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | <span data-ttu-id="e5743-147">根據指導方針，顯示封裝和廣告中的標誌，以及其他促銷材料。</span><span class="sxs-lookup"><span data-stu-id="e5743-147">Display the logo on packaging and in ads and other promotional materials according to the guidelines.</span></span> <span data-ttu-id="e5743-148">僅適用于 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="e5743-148">For Windows 7 only.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="e5743-149">另請參閱：</span><span class="sxs-lookup"><span data-stu-id="e5743-149">See also:</span></span>

<span data-ttu-id="e5743-150">[應用程式相容性論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility)：從社區尋找相容性與標誌認證的支援。</span><span class="sxs-lookup"><span data-stu-id="e5743-150">[App compatibility forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): Find support from the community about compatibility and logo certification.</span></span>

<span data-ttu-id="e5743-151">[Windows SDK 的 blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/)：尋找與應用程式認證相關的秘訣和新聞。</span><span class="sxs-lookup"><span data-stu-id="e5743-151">[Windows SDK blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Find tips and news related to app certification.</span></span>

<span data-ttu-id="e5743-152">[Windows Server 論壇]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat)：造訪認證論壇以取得解答。</span><span class="sxs-lookup"><span data-stu-id="e5743-152">[Windows Server forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Visit the Certification forum to get answers.</span></span>

<span data-ttu-id="e5743-153">[相容性操作手冊](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)：取得最新 Windows 版本的新功能或變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e5743-153">[Compatibility cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Get info about what's new or changed in the latest version of Windows.</span></span>

 

