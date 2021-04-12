---
description: 經過一段時間，可能會產生不同版本的 TAPI、應用程式和服務提供者。
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: TAPI 版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8565eb6282fd124c4f43e56d121ba7c053143683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319691"
---
# <a name="tapi-versioning"></a><span data-ttu-id="7dda1-103">TAPI 版本控制</span><span class="sxs-lookup"><span data-stu-id="7dda1-103">TAPI Versioning</span></span>

<span data-ttu-id="7dda1-104">經過一段時間，可能會產生不同版本的 TAPI、應用程式和服務提供者。</span><span class="sxs-lookup"><span data-stu-id="7dda1-104">Over time, different versions of TAPI, applications, and service providers may be produced.</span></span> <span data-ttu-id="7dda1-105">這些新版本可以建立新的定義，例如新功能、資料結構中的新成員，以及新的位欄位。</span><span class="sxs-lookup"><span data-stu-id="7dda1-105">These new versions can make new definitions, such as for new features, new members in data structures, and new bit fields.</span></span> <span data-ttu-id="7dda1-106">因此需要版本號碼來指出如何解讀各種資料結構。</span><span class="sxs-lookup"><span data-stu-id="7dda1-106">Version numbers are therefore necessary to indicate how to interpret various data structures.</span></span>

<span data-ttu-id="7dda1-107">為了讓不同的應用程式版本、TAPI 本身的版本，以及不同廠商的服務提供者版本獲得最佳互通性，Microsoft 電話語音為應用程式提供了一個簡單的版本協商機制。</span><span class="sxs-lookup"><span data-stu-id="7dda1-107">To allow optimal interoperability of different versions of applications, versions of TAPI itself, and versions of service providers by different vendors, Microsoft Telephony provides a simple version negotiation mechanism for applications.</span></span> <span data-ttu-id="7dda1-108">有兩個不同的版本，TAPI 和電話語音服務提供者必須針對每一行裝置同意。</span><span class="sxs-lookup"><span data-stu-id="7dda1-108">There are two different versions that TAPI and the telephony service provider need to agree on for each line device.</span></span> <span data-ttu-id="7dda1-109">第一個是與 TAPI 協商的版本，以及電話語音服務提供者 (TSP) 基本和補充電話語音，稱為 TAPI 介面版本。</span><span class="sxs-lookup"><span data-stu-id="7dda1-109">The first is the version negotiated with TAPI and the telephony service provider (TSP) Basic and Supplementary Telephony, referred to as the TAPI interface version.</span></span> <span data-ttu-id="7dda1-110">另一個則適用于提供者專屬的延伸模組（如果有的話），而且稱為延伸模組版本。</span><span class="sxs-lookup"><span data-stu-id="7dda1-110">The other is for provider-specific extensions, if any, and is referred to as the extension version.</span></span> <span data-ttu-id="7dda1-111">TAPI 的基本和增補功能所使用的資料結構和資料類型的格式是由 TAPI 版本所定義，而延伸模組版本則決定由供應商專屬的延伸模組所定義的資料結構格式。</span><span class="sxs-lookup"><span data-stu-id="7dda1-111">The format of the data structures and data types used by TAPI's Basic and Supplementary features is defined by the TAPI version, while the extension version determines the format of data structures defined by the vendor-specific extensions.</span></span>

