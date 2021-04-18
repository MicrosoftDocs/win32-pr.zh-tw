---
title: 初始、中詞和最終搜尋字串
description: 在檔中，有三種類型的萬用字元搜尋可參考結構搜尋字串查詢。 這些萬用字元搜尋為初始、中式和最後搜尋的字串。 本主題說明這些搜尋。
ms.assetid: 23cc4771-2dd6-478c-9c7a-43052594cb71
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f502753a87afc81856524c7ae5565db3af678d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965768"
---
# <a name="initial-medial-and-final-search-strings"></a><span data-ttu-id="e20dd-105">初始、中詞和最終搜尋字串</span><span class="sxs-lookup"><span data-stu-id="e20dd-105">Initial, Medial, and Final Search Strings</span></span>

<span data-ttu-id="e20dd-106">在檔中，有三種類型的萬用字元搜尋可參考結構搜尋字串查詢。</span><span class="sxs-lookup"><span data-stu-id="e20dd-106">There are three types of wildcard searches that are referenced throughout the documentation about construction search string queries.</span></span> <span data-ttu-id="e20dd-107">這些萬用字元搜尋是：初始、中的字串和最終搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="e20dd-107">These wildcard searches are: initial-, medial-, and final-search strings.</span></span> <span data-ttu-id="e20dd-108">本主題說明這些搜尋。</span><span class="sxs-lookup"><span data-stu-id="e20dd-108">This topics describes these searches.</span></span>

## <a name="initial-search-strings"></a><span data-ttu-id="e20dd-109">初始搜尋字串</span><span class="sxs-lookup"><span data-stu-id="e20dd-109">Initial Search Strings</span></span>

<span data-ttu-id="e20dd-110">初始搜尋字串會比對字串開頭的一組指定的字元，後面接著萬用字元。</span><span class="sxs-lookup"><span data-stu-id="e20dd-110">Initial-search strings match a given set of characters at the beginning of a string, followed by a wildcard.</span></span> <span data-ttu-id="e20dd-111">例如，初始搜尋字串 `Act*` 會符合 "Active Directory"。</span><span class="sxs-lookup"><span data-stu-id="e20dd-111">For example, the initial-search string `Act*` would match "Active Directory".</span></span>

## <a name="medial-search-strings"></a><span data-ttu-id="e20dd-112">Medial-Search 字串</span><span class="sxs-lookup"><span data-stu-id="e20dd-112">Medial-Search Strings</span></span>

<span data-ttu-id="e20dd-113">中間字元搜尋字串會比對字串中間的一組指定的字元，並在前面加上/或後面加上萬用字元。</span><span class="sxs-lookup"><span data-stu-id="e20dd-113">Medial-search strings match a given set of characters in the middle of a string, preceded by and/or followed by a wildcard.</span></span> <span data-ttu-id="e20dd-114">中間詞搜尋字串 `*Dir*` 、 `*ive*Dir*` 和 `*ve*Dir*tor*` 都會符合 "Active Directory"。</span><span class="sxs-lookup"><span data-stu-id="e20dd-114">The medial-search strings `*Dir*`, `*ive*Dir*`, and `*ve*Dir*tor*` would all match "Active Directory".</span></span>

## <a name="final-search-strings"></a><span data-ttu-id="e20dd-115">最終搜尋字串</span><span class="sxs-lookup"><span data-stu-id="e20dd-115">Final-search Strings</span></span>

<span data-ttu-id="e20dd-116">最終搜尋字串會比對字串結尾的一組指定字元，並在前面加上萬用字元。</span><span class="sxs-lookup"><span data-stu-id="e20dd-116">Final-search strings match a given set of characters at the end of a string, preceded by a wildcard.</span></span> <span data-ttu-id="e20dd-117">例如，最終搜尋字串 `*ory` 會符合 "Active Directory"。</span><span class="sxs-lookup"><span data-stu-id="e20dd-117">For example, the final-search string `*ory` would match "Active Directory".</span></span>

 

 




