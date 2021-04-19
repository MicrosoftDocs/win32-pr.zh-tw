---
description: 下列主題說明 Windows 即服務 (WaaS) 評估平臺 API 的運作方式。
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: 關於 WaaS 評定平臺
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996763"
---
# <a name="about-the-waas-assessment-platform"></a><span data-ttu-id="8c9d5-103">關於 WaaS 評定平臺</span><span class="sxs-lookup"><span data-stu-id="8c9d5-103">About the WaaS Assessment Platform</span></span>

<span data-ttu-id="8c9d5-104">下列主題說明 Windows 即服務 (WaaS) 評估平臺 API 的運作方式。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-104">The following topic describes how the Windows as a Service (WaaS) Assessment Platform API works.</span></span>

<span data-ttu-id="8c9d5-105">WaaS 評量 API 會將下列資訊提供給呼叫者：</span><span class="sxs-lookup"><span data-stu-id="8c9d5-105">The WaaS Assessment API offers the caller the following information:</span></span>

-   <span data-ttu-id="8c9d5-106">如果裝置位於最新的 Microsoft 更新。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-106">If a device is on the latest Microsoft updates.</span></span>
-   <span data-ttu-id="8c9d5-107">裝置是否已達到終止支援。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-107">Whether the device has reached end of support.</span></span>
-   <span data-ttu-id="8c9d5-108">裝置最新適用更新的發行時間。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-108">The release times for the latest applicable updates for the device.</span></span>
-   <span data-ttu-id="8c9d5-109">評量裝置不是最新狀態的原因，以及可能對裝置造成的潛在影響。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-109">An assessment of why a device is not up-to-date and the potential impact it may have on the device.</span></span>

<span data-ttu-id="8c9d5-110">WaaS 評估平臺會使用 COM API 模型，而且每天至少會自動執行一次。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-110">The WaaS Assessment Platform uses the COM API model and runs automatically at least once a day.</span></span> <span data-ttu-id="8c9d5-111">此迴圈會捕捉適用的發行資訊。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-111">This cycle catches applicable release information.</span></span> <span data-ttu-id="8c9d5-112">在快取期間，會對快取的版本資訊進行評量。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-112">During the cached period, assessments are made against the cached release information.</span></span> <span data-ttu-id="8c9d5-113">如果在快取到期時間範圍外進行呼叫，就會建立並快取並傳回新的呼叫和評量。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-113">If a call is made outside of the cache expiration window, a fresh call and assessment is made, cached, and returned.</span></span> <span data-ttu-id="8c9d5-114">進行呼叫時，WaaS 評估用戶端會將 WaaS 評量服務與裝置的屬性連線，並接收適用于裝置的資訊 dossier。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-114">When a call is made, the WaaS Assessment Client contacts the WaaS Assessment Service with the device's attributes, and receives back a dossier of information applicable to the device.</span></span> <span data-ttu-id="8c9d5-115">然後，用戶端會使用此資訊，根據它針對裝置所收集的資訊來執行評量。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-115">The client then uses this information against the information it gathers about the device to perform the assessment.</span></span>

> [!NOTE]
> <span data-ttu-id="8c9d5-116">您的程式碼必須具有系統管理員許可權，才能呼叫 Waas 評定 API。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-116">Your code must have administrator privileges to call the Waas Assessment API.</span></span> <span data-ttu-id="8c9d5-117">如需有關開發需要系統管理員許可權之應用程式的詳細資訊，請參閱 [這篇文章](../secauthz/developing-applications-that-require-administrator-privilege.md)。</span><span class="sxs-lookup"><span data-stu-id="8c9d5-117">For more details about developing applications that require administrator privileges, see [this article](../secauthz/developing-applications-that-require-administrator-privilege.md).</span></span>

 
