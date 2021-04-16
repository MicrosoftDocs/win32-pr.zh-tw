---
title: Windows 10
description: 本逐步指南提供相關資訊，讓開發人員瞭解 Windows 10 作業系統 (作業系統) 的平臺變更。
ms.assetid: bf8d7d10-bab6-4711-b65f-5393d906e47b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03fce627969573deb395fda356564a85a3573682
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382546"
---
# <a name="windows-10"></a><span data-ttu-id="ed96c-103">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed96c-103">Windows 10</span></span>

<span data-ttu-id="ed96c-104">本逐步指南提供相關資訊，讓開發人員瞭解 Windows 10 作業系統 (作業系統) 的平臺變更。</span><span class="sxs-lookup"><span data-stu-id="ed96c-104">This Cookbook provides info for developers about platform changes to the Windows 10 operating systems (OS).</span></span> <span data-ttu-id="ed96c-105">我們也會提供指導方針，讓您使用最新版本的作業系統驗證現有和已規劃應用程式的相容性。</span><span class="sxs-lookup"><span data-stu-id="ed96c-105">We also provide guidelines for you to verify the compatibility of your existing and planned apps with the latest version of the OS.</span></span> <span data-ttu-id="ed96c-106">我們假設您已經熟悉舊版的 Windows。</span><span class="sxs-lookup"><span data-stu-id="ed96c-106">We assume that you are familiar with previous versions of Windows.</span></span>

<span data-ttu-id="ed96c-107">內容適用于： Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed96c-107">The content applies to: Windows 10</span></span>

<span data-ttu-id="ed96c-108">本指南適用于協力廠商開發的應用程式和裝置，其設計目的是要在 Microsoft Windows 環境中使用。</span><span class="sxs-lookup"><span data-stu-id="ed96c-108">The Cookbook is for third party developers of apps and devices that are designed to be used in the Microsoft Windows environment.</span></span>

## <a name="introduction"></a><span data-ttu-id="ed96c-109">簡介</span><span class="sxs-lookup"><span data-stu-id="ed96c-109">Introduction</span></span>

<span data-ttu-id="ed96c-110">Windows 10 介紹最新的 OS 技術和軟體發展平臺，供全球的應用程式和驅動程式開發人員和企業使用。</span><span class="sxs-lookup"><span data-stu-id="ed96c-110">Windows 10 introduces the latest OS technology and software development platforms for use by app and driver developers and enterprises worldwide.</span></span> <span data-ttu-id="ed96c-111">為了進一步增強 Windows 的安全性、可靠性、效能和使用者體驗，Microsoft 引進了許多新功能、改良的現有功能，並移除其他功能。</span><span class="sxs-lookup"><span data-stu-id="ed96c-111">To further enhance the security, reliability, performance, and user experience of Windows, Microsoft has introduced many new features, improved existing features, and removed others.</span></span>

<span data-ttu-id="ed96c-112">雖然 Windows 10 的目標是要維持與針對舊版 Windows OS 所撰寫之應用程式的相容性，但由於創新、加強的安全性和可靠性，某些相容性中斷是不可避免的。</span><span class="sxs-lookup"><span data-stu-id="ed96c-112">While the goal of Windows 10 is to maintain compatibility with apps written for previously released versions of the Windows OS, some compatibility breaks are inevitable due to innovations, tightened security, and increased reliability.</span></span> <span data-ttu-id="ed96c-113">整體來說，最新版本的 Windows 作業系統與現有的應用程式和裝置的相容性很高。</span><span class="sxs-lookup"><span data-stu-id="ed96c-113">Overall, the compatibility of the latest version of the Windows OS with existing apps and devices is high.</span></span>

<span data-ttu-id="ed96c-114">本檔說明如何驗證您的應用程式和裝置是否與最新版本的作業系統相容，並提供已知應用程式不相容問題的總覽。</span><span class="sxs-lookup"><span data-stu-id="ed96c-114">This document shows you how to verify that your apps and devices are compatible with the latest version of the OS and provides an overview of known app incompatibility issues.</span></span>

<span data-ttu-id="ed96c-115">我們邀請您查看這些主題，以瞭解如何優化您的應用程式，並利用此最新版本的 Windows 所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="ed96c-115">We invite you to check out these topics to learn how to optimize your apps and take advantage of what this newest release of Windows has to offer.</span></span>

