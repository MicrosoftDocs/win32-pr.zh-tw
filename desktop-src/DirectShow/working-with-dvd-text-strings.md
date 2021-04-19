---
description: 使用 DVD 文字字串
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: 使用 DVD 文字字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997102"
---
# <a name="working-with-dvd-text-strings"></a><span data-ttu-id="bce1a-103">使用 DVD 文字字串</span><span class="sxs-lookup"><span data-stu-id="bce1a-103">Working with DVD Text Strings</span></span>

<span data-ttu-id="bce1a-104">某些 DVD 光碟（尤其是卡拉卡拉）可能包含文字字串清單來補充影片或音訊內容。</span><span class="sxs-lookup"><span data-stu-id="bce1a-104">Some DVD discs, especially karaoke discs, might contain a list of text strings to supplement the video or audio content.</span></span> <span data-ttu-id="bce1a-105">這些文字字串包含內容的相關中繼資料，例如歌曲標題、演出者名稱、內容類型資訊等等。</span><span class="sxs-lookup"><span data-stu-id="bce1a-105">These text strings contain metadata about the content, such as song titles, artist names, genre information, and so on.</span></span> <span data-ttu-id="bce1a-106">文字字串可以存在於一種以上的語言中。</span><span class="sxs-lookup"><span data-stu-id="bce1a-106">Text strings can be present in more than one language.</span></span> <span data-ttu-id="bce1a-107">這些字串是選擇性的，而許多光碟都沒有它們。</span><span class="sxs-lookup"><span data-stu-id="bce1a-107">These strings are optional, and many discs do not have them.</span></span>

<span data-ttu-id="bce1a-108">若要從 DVD 取出文字字串，請使用 [dvd 導覽器](dvd-navigator-filter.md)所公開的 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)介面。</span><span class="sxs-lookup"><span data-stu-id="bce1a-108">To retrieve text strings from a DVD, use the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interface, which is exposed by the [DVD Navigator](dvd-navigator-filter.md).</span></span> <span data-ttu-id="bce1a-109">您實際上不需要建立 DVD 播放圖形來取出文字字串。</span><span class="sxs-lookup"><span data-stu-id="bce1a-109">You do not actually need to build a DVD playback graph to retrieve the text strings.</span></span> <span data-ttu-id="bce1a-110">您可以直接建立 DVD Navigator、設定 DVD 音量，然後呼叫相關的文字字串方法：</span><span class="sxs-lookup"><span data-stu-id="bce1a-110">You can simply create the DVD Navigator, set the DVD volume, and then call the relevant text-string methods:</span></span>



