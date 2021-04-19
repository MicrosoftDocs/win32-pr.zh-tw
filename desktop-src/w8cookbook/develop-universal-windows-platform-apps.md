---
title: 開發通用 Windows 平臺 (UWP) 應用程式
description: 開發通用 Windows 平臺 (UWP) 應用程式
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "106968889"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a><span data-ttu-id="b7c5c-103">開發通用 Windows 平臺 (UWP) 應用程式</span><span class="sxs-lookup"><span data-stu-id="b7c5c-103">Develop Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="b7c5c-104">我們鼓勵所有 desktop (Win32) 應用程式 Isv，透過) 將您的桌面應用程式帶入 [通用 Windows 平臺 (UWP 傳統型橋接器 ](https://developer.microsoft.com/windows/bridges/desktop/) 。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-104">We encourage all desktop (Win32) app ISVs to bring your desktop apps to the [Universal Windows Platform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via the Desktop Bridge.</span></span> <span data-ttu-id="b7c5c-105">[Windows 市集](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/)中也支援 UWP app，這可讓您更容易地將使用者自動更新至一致的版本，減低您的支援成本。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-105">UWP apps are also supported in the [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), so it’s easier for you to update your users to a consistent version automatically, lowering your support costs.</span></span>

<span data-ttu-id="b7c5c-106">如果您的桌面應用程式無法使用傳統型橋接器進行轉換，強烈建議您使用遵循最佳作法的安裝程式，並確定已完整測試。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-106">If your desktop apps cannot be converted using the Desktop Bridge, we highly recommend that you use an installer that follows best practices, and ensure this is fully tested.</span></span> <span data-ttu-id="b7c5c-107">安裝程式是您的使用者或客戶首次使用您的應用程式體驗。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-107">An installer is your user or customer's first experience with your app.</span></span> <span data-ttu-id="b7c5c-108">很多時候安裝程式無法正常運作，或未經過所有案例的完整測試。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-108">All too often, this doesn’t work well or it hasn’t been fully tested for all scenarios.</span></span> <span data-ttu-id="b7c5c-109">[Windows 應用程式認證套件](https://dev.windows.com/develop/app-certification-kit)可協助您測試 Win32 應用程式的安裝和卸載，並協助您識別使用未記載的 api，以及在使用者執行之前的其他基本效能相關最佳做法問題。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-109">The [Windows App Certification Kit](https://dev.windows.com/develop/app-certification-kit) can help you test install and uninstall of your Win32 app and help you identify use of undocumented APIs, as well as other basic performance-related best-practice issues before your users do.</span></span>

## <a name="best-practices"></a><span data-ttu-id="b7c5c-110">最佳做法：</span><span class="sxs-lookup"><span data-stu-id="b7c5c-110">Best practices:</span></span>

-   <span data-ttu-id="b7c5c-111">使用可在 32 位元及 64 位元版本 Windows 中運作的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-111">Use installers that work for both 32-bit and 64-bit versions of Windows.</span></span>
-   <span data-ttu-id="b7c5c-112">將您的安裝程式設計為在多種案例上執行 (使用者或電腦層級)。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-112">Design your installers to run on multiple scenarios (user or machine level).</span></span>
-   <span data-ttu-id="b7c5c-113">將所有的 Windows 可轉散發檔案保留在原始封裝中 – 如果您重新封裝這些檔案，可能會破壞安裝程式。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-113">Keep all Windows redistributables in the original packaging – if you repackage these, it’s possible that this will break the installer.</span></span>
-   <span data-ttu-id="b7c5c-114">為您的安裝程式排程開發時間—這些通常會在軟體開發週其中忽略為可交付項目。</span><span class="sxs-lookup"><span data-stu-id="b7c5c-114">Schedule development time for your installers—these are often overlooked as a deliverable during the software development lifecycle.</span></span>

 

 