## <a name="contents"></a><span data-ttu-id="ed96c-116">目錄</span><span class="sxs-lookup"><span data-stu-id="ed96c-116">Contents</span></span>

-   [<span data-ttu-id="ed96c-117">自 Windows 7 起的重要變更，以確保相容性</span><span class="sxs-lookup"><span data-stu-id="ed96c-117">Key changes since Windows 7 to ensure compatibility</span></span>](key-changes-since-windows-7-to-ensure-compatibility.md)
-   [<span data-ttu-id="ed96c-118">如何確保合併生態系統的相容性</span><span class="sxs-lookup"><span data-stu-id="ed96c-118">How we can ensure compatibility of the combined ecosystem</span></span>](how-we-can-ensure-compatibility-of-the-combined-ecosystem.md)
    -   [<span data-ttu-id="ed96c-119">Windows 版本檢查</span><span class="sxs-lookup"><span data-stu-id="ed96c-119">Windows version check</span></span>](windows-version-check.md)
    -   [<span data-ttu-id="ed96c-120">未記載的 API</span><span class="sxs-lookup"><span data-stu-id="ed96c-120">Undocumented APIs</span></span>](undocumented-apis.md)
    -   [<span data-ttu-id="ed96c-121">開發 UWP 和傳統型橋接器應用程式</span><span class="sxs-lookup"><span data-stu-id="ed96c-121">Develop UWP and Desktop Bridge apps</span></span>](/windows/desktop/w8cookbook/develop-universal-windows-platform-apps)
    -   [<span data-ttu-id="ed96c-122">如果未在視窗模式下執行，則會影響新式桌面應用程式功能</span><span class="sxs-lookup"><span data-stu-id="ed96c-122">Modern Desktop App functionality is impacted if not run in Windowed Mode</span></span>](modern-desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode.md)
    -   [<span data-ttu-id="ed96c-123">Windows Update 上適用的圖形驅動程式可用性</span><span class="sxs-lookup"><span data-stu-id="ed96c-123">Availability of applicable graphics drivers on Windows Update</span></span>](availability-of-applicable-graphics-drivers-on-windows-update.md)
    -   [<span data-ttu-id="ed96c-124">將圖形驅動程式遷移至 Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed96c-124">Graphics driver migration to Windows 10</span></span>](graphics-driver-migration-to-windows-10.md)
    -   [<span data-ttu-id="ed96c-125">藍牙驅動程式</span><span class="sxs-lookup"><span data-stu-id="ed96c-125">Bluetooth drivers</span></span>](bluetooth-drivers.md)

## <a name="download-the-cookbook"></a><span data-ttu-id="ed96c-126">下載操作手冊</span><span class="sxs-lookup"><span data-stu-id="ed96c-126">Download the cookbook</span></span>

<span data-ttu-id="ed96c-127">如需這些資訊的快速參考，以及有關 Windows 即服務的資訊、支援 Windows 中的應用程式，以及測試應用程式的優化策略，請 [下載 Windows 10 相容性操作手冊](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx)。</span><span class="sxs-lookup"><span data-stu-id="ed96c-127">For a quick reference to all this information, as well as information on Windows as a service, supporting apps in Windows, and optimized strategies for testing your app, [download the Windows 10 Compatibility Cookbook](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed96c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed96c-128">See Also</span></span>

-   <span data-ttu-id="ed96c-129">[Windows 即服務](/windows/deployment/update/)，以取得 Windows 10 版本類型和應用程式支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ed96c-129">[Windows as a service](/windows/deployment/update/), for information about Windows 10 release types and app support.</span></span>
-   <span data-ttu-id="ed96c-130">[Windows 測試人員](https://insider.windows.com/)，以存取預覽組建、測試及提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="ed96c-130">[Windows Insider](https://insider.windows.com/), to access preview builds, test, and provide feedback.</span></span>
-   <span data-ttu-id="ed96c-131">[Ready for Windows 10](https://www.readyfor10.com/)，將貴公司的資訊提交給 IT 管理員的資源。</span><span class="sxs-lookup"><span data-stu-id="ed96c-131">[Ready for Windows 10](https://www.readyfor10.com/), to submit your company's information to a resource for IT managers.</span></span>

 

 