| <span data-ttu-id="bce1a-111">方法</span><span class="sxs-lookup"><span data-stu-id="bce1a-111">Method</span></span>                                                                                  | <span data-ttu-id="bce1a-112">描述</span><span class="sxs-lookup"><span data-stu-id="bce1a-112">Description</span></span>                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bce1a-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="bce1a-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | <span data-ttu-id="bce1a-114">取得包含文字字串的語言數目。</span><span class="sxs-lookup"><span data-stu-id="bce1a-114">Gets the number of languages for which there are text strings.</span></span>                                                                                                                                  |
| [<span data-ttu-id="bce1a-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span><span class="sxs-lookup"><span data-stu-id="bce1a-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | <span data-ttu-id="bce1a-116">取得一種語言之文字字串的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bce1a-116">Gets information about the text strings for one language.</span></span>                                                                                                                                       |
| [<span data-ttu-id="bce1a-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span><span class="sxs-lookup"><span data-stu-id="bce1a-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | <span data-ttu-id="bce1a-118">依索引取得指定之語言的文字字串。</span><span class="sxs-lookup"><span data-stu-id="bce1a-118">Gets a text string for a specified language, by index.</span></span>                                                                                                                                          |
| [<span data-ttu-id="bce1a-119">**IDvdInfo2::GetDVDTextStringAsNative**</span><span class="sxs-lookup"><span data-stu-id="bce1a-119">**IDvdInfo2::GetDVDTextStringAsNative**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | <span data-ttu-id="bce1a-120">取得文字字串做為原始位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="bce1a-120">Gets a text string as a raw byte array.</span></span> <span data-ttu-id="bce1a-121">如果文字字串使用 [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)不支援的字元編碼，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="bce1a-121">Use this method if the text string uses a character encoding not supported by [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span></span> |



 

<span data-ttu-id="bce1a-122">以下是取得文字字串的基本程式：</span><span class="sxs-lookup"><span data-stu-id="bce1a-122">Here is the basic procedure for getting text strings:</span></span>

1.  <span data-ttu-id="bce1a-123">呼叫 [**IDvdInfo2：： GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) ，以尋找文字字串出現的總語言數。</span><span class="sxs-lookup"><span data-stu-id="bce1a-123">Call [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) to find the total number of languages in which the text strings appear.</span></span> <span data-ttu-id="bce1a-124">如果數位為零，則表示 DVD 沒有任何文字字串。</span><span class="sxs-lookup"><span data-stu-id="bce1a-124">If the number is zero, it means the DVD does not have any text strings.</span></span> <span data-ttu-id="bce1a-125"> (這可能是最常見的情況，也就是最常見的情況。 ) </span><span class="sxs-lookup"><span data-stu-id="bce1a-125">(This is perhaps the most common case, in fact.)</span></span>
2.  <span data-ttu-id="bce1a-126">如果語言的數目至少為一個，請呼叫 [**IDvdInfo2：： GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) 來取得每個語言的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bce1a-126">If the number of languages is at least one, call [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) to get information about each language.</span></span> <span data-ttu-id="bce1a-127">此語言是以索引指定。</span><span class="sxs-lookup"><span data-stu-id="bce1a-127">The language is specified by index.</span></span> <span data-ttu-id="bce1a-128">方法會傳回該語言中的文字字串總數、語言的地區設定識別碼 (**LCID**) ，以及字元編碼 (Unicode 或其他) 。</span><span class="sxs-lookup"><span data-stu-id="bce1a-128">The method returns the total number of text strings in that language, the locale identifier (**LCID**) for the language, and the character encoding (Unicode or other).</span></span> <span data-ttu-id="bce1a-129">DVD 文字字串可以使用數個不同的字元集;這些會列在 [**DVD \_ TextCharSet 列舉**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset)中。</span><span class="sxs-lookup"><span data-stu-id="bce1a-129">DVD text strings can use several different character sets; these are listed in [**DVD\_TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span></span>
3.  <span data-ttu-id="bce1a-130">若要取得文字字串，請呼叫 [**IDvdInfo2：： GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) 或 [**IDvdInfo2：： GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)。</span><span class="sxs-lookup"><span data-stu-id="bce1a-130">To get a text string, call [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) or [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span></span> <span data-ttu-id="bce1a-131">第一個方法會傳回寬字元字串，但不支援每個字元集。</span><span class="sxs-lookup"><span data-stu-id="bce1a-131">The first method returns a wide-character string, but does not support every character set.</span></span> <span data-ttu-id="bce1a-132">第二個方法會傳回包含原始文字資料的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="bce1a-132">The second method returns a byte array containing the raw text data.</span></span> <span data-ttu-id="bce1a-133">針對這兩種方法，您可以使用 **Null** 緩衝區指標來呼叫方法，以找出字串的大小和文字類型。</span><span class="sxs-lookup"><span data-stu-id="bce1a-133">For both methods, you can call the method with a **NULL** buffer pointer to find the size of the string and the text type.</span></span> <span data-ttu-id="bce1a-134">接著配置緩衝區，並再次呼叫方法以取得字串。</span><span class="sxs-lookup"><span data-stu-id="bce1a-134">Then allocate a buffer and call the method again to get the string.</span></span>

<span data-ttu-id="bce1a-135">每個文字字串都有相關聯的識別碼代碼，表示文字字串的意義。</span><span class="sxs-lookup"><span data-stu-id="bce1a-135">Each text string has an associated identifier code, which indicates the meaning of the text string.</span></span> <span data-ttu-id="bce1a-136">此識別碼會以 [**DVD \_ TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) 值的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="bce1a-136">The identifier is returned as a [**DVD\_TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) value.</span></span> <span data-ttu-id="bce1a-137">有兩種類別的識別碼： *結構識別碼* 和 *內容識別碼*。</span><span class="sxs-lookup"><span data-stu-id="bce1a-137">There are two categories of identifier: *structure identifiers* and *content identifiers*.</span></span> <span data-ttu-id="bce1a-138">結構識別碼的數值代碼範圍為0x00 –0x02F。</span><span class="sxs-lookup"><span data-stu-id="bce1a-138">Structure identifiers have numeric codes in the range 0x00–0x02F.</span></span> <span data-ttu-id="bce1a-139">內容識別碼的範圍為0x30< 和更高。</span><span class="sxs-lookup"><span data-stu-id="bce1a-139">Content identifiers have a range of 0x30 and higher.</span></span> <span data-ttu-id="bce1a-140"> (**DVD \_ TextStringType** 列舉會定義最常見識別碼的子集，但 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) 方法可以傳回任何識別碼代碼。 ) 結構識別碼描述 DVD 的邏輯部分，例如音量、標題或標題的一部分 (platform ptt) 。</span><span class="sxs-lookup"><span data-stu-id="bce1a-140">(The **DVD\_TextStringType** enumeration defines a subset of the most common identifiers, but the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods can return any identifier code.) A structure identifier describes a logical portion of the DVD, such as volume, title, or part of title (PTT).</span></span> <span data-ttu-id="bce1a-141">內容識別碼表示特定文字字串的意義，例如電影標題、歌曲標題或內容類型。</span><span class="sxs-lookup"><span data-stu-id="bce1a-141">A content identifier indicates the meaning of a particular text string, such as movie title, song title, or genre.</span></span>

<span data-ttu-id="bce1a-142">結構識別碼沒有相關聯的文字字串。</span><span class="sxs-lookup"><span data-stu-id="bce1a-142">Structure identifiers do not have associated text strings.</span></span> <span data-ttu-id="bce1a-143">當結構識別碼出現在文字字串資料中時，它會指出下列文字字串會套用至 DVD 的該邏輯部分，直到下一個結構識別碼為止。</span><span class="sxs-lookup"><span data-stu-id="bce1a-143">When a structure identifier appears in the text-string data, it signals that the following text strings apply to that logical portion of the DVD, up until the next structure identifier.</span></span> <span data-ttu-id="bce1a-144">文字資料中結構識別碼的位置會對應至 DVD 磁片區的邏輯階層。</span><span class="sxs-lookup"><span data-stu-id="bce1a-144">The position of the structure identifiers within the text data corresponds to the logical hierarchy of the DVD volume.</span></span> <span data-ttu-id="bce1a-145">例如，第一次出現的 DVD \_ 結構 \_ 標題識別碼 (0x02) 代表磁片區中的第一個標題，而下一個出現專案代表第二個標題。</span><span class="sxs-lookup"><span data-stu-id="bce1a-145">For example, the first occurrence of the DVD\_Struct\_Title identifier (0x02) represents the first title in the volume, and the next occurrence represents the second title.</span></span>

<span data-ttu-id="bce1a-146">下表說明如何針對有兩個標題的 DVD 定義文字字串。</span><span class="sxs-lookup"><span data-stu-id="bce1a-146">The following table shows how the text strings might be defined for a DVD with two titles.</span></span>



| <span data-ttu-id="bce1a-147">DVD \_ TextStringType</span><span class="sxs-lookup"><span data-stu-id="bce1a-147">DVD\_TextStringType</span></span>        | <span data-ttu-id="bce1a-148">文字字串</span><span class="sxs-lookup"><span data-stu-id="bce1a-148">Text string</span></span>  | <span data-ttu-id="bce1a-149">Description</span><span class="sxs-lookup"><span data-stu-id="bce1a-149">Description</span></span>                                    |
|----------------------------|--------------|------------------------------------------------|
| <span data-ttu-id="bce1a-150">DVD \_ 結構 \_ 磁片區 (0x01) </span><span class="sxs-lookup"><span data-stu-id="bce1a-150">DVD\_Struct\_Volume (0x01)</span></span> | <span data-ttu-id="bce1a-151">""</span><span class="sxs-lookup"><span data-stu-id="bce1a-151">""</span></span>           | <span data-ttu-id="bce1a-152">整個光碟端的結構識別碼。</span><span class="sxs-lookup"><span data-stu-id="bce1a-152">Structure identifier for the entire disc side.</span></span> |
| <span data-ttu-id="bce1a-153">DVD \_ 一般 \_ 名稱 (0x30<) </span><span class="sxs-lookup"><span data-stu-id="bce1a-153">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="bce1a-154">「DVD 音量」</span><span class="sxs-lookup"><span data-stu-id="bce1a-154">"DVD Volume"</span></span> | <span data-ttu-id="bce1a-155">DVD 磁片區名稱。</span><span class="sxs-lookup"><span data-stu-id="bce1a-155">DVD volume name.</span></span>                               |
| <span data-ttu-id="bce1a-156">DVD \_ 結構 \_ 標題 (0x02) </span><span class="sxs-lookup"><span data-stu-id="bce1a-156">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="bce1a-157">""</span><span class="sxs-lookup"><span data-stu-id="bce1a-157">""</span></span>           | <span data-ttu-id="bce1a-158">第一個標題的結構識別碼。</span><span class="sxs-lookup"><span data-stu-id="bce1a-158">Structure identifier for the first title.</span></span>      |
| <span data-ttu-id="bce1a-159">DVD \_ 一般 \_ 名稱 (0x30<) </span><span class="sxs-lookup"><span data-stu-id="bce1a-159">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="bce1a-160">"Title 1"</span><span class="sxs-lookup"><span data-stu-id="bce1a-160">"Title 1"</span></span>    | <span data-ttu-id="bce1a-161">第一個標題的名稱。</span><span class="sxs-lookup"><span data-stu-id="bce1a-161">Name of the first title.</span></span>                       |
| <span data-ttu-id="bce1a-162">DVD \_ 結構 \_ 標題 (0x02) </span><span class="sxs-lookup"><span data-stu-id="bce1a-162">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="bce1a-163">""</span><span class="sxs-lookup"><span data-stu-id="bce1a-163">""</span></span>           | <span data-ttu-id="bce1a-164">第二個標題的結構識別碼。</span><span class="sxs-lookup"><span data-stu-id="bce1a-164">Structure identifier for the second title.</span></span>     |
| <span data-ttu-id="bce1a-165">DVD \_ 一般 \_ 名稱 (0x30<) </span><span class="sxs-lookup"><span data-stu-id="bce1a-165">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="bce1a-166">"Title 2"</span><span class="sxs-lookup"><span data-stu-id="bce1a-166">"Title 2"</span></span>    | <span data-ttu-id="bce1a-167">第二個標題的名稱。</span><span class="sxs-lookup"><span data-stu-id="bce1a-167">Name of the second title.</span></span>                      |



 

<span data-ttu-id="bce1a-168">[**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)和 [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)方法會將結構識別碼和內容識別碼視為相同。</span><span class="sxs-lookup"><span data-stu-id="bce1a-168">The [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) and [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) methods treat structure identifiers and content identifiers the same.</span></span> <span data-ttu-id="bce1a-169">唯一的差別在於，在結構識別碼中，相關聯的文字緩衝區是空的。</span><span class="sxs-lookup"><span data-stu-id="bce1a-169">The only difference is that for structure identifiers, the associated text buffer is empty.</span></span> <span data-ttu-id="bce1a-170">應用程式會負責追蹤文字字串與 DVD 邏輯部分之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="bce1a-170">It is up to the application to keep track of the relationship between the text strings and the logical portions of the DVD.</span></span>

<span data-ttu-id="bce1a-171">下列範例顯示如何從 DVD 取得文字字串。</span><span class="sxs-lookup"><span data-stu-id="bce1a-171">The following example shows how to get text strings from a DVD.</span></span> <span data-ttu-id="bce1a-172">此範例會忽略實際應用程式需要的一些詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bce1a-172">This example ignores some details that a real application would require.</span></span> <span data-ttu-id="bce1a-173"> (例如，它會忽略結構識別碼。 ) 此範例只會顯示正確的呼叫順序。</span><span class="sxs-lookup"><span data-stu-id="bce1a-173">(For example, it ignores structure identifiers.) The example is only meant to show the correct sequence of calls.</span></span>


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



<span data-ttu-id="bce1a-174">如需 DVD 文字字串的詳細資訊，請參閱 [Dvd 論壇的網站](https://go.microsoft.com/fwlink/?LinkId=8677)。</span><span class="sxs-lookup"><span data-stu-id="bce1a-174">For information on DVD text strings, see the [DVD Forum's Web site](https://go.microsoft.com/fwlink/?LinkId=8677).</span></span>

<span data-ttu-id="bce1a-175">DVDSample 應用程式中的 **CDvdCore：： GetDvdText** 方法會示範列舉和顯示 DVD 文字字串的基本步驟。</span><span class="sxs-lookup"><span data-stu-id="bce1a-175">The **CDvdCore::GetDvdText** method in the DVDSample application demonstrates the basic steps in enumerating and displaying DVD text strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bce1a-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="bce1a-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce1a-177">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="bce1a-177">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



