---
description: 地區設定 \_ ICONSTRUCTEDLOCALE 常數描述
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/30/2021
ms.locfileid: "107001248"
---
# <a name="locale_iconstructedlocale"></a><span data-ttu-id="cb708-103">地區設定 \_ ICONSTRUCTEDLOCALE</span><span class="sxs-lookup"><span data-stu-id="cb708-103">LOCALE\_ICONSTRUCTEDLOCALE</span></span>

<span data-ttu-id="cb708-104">如果地區設定是「已建立」地區設定，則為要求的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb708-104">Identifier to request if the locale is a "constructed" locale.</span></span> <span data-ttu-id="cb708-105">不建議使用此 LCTYPE。</span><span class="sxs-lookup"><span data-stu-id="cb708-105">Use of this LCTYPE is discouraged.</span></span>

<span data-ttu-id="cb708-106">這會識別 Windows 上有許多沒有完整資訊的地區設定，而且必須在執行時間「建立」資訊。</span><span class="sxs-lookup"><span data-stu-id="cb708-106">This identifies a locale for which Windows many not have complete information and has to "construct" information at runtime.</span></span> <span data-ttu-id="cb708-107">一般來說，LOCALE_ICONSTRUCTEDLOCALE 提供的資訊有限，因為 Windows 會提供每個地區設定所能使用的資料量。</span><span class="sxs-lookup"><span data-stu-id="cb708-107">Typically the information provided by LOCALE_ICONSTRUCTEDLOCALE is of limited use as Windows will provide as much data as is available for every locale.</span></span> <span data-ttu-id="cb708-108">因此，不建議使用此 LCTYPE。</span><span class="sxs-lookup"><span data-stu-id="cb708-108">Therefore, use of this LCTYPE is discouraged.</span></span>


| <span data-ttu-id="cb708-109">值</span><span class="sxs-lookup"><span data-stu-id="cb708-109">Value</span></span> | <span data-ttu-id="cb708-110">意義</span><span class="sxs-lookup"><span data-stu-id="cb708-110">Meaning</span></span>                 |
|-------|-------------------------|
| <span data-ttu-id="cb708-111">0</span><span class="sxs-lookup"><span data-stu-id="cb708-111">0</span></span>     | <span data-ttu-id="cb708-112">未結構化</span><span class="sxs-lookup"><span data-stu-id="cb708-112">Not constructed</span></span>         |
| <span data-ttu-id="cb708-113">1</span><span class="sxs-lookup"><span data-stu-id="cb708-113">1</span></span>     | <span data-ttu-id="cb708-114">是一種結構化的地區設定</span><span class="sxs-lookup"><span data-stu-id="cb708-114">Is a constructed locale</span></span> |


<span data-ttu-id="cb708-115">例如，「de US」或「美國德文」的要求。</span><span class="sxs-lookup"><span data-stu-id="cb708-115">An example would be a request for "de-US", or German in the United States.</span></span> <span data-ttu-id="cb708-116">NLS 將使用可找到的德文語言資料，以及可找到的美國地區資料。</span><span class="sxs-lookup"><span data-stu-id="cb708-116">NLS will use the German language data that it can find and the United States region data that it can find.</span></span> 

<span data-ttu-id="cb708-117">這可能不是最理想的，例如，系統可能沒有德文中美國名稱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb708-117">This may not be perfect as, for example, the system will likely not have information about the name of United States in German.</span></span> <span data-ttu-id="cb708-118">但是，如果應用程式或使用者想要「de US」內容，則傳回的資料會是最佳的可用資料。</span><span class="sxs-lookup"><span data-stu-id="cb708-118">However, if the application or user desires a "de-US" context, then the returned data is the best available.</span></span> 

<span data-ttu-id="cb708-119">使用 LOCALE_ICONSTRUCTEDLOCALE 拒絕地區設定並切換回不同地區設定的應用程式，通常會產生較糟的體驗，例如在此範例中登陸或 en-us。</span><span class="sxs-lookup"><span data-stu-id="cb708-119">Apps that use LOCALE_ICONSTRUCTEDLOCALE to reject locales and fall back to a different locale typically end up with a worse experience, such as landing on de-DE or en-US in this example.</span></span> <span data-ttu-id="cb708-120">這兩種方式都不會接近德國語言的原始要求（美國地區）。</span><span class="sxs-lookup"><span data-stu-id="cb708-120">Neither of those are close to the original request for German language with a United States region.</span></span>

