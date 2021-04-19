---
description: 從 Windows 8 開始， \_ 啟用安全開機時，會停用 AppInit dll 基礎結構。
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit Dll 和安全開機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000323"
---
# <a name="appinit-dlls-and-secure-boot"></a><span data-ttu-id="cca5d-103">AppInit Dll 和安全開機</span><span class="sxs-lookup"><span data-stu-id="cca5d-103">AppInit DLLs and Secure Boot</span></span>

<span data-ttu-id="cca5d-104">從 Windows 8 開始， \_ 啟用安全開機時，會停用 AppInit dll 基礎結構。</span><span class="sxs-lookup"><span data-stu-id="cca5d-104">Starting in Windows 8, the AppInit\_DLLs infrastructure is disabled when secure boot is enabled.</span></span>

## <a name="about-appinit_dlls"></a><span data-ttu-id="cca5d-105">關於 AppInit \_ dll</span><span class="sxs-lookup"><span data-stu-id="cca5d-105">About AppInit\_DLLs</span></span>

<span data-ttu-id="cca5d-106">AppInit \_ dll 基礎結構可讓您輕鬆地攔截系統 api，方法是允許將自訂 dll 載入至每個互動式應用程式的位址空間中。</span><span class="sxs-lookup"><span data-stu-id="cca5d-106">The AppInit\_DLLs infrastructure provides an easy way to hook system APIs by allowing custom DLLs to be loaded into the address space of every interactive application.</span></span> <span data-ttu-id="cca5d-107">應用程式和惡意軟體都使用 AppInit Dll 的原因，是為了攔截 Api;載入自訂 DLL 之後，它可以攔截已知的系統 API 並執行替代功能。</span><span class="sxs-lookup"><span data-stu-id="cca5d-107">Applications and malicious software both use AppInit DLLs for the same basic reason, which is to hook APIs; after the custom DLL is loaded, it can hook a well-known system API and implement alternate functionality.</span></span> <span data-ttu-id="cca5d-108">只有一小部分的新式合法應用程式會使用這項機制來載入 Dll，而一組大型惡意程式碼會使用這項機制來危害系統。</span><span class="sxs-lookup"><span data-stu-id="cca5d-108">Only a small set of modern legitimate applications use this mechanism to load DLLs, while a large set of malware use this mechanism to compromise systems.</span></span> <span data-ttu-id="cca5d-109">即使合法的 AppInit \_ dll 也可能會不慎造成系統鎖死和效能問題，因此 \_ 不建議使用 AppInit dll。</span><span class="sxs-lookup"><span data-stu-id="cca5d-109">Even legitimate AppInit\_DLLs can unintentionally cause system deadlocks and performance problems, therefore usage of AppInit\_DLLs is not recommended.</span></span>

## <a name="appinit_dlls-and-secure-boot"></a><span data-ttu-id="cca5d-110">AppInit \_ dll 和安全開機</span><span class="sxs-lookup"><span data-stu-id="cca5d-110">AppInit\_DLLs and secure boot</span></span>

<span data-ttu-id="cca5d-111">Windows 8 採用 UEFI 和安全開機來改善整體系統完整性，並為複雜的威脅提供強式保護。</span><span class="sxs-lookup"><span data-stu-id="cca5d-111">Windows 8 adopted UEFI and secure boot to improve the overall system integrity and to provide strong protection against sophisticated threats.</span></span> <span data-ttu-id="cca5d-112">啟用安全開機時， \_ 會停用 AppInit dll 機制，以保護客戶免于惡意程式碼和威脅的侵害。</span><span class="sxs-lookup"><span data-stu-id="cca5d-112">When secure boot is enabled, the AppInit\_DLLs mechanism is disabled as part of a no-compromise approach to protect customers against malware and threats.</span></span>

<span data-ttu-id="cca5d-113">請注意，安全開機是 UEFI 通訊協定，而不是 Windows 8 功能。</span><span class="sxs-lookup"><span data-stu-id="cca5d-113">Please note that secure boot is a UEFI protocol and not a Windows 8 feature.</span></span> <span data-ttu-id="cca5d-114">如需 UEFI 和安全開機通訊協定規格的詳細資訊，請參閱 [https://www.uefi.org](https://www.uefi.org/) 。</span><span class="sxs-lookup"><span data-stu-id="cca5d-114">More info on UEFI and the secure boot protocol specification can be found at [https://www.uefi.org](https://www.uefi.org/).</span></span>

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a><span data-ttu-id="cca5d-115">\_Windows 8 桌面應用程式的 AppInit dll 認證需求</span><span class="sxs-lookup"><span data-stu-id="cca5d-115">AppInit\_DLLs certification requirement for Windows 8 desktop apps</span></span>

<span data-ttu-id="cca5d-116">Windows 8 傳統型應用程式的其中一項認證需求是，應用程式不能載入任意 Dll 來攔截使用 AppInit dll 機制的 WIN32 API 呼叫 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cca5d-116">One of the certification requirements for Windows 8 desktop apps is that the app must not load arbitrary DLLs to intercept Win32 API calls using the AppInit\_DLLs mechanism.</span></span> <span data-ttu-id="cca5d-117">如需有關認證需求的詳細資訊，請參閱 [Windows 8 傳統型應用程式的認證需求](../win_cert/certification-requirements-for-windows-desktop-apps.md)1.1 一節。</span><span class="sxs-lookup"><span data-stu-id="cca5d-117">For more detailed information about the certification requirements, refer to section 1.1 of [Certification requirements for Windows 8 desktop apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).</span></span>

## <a name="summary"></a><span data-ttu-id="cca5d-118">總結</span><span class="sxs-lookup"><span data-stu-id="cca5d-118">Summary</span></span>

-   <span data-ttu-id="cca5d-119">AppInit \_ dll 機制不是合法應用程式的建議方法，因為它可能會導致系統鎖死和效能問題。</span><span class="sxs-lookup"><span data-stu-id="cca5d-119">The AppInit\_DLLs mechanism is not a recommended approach for legitimate applications because it can lead to system deadlocks and performance problems.</span></span>
-   <span data-ttu-id="cca5d-120">\_啟用安全開機時，預設會停用 AppInit dll 機制。</span><span class="sxs-lookup"><span data-stu-id="cca5d-120">The AppInit\_DLLs mechanism is disabled by default when secure boot is enabled.</span></span>
-   <span data-ttu-id="cca5d-121">\_在 Windows 8 desktop 應用程式中使用 AppInit dll 是 Windows 桌面應用程式認證失敗。</span><span class="sxs-lookup"><span data-stu-id="cca5d-121">Using AppInit\_DLLs in a Windows 8 desktop app is a Windows desktop app certification failure.</span></span>

<span data-ttu-id="cca5d-122">請參閱下列白皮書，以取得有關 2008 Windows 7 和 windows server \_ [2008 r2 中](/previous-versions/windows/hardware/download/dn550976(v=vs.85))的 AppInit dll 的詳細資訊： AppInit dll。</span><span class="sxs-lookup"><span data-stu-id="cca5d-122">See the following whitepaper for info about AppInit\_DLLs on Windows 7 and Windows Server 2008 R2: [AppInit DLLs in Windows 7 and Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).</span></span>

 

 
