---
description: 地區設定 \_ SNATIVE \* 常數
ms.assetid: 560978d7-a33c-4e62-9abd-cbd3ec38f3b5
title: LOCALE_SNATIVE * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaa6942b6ed114e6cbabdb48ae55ba8f8d7bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195441"
---
# <a name="locale_snative-constants"></a><span data-ttu-id="62031-103">地區設定 \_ SNATIVE \* 常數</span><span class="sxs-lookup"><span data-stu-id="62031-103">LOCALE\_SNATIVE\* Constants</span></span>

<span data-ttu-id="62031-104">本主題定義 \_ \* NLS 用來代表原生語言名稱的地區設定 SNATIVE 常數。</span><span class="sxs-lookup"><span data-stu-id="62031-104">This topic defines the LOCALE\_SNATIVE\* constants used by NLS to represent native language names.</span></span>



| <span data-ttu-id="62031-105">值</span><span class="sxs-lookup"><span data-stu-id="62031-105">Value</span></span>                       | <span data-ttu-id="62031-106">意義</span><span class="sxs-lookup"><span data-stu-id="62031-106">Meaning</span></span>                                                                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62031-107">地區設定 \_ SNATIVECOUNTRYNAME</span><span class="sxs-lookup"><span data-stu-id="62031-107">LOCALE\_SNATIVECOUNTRYNAME</span></span>  | <span data-ttu-id="62031-108">**Windows 7 和更新版本：** 國家/地區的原生名稱，例如，España，西班牙。</span><span class="sxs-lookup"><span data-stu-id="62031-108">**Windows 7 and later:** Native name of the country/region, for example, España for Spain.</span></span> <span data-ttu-id="62031-109">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="62031-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>                                                                 |
| <span data-ttu-id="62031-110">地區設定 \_ SNATIVECTRYNAME</span><span class="sxs-lookup"><span data-stu-id="62031-110">LOCALE\_SNATIVECTRYNAME</span></span>     | <span data-ttu-id="62031-111">適用于 Windows 7 和更新版本的已淘汰。</span><span class="sxs-lookup"><span data-stu-id="62031-111">Deprecated for Windows 7 and later.</span></span> <span data-ttu-id="62031-112">國家/地區的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="62031-112">Native name of the country/region.</span></span> <span data-ttu-id="62031-113">請參閱地區設定 \_ SNATIVECOUNTRYNAME。</span><span class="sxs-lookup"><span data-stu-id="62031-113">See LOCALE\_SNATIVECOUNTRYNAME.</span></span>                                                                                                                                                             |
| <span data-ttu-id="62031-114">地區設定 \_ SNATIVECURRNAME</span><span class="sxs-lookup"><span data-stu-id="62031-114">LOCALE\_SNATIVECURRNAME</span></span>     | <span data-ttu-id="62031-115">**Windows Me/98、windows 2000：** 與地區設定相關聯之貨幣的原生名稱（以地區設定的原生語言）。</span><span class="sxs-lookup"><span data-stu-id="62031-115">**Windows Me/98, Windows 2000:** The native name of the currency associated with the locale, in the native language of the locale.</span></span> <span data-ttu-id="62031-116">此字串允許的字元數沒有限制。</span><span class="sxs-lookup"><span data-stu-id="62031-116">There is no limit on the number of characters allowed for this string.</span></span>                                                          |
| <span data-ttu-id="62031-117">地區設定 \_ SNATIVEDIGITS</span><span class="sxs-lookup"><span data-stu-id="62031-117">LOCALE\_SNATIVEDIGITS</span></span>       | <span data-ttu-id="62031-118">ASCII 0 到9的原生對等專案。</span><span class="sxs-lookup"><span data-stu-id="62031-118">Native equivalents of ASCII 0 through 9.</span></span> <span data-ttu-id="62031-119">此字串允許的最大字元數為十個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="62031-119">The maximum number of characters allowed for this string is eleven, including a terminating null character.</span></span> <span data-ttu-id="62031-120">例如，阿拉伯文會使用 "012345 6789"。</span><span class="sxs-lookup"><span data-stu-id="62031-120">For example, Arabic uses "٠١٢٣٤٥ ٦٧٨٩".</span></span> <span data-ttu-id="62031-121">另請參閱 [地區設定 \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md)。</span><span class="sxs-lookup"><span data-stu-id="62031-121">See also [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md).</span></span> |
| <span data-ttu-id="62031-122">地區設定 \_ SNATIVEDISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="62031-122">LOCALE\_SNATIVEDISPLAYNAME</span></span>  | <span data-ttu-id="62031-123">**Windows 7 和更新版本：** 以原生語言顯示地區設定的名稱，例如，Deutsch (Deutschland) 適用于地區設定德文 (德國) 。</span><span class="sxs-lookup"><span data-stu-id="62031-123">**Windows 7 and later:** Display name of the locale in its native language, for example, Deutsch (Deutschland) for the locale German (Germany).</span></span> <br/>                                                                                                        |
| <span data-ttu-id="62031-124">地區設定 \_ SNATIVELANGNAME</span><span class="sxs-lookup"><span data-stu-id="62031-124">LOCALE\_SNATIVELANGNAME</span></span>     | <span data-ttu-id="62031-125">適用于 Windows 7 和更新版本的已淘汰。</span><span class="sxs-lookup"><span data-stu-id="62031-125">Deprecated for Windows 7 and later.</span></span> <span data-ttu-id="62031-126">語言的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="62031-126">Native name of the language.</span></span> <span data-ttu-id="62031-127">請參閱地區設定 \_ SNATIVELANGUAGENAME。</span><span class="sxs-lookup"><span data-stu-id="62031-127">See LOCALE\_SNATIVELANGUAGENAME.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="62031-128">地區設定 \_ SNATIVELANGUAGENAME</span><span class="sxs-lookup"><span data-stu-id="62031-128">LOCALE\_SNATIVELANGUAGENAME</span></span> | <span data-ttu-id="62031-129">**Windows 7 和更新版本：** 語言的原生名稱，例如 (亞美尼亞) 的亞美尼亞文Հայերեն。</span><span class="sxs-lookup"><span data-stu-id="62031-129">**Windows 7 and later:** Native name of the language, for example, Հայերեն for Armenian (Armenia).</span></span> <span data-ttu-id="62031-130">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="62031-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>                                                         |



 

 

 