<span data-ttu-id="7dda1-112">[**LineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)函式會協商 TAPI 版本，而 [**LINENEGOTIATEEXTVERSION**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)會協商 TSP 延伸模組版本。</span><span class="sxs-lookup"><span data-stu-id="7dda1-112">The [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) function negotiates a TAPI version and [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negotiates the TSP extension version.</span></span> <span data-ttu-id="7dda1-113">單一 TSP 可以處理一個以上的版本，而如果使用較舊的 TSP，應用程式必須「切換回」使用較舊的版本。</span><span class="sxs-lookup"><span data-stu-id="7dda1-113">A single TSP could be capable of handling more than one version, and an application must "fall back" to using an older version if using an older TSP.</span></span> <span data-ttu-id="7dda1-114">在 **lineNegotiateAPIVersion** 中， *dwApiVersion* 參數預設為根據版本的值，如下所示。</span><span class="sxs-lookup"><span data-stu-id="7dda1-114">In **lineNegotiateAPIVersion** the *dwApiVersion* parameter defaults to a value according to version, as follows.</span></span>



| <span data-ttu-id="7dda1-115">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="7dda1-115">TAPI version</span></span> | <span data-ttu-id="7dda1-116">預設值</span><span class="sxs-lookup"><span data-stu-id="7dda1-116">Default value</span></span> |
|--------------|---------------|
| <span data-ttu-id="7dda1-117">1.3</span><span class="sxs-lookup"><span data-stu-id="7dda1-117">1.3</span></span>          | <span data-ttu-id="7dda1-118">0x00010003</span><span class="sxs-lookup"><span data-stu-id="7dda1-118">0x00010003</span></span>    |
| <span data-ttu-id="7dda1-119">1.4</span><span class="sxs-lookup"><span data-stu-id="7dda1-119">1.4</span></span>          | <span data-ttu-id="7dda1-120">0x00010004</span><span class="sxs-lookup"><span data-stu-id="7dda1-120">0x00010004</span></span>    |
| <span data-ttu-id="7dda1-121">2.0</span><span class="sxs-lookup"><span data-stu-id="7dda1-121">2.0</span></span>          | <span data-ttu-id="7dda1-122">0x00020000</span><span class="sxs-lookup"><span data-stu-id="7dda1-122">0x00020000</span></span>    |
| <span data-ttu-id="7dda1-123">2.1</span><span class="sxs-lookup"><span data-stu-id="7dda1-123">2.1</span></span>          | <span data-ttu-id="7dda1-124">0x00020001</span><span class="sxs-lookup"><span data-stu-id="7dda1-124">0x00020001</span></span>    |
| <span data-ttu-id="7dda1-125">2.2</span><span class="sxs-lookup"><span data-stu-id="7dda1-125">2.2</span></span>          | <span data-ttu-id="7dda1-126">0x00020002</span><span class="sxs-lookup"><span data-stu-id="7dda1-126">0x00020002</span></span>    |



 

<span data-ttu-id="7dda1-127">但是，只要 TSP 本身使用的是比應用程式更新的版本，TAPI 就能讓這項作業更容易。</span><span class="sxs-lookup"><span data-stu-id="7dda1-127">However, TAPI makes this much easier as long as the TSP itself is using a newer version than the application.</span></span> <span data-ttu-id="7dda1-128">如果 TSP 的確很新，則 TAPI 能夠將 "down" 轉譯為應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="7dda1-128">If the TSP is indeed newer, then TAPI is capable of translating "down" to the application's version.</span></span> <span data-ttu-id="7dda1-129">例如，TAPI 2.0 Tsp 不需要特別能夠處理 TAPI 1.4 版。</span><span class="sxs-lookup"><span data-stu-id="7dda1-129">For example, TAPI 2.0 TSPs do not need to be specifically capable of dealing with TAPI version 1.4.</span></span> <span data-ttu-id="7dda1-130">如果執行 TAPI 1.4 應用程式，TAPI 會將所有 TAPI 2.0 結構和訊息轉換成 TAPI 1.4 對等專案，或盡可能接近。</span><span class="sxs-lookup"><span data-stu-id="7dda1-130">If a TAPI 1.4 application is run, TAPI converts all TAPI 2.0 structures and messages into TAPI 1.4 equivalents, or as close as possible.</span></span> <span data-ttu-id="7dda1-131">如果 TAPI 1.4 中沒有接近近似值，則所有 TAPI 2.0 特定的資訊都將遺失。</span><span class="sxs-lookup"><span data-stu-id="7dda1-131">If there is no close approximation in TAPI 1.4, then all TAPI 2.0-specific information will be lost.</span></span>

<span data-ttu-id="7dda1-132">延伸模組版本的精確意義是提供者特有的。</span><span class="sxs-lookup"><span data-stu-id="7dda1-132">The precise meaning of an extension version is provider-specific.</span></span> <span data-ttu-id="7dda1-133">若要使用支援擴充功能的 TSP，請參閱提供者的檔。</span><span class="sxs-lookup"><span data-stu-id="7dda1-133">To use a TSP that supports extensions, consult the provider's documentation.</span></span>

<span data-ttu-id="7dda1-134">TAPI 有許多版本。</span><span class="sxs-lookup"><span data-stu-id="7dda1-134">There are a number of versions of TAPI.</span></span> <span data-ttu-id="7dda1-135">雖然這些版本大多涉及變更 TAPI 和電話語音服務提供者介面 (TSPI) 檔集，但每個版本都有其他含意，也就是架構差異、作業系統變化、可轉散發套件和 TSP 開發問題。</span><span class="sxs-lookup"><span data-stu-id="7dda1-135">While most of these versions involved changes to the TAPI and Telephony Service Provider Interface (TSPI) documentation sets, there are other implications for each version, namely, architectural differences, operating system variations, redistributables, and TSP development issues.</span></span>



| <span data-ttu-id="7dda1-136">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="7dda1-136">TAPI version</span></span>        | <span data-ttu-id="7dda1-137">散發</span><span class="sxs-lookup"><span data-stu-id="7dda1-137">Distribution</span></span>                                                   |
|---------------------|----------------------------------------------------------------|
| <span data-ttu-id="7dda1-138">1.0 –1。2</span><span class="sxs-lookup"><span data-stu-id="7dda1-138">1.0 – 1.2</span></span>           | <span data-ttu-id="7dda1-139">不應再使用的 Beta 版。</span><span class="sxs-lookup"><span data-stu-id="7dda1-139">Beta versions that should not be used any longer.</span></span>              |
| [<span data-ttu-id="7dda1-140">1.4</span><span class="sxs-lookup"><span data-stu-id="7dda1-140">1.4</span></span>](tapi-1-4.md) | <span data-ttu-id="7dda1-141">包含在 Windows 95 中。</span><span class="sxs-lookup"><span data-stu-id="7dda1-141">Included in Windows 95.</span></span>                                        |
| [<span data-ttu-id="7dda1-142">1.5</span><span class="sxs-lookup"><span data-stu-id="7dda1-142">1.5</span></span>](tapi-1-5.md) | <span data-ttu-id="7dda1-143">隨附于 Windows CE 1.0。</span><span class="sxs-lookup"><span data-stu-id="7dda1-143">Included in Windows CE 1.0.</span></span>                                    |
| [<span data-ttu-id="7dda1-144">2.0</span><span class="sxs-lookup"><span data-stu-id="7dda1-144">2.0</span></span>](tapi-2-0.md) | <span data-ttu-id="7dda1-145">隨附于 Windows NT 4.0 SP3。</span><span class="sxs-lookup"><span data-stu-id="7dda1-145">Included in Windows NT 4.0 with SP3.</span></span>                           |
| [<span data-ttu-id="7dda1-146">2.1</span><span class="sxs-lookup"><span data-stu-id="7dda1-146">2.1</span></span>](tapi-2-1.md) | <span data-ttu-id="7dda1-147">隨附于 Windows NT 4.0 與 SP4 和 Windows 98。</span><span class="sxs-lookup"><span data-stu-id="7dda1-147">Included in Windows NT 4.0 with SP4 and Windows 98.</span></span>            |
| [<span data-ttu-id="7dda1-148">2.2</span><span class="sxs-lookup"><span data-stu-id="7dda1-148">2.2</span></span>](tapi-2-2.md) | <span data-ttu-id="7dda1-149">包含在 Windows Server 2003、Windows XP 及 Windows 2000 中。</span><span class="sxs-lookup"><span data-stu-id="7dda1-149">Included in Windows Server 2003, Windows XP, and Windows 2000.</span></span> |



 

 

 



