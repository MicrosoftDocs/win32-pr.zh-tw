---
description: 設定 [每個使用者的系統原則] 會指定安裝程式搜尋三種來源類型的順序。
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852931"
---
# <a name="searchorder"></a><span data-ttu-id="b5505-103">SearchOrder</span><span class="sxs-lookup"><span data-stu-id="b5505-103">SearchOrder</span></span>

<span data-ttu-id="b5505-104">設定 [每個使用者的 [系統原則](system-policy.md) ] 會指定安裝程式搜尋三種來源類型的順序。</span><span class="sxs-lookup"><span data-stu-id="b5505-104">Setting this per-user [system policy](system-policy.md) specifies the order in which the installer searches three types of sources.</span></span> <span data-ttu-id="b5505-105">來源的類型為：</span><span class="sxs-lookup"><span data-stu-id="b5505-105">The types of sources are:</span></span>

<span data-ttu-id="b5505-106">"n" –網路</span><span class="sxs-lookup"><span data-stu-id="b5505-106">"n" – network</span></span>

<span data-ttu-id="b5505-107">"m" –媒體 (CD-ROM 或 DVD) </span><span class="sxs-lookup"><span data-stu-id="b5505-107">"m" – media (CD-ROM or DVD)</span></span>

<span data-ttu-id="b5505-108">"u" –統一資源定位器 (URL) </span><span class="sxs-lookup"><span data-stu-id="b5505-108">"u" – Uniform Resource Locator (URL)</span></span>

<span data-ttu-id="b5505-109">例如，若要先搜尋網路來源、媒體來源第二個和 URL 來源，最後將此原則設定為 "nmu" 值。</span><span class="sxs-lookup"><span data-stu-id="b5505-109">For example, to search network sources first, media sources second, and URL sources last set this policy to a value of "nmu".</span></span> <span data-ttu-id="b5505-110">若要省略搜尋特定來源類型，請從值中省略對應的字母。</span><span class="sxs-lookup"><span data-stu-id="b5505-110">To omit searching for a particular source type, leave out the corresponding letter from the value.</span></span>

<span data-ttu-id="b5505-111">如果未設定 SearchOrder，則預設搜尋順序為 [網路]、[媒體] 和 [URL]。</span><span class="sxs-lookup"><span data-stu-id="b5505-111">If SearchOrder is not set, the default search order is network, media, and then URL.</span></span>

## <a name="registry-key"></a><span data-ttu-id="b5505-112">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="b5505-112">Registry Key</span></span>

<span data-ttu-id="b5505-113">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="b5505-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="b5505-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="b5505-114">Data Type</span></span>

<span data-ttu-id="b5505-115">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b5505-115">**REG\_SZ**</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5505-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5505-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5505-117">來源復原</span><span class="sxs-lookup"><span data-stu-id="b5505-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



