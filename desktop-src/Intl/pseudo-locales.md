---
description: Windows Vista 和更新版本： NLS 除了現有的 Windows 地區設定之外，還定義了數個虛擬地區設定來使用。
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974025"
---
# <a name="pseudo-locales"></a><span data-ttu-id="d8caa-103">Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="d8caa-103">Pseudo-Locales</span></span>

<span data-ttu-id="d8caa-104">**Windows Vista 和更新版本：** NLS 除了現有的 Windows 地區設定之外，還定義了數個虛擬地區設定。</span><span class="sxs-lookup"><span data-stu-id="d8caa-104">**Windows Vista and later:** NLS defines several pseudo-locales for use in addition to the existing Windows locales.</span></span> <span data-ttu-id="d8caa-105">使用這些虛擬地區設定來測試應用程式的當地語系化。</span><span class="sxs-lookup"><span data-stu-id="d8caa-105">Use these pseudo-locales for testing the localization of your applications.</span></span> <span data-ttu-id="d8caa-106">如需執行的詳細資訊，請參閱 [使用 Pseudo-Locales 進行當地語系化測試](using-pseudo-locales-for-localization-testing.md)。</span><span class="sxs-lookup"><span data-stu-id="d8caa-106">For implementation details, see [Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).</span></span>

## <a name="supported-pseudo-locales"></a><span data-ttu-id="d8caa-107">支援的 Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="d8caa-107">Supported Pseudo-Locales</span></span>

<span data-ttu-id="d8caa-108">NLS 支援的虛擬地區設定如下：</span><span class="sxs-lookup"><span data-stu-id="d8caa-108">The pseudo-locales supported by NLS are:</span></span>

-   <span data-ttu-id="d8caa-109">基底虛擬-地區設定</span><span class="sxs-lookup"><span data-stu-id="d8caa-109">Base pseudo-locale</span></span>
-   <span data-ttu-id="d8caa-110">鏡像 (由右至左) 虛擬地區設定</span><span class="sxs-lookup"><span data-stu-id="d8caa-110">Mirrored (right-to-left) pseudo-locale</span></span>
-   <span data-ttu-id="d8caa-111">東亞語言虛擬-地區設定</span><span class="sxs-lookup"><span data-stu-id="d8caa-111">East Asian-language pseudo-locale</span></span>

<span data-ttu-id="d8caa-112">根據其字碼頁指派和當地語系化的字串（例如月份名稱、日期名稱），選擇要使用的特定虛擬地區設定。</span><span class="sxs-lookup"><span data-stu-id="d8caa-112">Choose the particular pseudo-locale to use based on its code page assignments and the strings for localization, for example, month names, day names.</span></span> <span data-ttu-id="d8caa-113">每個虛擬地區設定的資料，不僅包含相關的字碼頁，也包括用於當地語系化的日期和月份字串，也包含其他數個 NLS 測試案例的資料。</span><span class="sxs-lookup"><span data-stu-id="d8caa-113">Data for each pseudo-locale includes not only relevant code pages and day and month strings for localization, but also data for several other test cases for NLS.</span></span> <span data-ttu-id="d8caa-114">測試案例會檢查下列資料類型：</span><span class="sxs-lookup"><span data-stu-id="d8caa-114">The test cases examine the following types of data:</span></span>

