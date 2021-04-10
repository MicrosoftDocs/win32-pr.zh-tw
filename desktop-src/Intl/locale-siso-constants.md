---
description: 地區設定 \_ SISO \* 常數
ms.assetid: c830e9e9-b58a-4d31-929a-ed699bc08d9f
title: LOCALE_SISO * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16a3d7583bc920daa2edc85b641f191b016bbbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944369"
---
# <a name="locale_siso-constants"></a><span data-ttu-id="0305a-103">地區設定 \_ SISO \* 常數</span><span class="sxs-lookup"><span data-stu-id="0305a-103">LOCALE\_SISO\* Constants</span></span>

<span data-ttu-id="0305a-104">本主題定義 NLS 所使用的地區設定 \_ SISO \* 常數。</span><span class="sxs-lookup"><span data-stu-id="0305a-104">This topic defines the LOCALE\_SISO\* constants used by NLS.</span></span>



| <span data-ttu-id="0305a-105">值</span><span class="sxs-lookup"><span data-stu-id="0305a-105">Value</span></span>                     | <span data-ttu-id="0305a-106">意義</span><span class="sxs-lookup"><span data-stu-id="0305a-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0305a-107">地區設定 \_ SISO3166CTRYNAME</span><span class="sxs-lookup"><span data-stu-id="0305a-107">LOCALE\_SISO3166CTRYNAME</span></span>  | <span data-ttu-id="0305a-108">**Windows Me/98，Windows NT 4.0：** 國家/地區名稱，根據 ISO 標準3166（例如美國的 "US"）。</span><span class="sxs-lookup"><span data-stu-id="0305a-108">**Windows Me/98, Windows NT 4.0:** Country/region name, based on ISO Standard 3166, such as "US" for the United States.</span></span> <span data-ttu-id="0305a-109">這也會傳回數位，例如 "029" 代表加勒比海。</span><span class="sxs-lookup"><span data-stu-id="0305a-109">This can also return a number, such as "029" for Caribbean.</span></span> <span data-ttu-id="0305a-110">此字串允許的最大字元數為九個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="0305a-110">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                                                        |
| <span data-ttu-id="0305a-111">地區設定 \_ SISO3166CTRYNAME2</span><span class="sxs-lookup"><span data-stu-id="0305a-111">LOCALE\_SISO3166CTRYNAME2</span></span> | <span data-ttu-id="0305a-112">**Windows Vista 和更新版本：** 三個字母的 ISO 區功能變數名稱稱 (ISO 3166 3-國家/地區) 的字母代碼，例如美國的 "USA"。</span><span class="sxs-lookup"><span data-stu-id="0305a-112">**Windows Vista and later:** Three-letter ISO region name (ISO 3166 three-letter code for the country/region), such as "USA" for the United States.</span></span> <span data-ttu-id="0305a-113">這也會傳回數位，例如 "029" 代表加勒比海。</span><span class="sxs-lookup"><span data-stu-id="0305a-113">This can also return a number, such as "029" for Caribbean.</span></span> <span data-ttu-id="0305a-114">此字串允許的最大字元數為九個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="0305a-114">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                            |
| <span data-ttu-id="0305a-115">地區設定 \_ SISO639LANGNAME</span><span class="sxs-lookup"><span data-stu-id="0305a-115">LOCALE\_SISO639LANGNAME</span></span>   | <span data-ttu-id="0305a-116">**Windows Me/98，Windows NT 4.0：** 完全以 ISO 標準639值為基礎之語言的縮寫名稱（以小寫形式表示，例如 "en" 代表英文）。</span><span class="sxs-lookup"><span data-stu-id="0305a-116">**Windows Me/98, Windows NT 4.0:** The abbreviated name of the language based entirely on the ISO Standard 639 values, in lowercase form, such as "en" for English.</span></span> <span data-ttu-id="0305a-117">針對沒有2個字母代碼的語言，這可以是3個字母的代碼，例如夏威夷的 "haw"。</span><span class="sxs-lookup"><span data-stu-id="0305a-117">This can be a 3-letter code for languages that don't have a 2-letter code, such as "haw" for Hawaiian.</span></span> <span data-ttu-id="0305a-118">此字串允許的最大字元數為九個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="0305a-118">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span> |
| <span data-ttu-id="0305a-119">地區設定 \_ SISO639LANGNAME2</span><span class="sxs-lookup"><span data-stu-id="0305a-119">LOCALE\_SISO639LANGNAME2</span></span>  | <span data-ttu-id="0305a-120">**Windows Vista 和更新版本：** 三個字母的 ISO 語言名稱（小寫形式） (ISO 639-2 三個字母代碼（適用于 language) ，例如 "eng" 代表英文）。</span><span class="sxs-lookup"><span data-stu-id="0305a-120">**Windows Vista and later:** Three-letter ISO language name, in lowercase form (ISO 639-2 three-letter code for the language), such as "eng" for English.</span></span> <span data-ttu-id="0305a-121">此字串允許的最大字元數為九個字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="0305a-121">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                                                                                  |



 

 

 