-   <span data-ttu-id="d8caa-115">9位 [地區設定識別碼](locale-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="d8caa-115">9-bit [locale identifiers](locale-identifiers.md).</span></span> <span data-ttu-id="d8caa-116">虛擬地區設定可讓您更有效地測試9位地區設定識別碼的操作。</span><span class="sxs-lookup"><span data-stu-id="d8caa-116">Pseudo-locales provide a good opportunity to test the operation of 9-bit locale identifiers.</span></span>
-   <span data-ttu-id="d8caa-117">需要使用小型字型的語言字串。</span><span class="sxs-lookup"><span data-stu-id="d8caa-117">Strings from languages that must use small fonts.</span></span> <span data-ttu-id="d8caa-118">由於圖形裝置介面 (GDI) 的限制，某些語言的使用者介面字型小於最佳。</span><span class="sxs-lookup"><span data-stu-id="d8caa-118">Because of limitations in the graphics device interface (GDI), the user interface font for some languages is smaller than optimal.</span></span> <span data-ttu-id="d8caa-119">虛擬地區設定包含這些語言中的數個字串，並結合了具有更標準字型處理語言的字串。</span><span class="sxs-lookup"><span data-stu-id="d8caa-119">Pseudo-locales include several strings from these languages, combined with strings from languages with more standard font handling.</span></span> <span data-ttu-id="d8caa-120">您可以在測試中使用這些字串來判斷如何轉譯受 GDI 限制的字型。</span><span class="sxs-lookup"><span data-stu-id="d8caa-120">You can use these strings in testing to determine how a GDI-limited font renders.</span></span>
-   <span data-ttu-id="d8caa-121">不尋常的字串長度。</span><span class="sxs-lookup"><span data-stu-id="d8caa-121">Unusual string lengths.</span></span> <span data-ttu-id="d8caa-122">某些地區設定資訊常數（例如， [地區設定 \_ SLIST](locale-slist.md) 和 [地區設定 \_ ICURRENCY](locale-icurrency.md)）具有字串大小的傳統限制。</span><span class="sxs-lookup"><span data-stu-id="d8caa-122">Some locale information constants, for example, [LOCALE\_SLIST](locale-slist.md) and [LOCALE\_ICURRENCY](locale-icurrency.md), have conventional limits on string size.</span></span> <span data-ttu-id="d8caa-123">虛擬地區設定支援不同字串長度的檢查。</span><span class="sxs-lookup"><span data-stu-id="d8caa-123">The pseudo-locales support the examination of varied string lengths.</span></span>
-   <span data-ttu-id="d8caa-124">替代排序。</span><span class="sxs-lookup"><span data-stu-id="d8caa-124">Alternate sorts.</span></span> <span data-ttu-id="d8caa-125">當替代 [排序次序識別碼](sort-order-identifiers.md) 與通常與地區設定相關聯的基底排序次序識別碼不同時，可以使用虛擬地區設定來測試替代排序功能。</span><span class="sxs-lookup"><span data-stu-id="d8caa-125">Pseudo-locales can be used to test alternate sort functionality when the alternate [sort order identifier](sort-order-identifiers.md) differs from the base sort order identifier that is usually associated with the locale.</span></span>

## <a name="pseudo-locale-names-and-identifiers"></a><span data-ttu-id="d8caa-126">虛擬地區設定名稱和識別碼</span><span class="sxs-lookup"><span data-stu-id="d8caa-126">Pseudo-locale Names and Identifiers</span></span>

<span data-ttu-id="d8caa-127">虛擬地區設定具有從私用空間選擇的 [地區設定名稱](locale-names.md) ，以避免與國際標準組織中引入的可能字串 (ISO) 639 和 iso 3166 標準發生衝突。</span><span class="sxs-lookup"><span data-stu-id="d8caa-127">The pseudo-locales have [locale names](locale-names.md) that are chosen from the private use space to avoid conflict with possible strings introduced into the International Organization for Standardization (ISO) 639 and ISO 3166 standards.</span></span> <span data-ttu-id="d8caa-128">每個虛擬地區設定也都有自己的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8caa-128">Each pseudo-locale also has its own locale identifier.</span></span> <span data-ttu-id="d8caa-129">下表提供所定義虛擬地區設定的名稱和識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8caa-129">The following table provides the names and identifiers for the defined pseudo-locales.</span></span>



| <span data-ttu-id="d8caa-130">虛擬地區設定</span><span class="sxs-lookup"><span data-stu-id="d8caa-130">Pseudo-locale</span></span>       | <span data-ttu-id="d8caa-131">地區設定名稱</span><span class="sxs-lookup"><span data-stu-id="d8caa-131">Locale name</span></span> | <span data-ttu-id="d8caa-132">地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="d8caa-132">Locale identifier</span></span> |
|---------------------|-------------|-------------------|
| <span data-ttu-id="d8caa-133">基本</span><span class="sxs-lookup"><span data-stu-id="d8caa-133">Base</span></span>                | <span data-ttu-id="d8caa-134">qps-qps-ploc</span><span class="sxs-lookup"><span data-stu-id="d8caa-134">qps-ploc</span></span>    | <span data-ttu-id="d8caa-135">0501</span><span class="sxs-lookup"><span data-stu-id="d8caa-135">0501</span></span>              |
| <span data-ttu-id="d8caa-136">鏡像</span><span class="sxs-lookup"><span data-stu-id="d8caa-136">Mirrored</span></span>            | <span data-ttu-id="d8caa-137">qps-plocm</span><span class="sxs-lookup"><span data-stu-id="d8caa-137">qps-plocm</span></span>   | <span data-ttu-id="d8caa-138">09ff</span><span class="sxs-lookup"><span data-stu-id="d8caa-138">09ff</span></span>              |
| <span data-ttu-id="d8caa-139">東亞語言</span><span class="sxs-lookup"><span data-stu-id="d8caa-139">East Asian-language</span></span> | <span data-ttu-id="d8caa-140">qps-ploca</span><span class="sxs-lookup"><span data-stu-id="d8caa-140">qps-ploca</span></span>   | <span data-ttu-id="d8caa-141">05fe</span><span class="sxs-lookup"><span data-stu-id="d8caa-141">05fe</span></span>              |



 

## <a name="example"></a><span data-ttu-id="d8caa-142">範例</span><span class="sxs-lookup"><span data-stu-id="d8caa-142">Example</span></span>

<span data-ttu-id="d8caa-143">下列範例會顯示針對基底虛擬地區設定顯示的文字：</span><span class="sxs-lookup"><span data-stu-id="d8caa-143">The following example shows text displayed for a base pseudo-locale:</span></span>

<span data-ttu-id="d8caa-144">\[Шěđлеśđαỳ!!! \] 、8ōf \[ Μäŕςћ！！ \] ōf 2006</span><span class="sxs-lookup"><span data-stu-id="d8caa-144">\[Шěđлеśđαỳ !!!\], 8 ōf \[Μäŕςћ !!\] ōf 2006</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8caa-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8caa-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8caa-146">地區設定和語言</span><span class="sxs-lookup"><span data-stu-id="d8caa-146">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="d8caa-147">地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="d8caa-147">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="d8caa-148">地區設定名稱</span><span class="sxs-lookup"><span data-stu-id="d8caa-148">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="d8caa-149">排序次序識別碼</span><span class="sxs-lookup"><span data-stu-id="d8caa-149">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="d8caa-150">使用 Pseudo-Locales 進行當地語系化測試</span><span class="sxs-lookup"><span data-stu-id="d8caa-150">Using Pseudo-Locales for Localization Testing</span></span>](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



