---
description: 本文描述篩選圖形管理員如何找出檔案名，以尋找來源篩選。
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: 註冊自訂檔案類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970883"
---
# <a name="registering-a-custom-file-type"></a><span data-ttu-id="b55f0-103">註冊自訂檔案類型</span><span class="sxs-lookup"><span data-stu-id="b55f0-103">Registering a Custom File Type</span></span>

<span data-ttu-id="b55f0-104">本文描述篩選圖形管理員如何找出檔案名，以尋找來源篩選。</span><span class="sxs-lookup"><span data-stu-id="b55f0-104">This article describes how the Filter Graph Manager locates a source filter, given a file name.</span></span> <span data-ttu-id="b55f0-105">您可以使用此機制來註冊您自己的自訂檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b55f0-105">You can use this mechanism to register your own custom file types.</span></span> <span data-ttu-id="b55f0-106">一旦註冊檔案類型，每當應用程式呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 或 [**IGraphBuilder：： AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)時，DirectShow 都會自動載入正確的來源篩選器。</span><span class="sxs-lookup"><span data-stu-id="b55f0-106">Once the file type is registered, DirectShow will automatically load the correct source filter whenever an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

-   [<span data-ttu-id="b55f0-107">概觀</span><span class="sxs-lookup"><span data-stu-id="b55f0-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="b55f0-108">通訊協定</span><span class="sxs-lookup"><span data-stu-id="b55f0-108">Protocols</span></span>](#protocols)
-   [<span data-ttu-id="b55f0-109">副檔名</span><span class="sxs-lookup"><span data-stu-id="b55f0-109">File Extensions</span></span>](#file-extensions)
-   [<span data-ttu-id="b55f0-110">檢查位元組</span><span class="sxs-lookup"><span data-stu-id="b55f0-110">Check Bytes</span></span>](#check-bytes)
-   [<span data-ttu-id="b55f0-111">載入來源篩選</span><span class="sxs-lookup"><span data-stu-id="b55f0-111">Loading the Source Filter</span></span>](#loading-the-source-filter)
-   [<span data-ttu-id="b55f0-112">Windows Media Player 中的自訂檔案類型</span><span class="sxs-lookup"><span data-stu-id="b55f0-112">Custom File Types in Windows Media Player</span></span>](#custom-file-types-in-windows-media-player)
-   [<span data-ttu-id="b55f0-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b55f0-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="b55f0-114">概觀</span><span class="sxs-lookup"><span data-stu-id="b55f0-114">Overview</span></span>

<span data-ttu-id="b55f0-115">若要從指定的檔案名找出來源篩選，篩選圖形管理員會嘗試依序執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="b55f0-115">To locate a source filter from a given file name, the Filter Graph Manager attempts to do the following, in order:</span></span>

1.  <span data-ttu-id="b55f0-116">符合通訊協定（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b55f0-116">Match the protocol, if any.</span></span>
2.  <span data-ttu-id="b55f0-117">符合副檔名。</span><span class="sxs-lookup"><span data-stu-id="b55f0-117">Match the file extension.</span></span>
3.  <span data-ttu-id="b55f0-118">符合檔案內的位元組模式，稱為 *檢查位元組*。</span><span class="sxs-lookup"><span data-stu-id="b55f0-118">Match patterns of bytes within the file, called *check bytes*.</span></span>

## <a name="protocols"></a><span data-ttu-id="b55f0-119">通訊協定</span><span class="sxs-lookup"><span data-stu-id="b55f0-119">Protocols</span></span>

<span data-ttu-id="b55f0-120">通訊協定名稱（例如 "ftp" 或 "HTTP"）會註冊在</span><span class="sxs-lookup"><span data-stu-id="b55f0-120">Protocol names such as "ftp" or "http" are registered under the</span></span>

<span data-ttu-id="b55f0-121">**HKEY \_ 類別 \_ 根目錄**</span><span class="sxs-lookup"><span data-stu-id="b55f0-121">**HKEY\_CLASSES\_ROOT**</span></span>

<span data-ttu-id="b55f0-122">具有下列結構的索引鍵：</span><span class="sxs-lookup"><span data-stu-id="b55f0-122">key, with the following structure:</span></span>


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



<span data-ttu-id="b55f0-123">如果檔案名或 URL 包含冒號 ( '： ' ) ，則篩選圖形管理員會嘗試使用 '： ' 之前的部分做為通訊協定名稱。</span><span class="sxs-lookup"><span data-stu-id="b55f0-123">If the file name or URL contains a colon (':'), the Filter Graph Manager attempts to use the portion before the ':' as a protocol name.</span></span> <span data-ttu-id="b55f0-124">例如，如果名稱為 "myprot://myfile.ext"，則會搜尋名為 **myprot** 的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="b55f0-124">For example, if the name is "myprot://myfile.ext", it searches for a registry key named **myprot**.</span></span> <span data-ttu-id="b55f0-125">如果此索引鍵存在且包含名為 "Extensions" 的子機碼，則篩選圖形管理員會在該子機碼內搜尋符合副檔名的專案。</span><span class="sxs-lookup"><span data-stu-id="b55f0-125">If this key exists and contains a subkey named "Extensions", the Filter Graph Manager searches within that subkey for entries that match the file extension.</span></span> <span data-ttu-id="b55f0-126">索引鍵的值必須是字串格式的 GUID。例如： " {00000000-0000-0000-0000-000000000000} "。</span><span class="sxs-lookup"><span data-stu-id="b55f0-126">The value of the key must be a GUID in string form; for example, "{00000000-0000-0000-0000-000000000000}".</span></span> <span data-ttu-id="b55f0-127">如果篩選圖形管理員無法比對 **延伸** 子機碼內的任何字元，則會尋找名為 **來源篩選** 器的子機碼，該子機碼必須也是字串格式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b55f0-127">If the Filter Graph Manager cannot match anything within the **Extensions** subkey, it looks for a subkey named **Source Filter**, which must also be a GUID in string form.</span></span>

<span data-ttu-id="b55f0-128">如果篩選圖形管理員找到相符的 GUID，則會使用此 GUID 做為來源篩選的 CLSID，並嘗試載入篩選。</span><span class="sxs-lookup"><span data-stu-id="b55f0-128">If the Filter Graph Manager finds a matching GUID, it uses this as the CLSID of the source filter, and attempts to load the filter.</span></span> <span data-ttu-id="b55f0-129">如果找不到相符項，則會使用檔案 [來源 (url) ](file-source--url--filter.md) 篩選，這會將檔案名視為 url。</span><span class="sxs-lookup"><span data-stu-id="b55f0-129">If it does not find a match, it uses the [File Source (URL)](file-source--url--filter.md) filter, which treats the file name as a URL.</span></span>

<span data-ttu-id="b55f0-130">此演算法有兩種例外狀況：</span><span class="sxs-lookup"><span data-stu-id="b55f0-130">There are two exceptions to this algorithm:</span></span>

-   <span data-ttu-id="b55f0-131">若要排除驅動程式字母，則不會將單一字元字串視為通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b55f0-131">To exclude driver letters, single-character strings are not considered protocols.</span></span>
-   <span data-ttu-id="b55f0-132">如果字串為 "file：" 或 "file://"，則不會將它視為通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b55f0-132">If the string is "file:" or "file://", it is not treated as a protocol.</span></span>

## <a name="file-extensions"></a><span data-ttu-id="b55f0-133">副檔名</span><span class="sxs-lookup"><span data-stu-id="b55f0-133">File Extensions</span></span>

<span data-ttu-id="b55f0-134">如果檔案名中沒有通訊協定，則篩選圖形管理員會在登錄中尋找具有 key **HKEY \_ 類別 \_ 根 \\ 媒體類型 \\ 副檔名 \\** 的專案。*ext* \\ ，其中。*ext* 是副檔名。</span><span class="sxs-lookup"><span data-stu-id="b55f0-134">If there is no protocol in the file name, the Filter Graph Manager looks in the registry for entries with the key **HKEY\_CLASSES\_ROOT\\Media Type\\Extensions\\**.*ext*\\, where .*ext* is the file extension.</span></span> <span data-ttu-id="b55f0-135">如果此索引鍵存在，值 **來源篩選** 就會包含來源篩選的 CLSID （以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="b55f0-135">If this key exists, the value **Source Filter** contains the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="b55f0-136">（選擇性）索引鍵可以有 **媒體類型** 和 **子** 類型的值，以提供主要類型和子類型 guid。</span><span class="sxs-lookup"><span data-stu-id="b55f0-136">Optionally, the key can have values for **Media Type** and **Subtype**, which give the major type and subtype GUIDs.</span></span>

## <a name="check-bytes"></a><span data-ttu-id="b55f0-137">檢查位元組</span><span class="sxs-lookup"><span data-stu-id="b55f0-137">Check Bytes</span></span>

<span data-ttu-id="b55f0-138">某些檔案類型可透過在檔案中特定位元組位移處發生的特定位模式來識別。</span><span class="sxs-lookup"><span data-stu-id="b55f0-138">Some file types can be identified by specific patterns of bits occurring at specific byte offsets in the file.</span></span> <span data-ttu-id="b55f0-139">篩選圖形管理員會在登錄中尋找下列格式的索引鍵：</span><span class="sxs-lookup"><span data-stu-id="b55f0-139">The Filter Graph Manager looks in the registry for keys with the following form:</span></span>

<span data-ttu-id="b55f0-140">\**HKEY \_類別 \_ 根 \\ 媒體 \\*\*\*類型 {主要類型*} \\ {*子類型*}</span><span class="sxs-lookup"><span data-stu-id="b55f0-140">**HKEY\_CLASSES\_ROOT\\MediaType\\**{ *major type* }\\{ *subtype* }</span></span>

<span data-ttu-id="b55f0-141">其中的 *主要類型* 和 *子類型* 為 guid，可定義位元組資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b55f0-141">where *major type* and *subtype* are GUIDs that define the media type for the byte stream.</span></span> <span data-ttu-id="b55f0-142">每個金鑰都包含一或多個子機碼，通常名為1、2等等，以定義檢查位元組;和名為 **來源篩選器** 的子機碼，以字串形式提供來源篩選器的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="b55f0-142">Each key contains one or more subkeys, usually named 1, 2, and so on, which define the check bytes; and a subkey named **Source Filter** that gives the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="b55f0-143">檢查位元組子機碼是包含一或多個數位四邊形的字串，稱為：</span><span class="sxs-lookup"><span data-stu-id="b55f0-143">The check-byte subkeys are strings that contain one or more quads of numbers called:</span></span>

<span data-ttu-id="b55f0-144">*offset*、 *cb*、 *mask*、 *val*</span><span class="sxs-lookup"><span data-stu-id="b55f0-144">*offset*, *cb*, *mask*, *val*</span></span>

<span data-ttu-id="b55f0-145">為了比對檔案，篩選圖形管理員會讀取 cb 個位元組，從位元組數位移開始。</span><span class="sxs-lookup"><span data-stu-id="b55f0-145">To match the file, the Filter Graph Manager reads cb bytes, starting from byte number offset.</span></span> <span data-ttu-id="b55f0-146">然後，它會對 mask 中的值執行位 AND。</span><span class="sxs-lookup"><span data-stu-id="b55f0-146">It then performs a bitwise-AND against the value in mask.</span></span> <span data-ttu-id="b55f0-147">如果結果等於 val，檔案就會符合該四個。</span><span class="sxs-lookup"><span data-stu-id="b55f0-147">If the result equals val, the file is a match for that quad.</span></span> <span data-ttu-id="b55f0-148">值 mask 和 val 會以十六進位提供。</span><span class="sxs-lookup"><span data-stu-id="b55f0-148">The values mask and val are given in hex.</span></span> <span data-ttu-id="b55f0-149">遮罩的空白專案會視為長度為 cb 的1：1的字串。</span><span class="sxs-lookup"><span data-stu-id="b55f0-149">A blank entry for mask is treated as a string of 1s of length cb.</span></span> <span data-ttu-id="b55f0-150">Offset 的負數值表示從檔案結尾算出的位移。</span><span class="sxs-lookup"><span data-stu-id="b55f0-150">A negative value for offset indicates an offset from the end of the file.</span></span> <span data-ttu-id="b55f0-151">為了符合此索引鍵，檔案必須符合任何子機碼中的所有四邊形。</span><span class="sxs-lookup"><span data-stu-id="b55f0-151">To match the key, the file must match all of the quads in any of the subkeys.</span></span>

<span data-ttu-id="b55f0-152">例如，假設登錄在 **HKCR \\ 媒體類型** 下包含下列機碼：</span><span class="sxs-lookup"><span data-stu-id="b55f0-152">For example, assume the registry contains the following keys under **HKCR\\Media Type**:</span></span>


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



<span data-ttu-id="b55f0-153">第一個索引鍵對應至主要型別媒體型 \_ 資料流程。</span><span class="sxs-lookup"><span data-stu-id="b55f0-153">The first key corresponds to the major type MEDIATYPE\_Stream.</span></span> <span data-ttu-id="b55f0-154">下面的子機碼會對應到類型為的型別（ \_ Midi）。</span><span class="sxs-lookup"><span data-stu-id="b55f0-154">The subkey below that corresponds to the subtype MEDIATYPE\_Midi.</span></span> <span data-ttu-id="b55f0-155">來源篩選子機碼的值是 CLSID \_ AsyncReader、檔案來源的 clsid [ (Async) ](file-source--async--filter.md) 篩選。</span><span class="sxs-lookup"><span data-stu-id="b55f0-155">The value for the Source Filter subkey is CLSID\_AsyncReader, the CLSID of the [File Source (Async)](file-source--async--filter.md) filter.</span></span>

<span data-ttu-id="b55f0-156">每個專案都可以有多個時;所有專案都必須相符。</span><span class="sxs-lookup"><span data-stu-id="b55f0-156">Each entry can have multiple quadruples; all of them must match.</span></span> <span data-ttu-id="b55f0-157">在下列範例中，檔案的前4個位元組必須是0xAB、0xCD、0x12、0x34;而且檔案的最後4個位元組必須是0xAB、0xAB、0x00、0xAB：</span><span class="sxs-lookup"><span data-stu-id="b55f0-157">In the following example, the first 4 bytes of the file must be 0xAB, 0xCD, 0x12, 0x34; and the last 4 bytes of the file must be 0xAB, 0xAB, 0x00, 0xAB:</span></span>


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



<span data-ttu-id="b55f0-158">此外，單一媒體類型下可能會有多個專案。</span><span class="sxs-lookup"><span data-stu-id="b55f0-158">Also, there can be multiple entries listed under a single media type.</span></span> <span data-ttu-id="b55f0-159">其中任何一項都已足夠。</span><span class="sxs-lookup"><span data-stu-id="b55f0-159">A match to any of them is sufficient.</span></span> <span data-ttu-id="b55f0-160">此配置允許一組替代的遮罩;例如，可能或可能不具有 RIFF 標頭的 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="b55f0-160">This scheme allows for a set of alternative masks; for instance, .wav files that might or might not have a RIFF header.</span></span>

> [!Note]  
> <span data-ttu-id="b55f0-161">此配置類似于 [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) 函數所使用的配置。</span><span class="sxs-lookup"><span data-stu-id="b55f0-161">This scheme is similar to the one used by the [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) function.</span></span>

 

## <a name="loading-the-source-filter"></a><span data-ttu-id="b55f0-162">載入來源篩選</span><span class="sxs-lookup"><span data-stu-id="b55f0-162">Loading the Source Filter</span></span>

<span data-ttu-id="b55f0-163">假設篩選圖形管理員找到相符的檔案來源篩選器，它會將該篩選新增至圖形、查詢 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) 介面的篩選，以及呼叫 [**IFileSourceFilter：： Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load)。</span><span class="sxs-lookup"><span data-stu-id="b55f0-163">Assuming that the Filter Graph Manager finds a matching source filter for the file, it adds that filter to the graph, queries the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface, and calls [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span></span> <span data-ttu-id="b55f0-164">**載入** 方法的引數是從登錄所決定的檔案名和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="b55f0-164">The arguments to the **Load** method are the file name and the media type, as determined from the registry.</span></span>

<span data-ttu-id="b55f0-165">如果篩選圖形管理員在登錄中找不到任何檔案，則會預設為使用非同步檔案來源篩選。</span><span class="sxs-lookup"><span data-stu-id="b55f0-165">If the Filter Graph Manager cannot find anything from the registry, it defaults to using the Async File Source filter.</span></span> <span data-ttu-id="b55f0-166">在這種情況下，它會將媒體類型 **設定為媒體 \_** 類型， **MEDIASUBTYPE \_ 無**。</span><span class="sxs-lookup"><span data-stu-id="b55f0-166">In that case, it sets the media type to **MEDIATYPE\_Stream**, **MEDIASUBTYPE\_None**.</span></span>

## <a name="custom-file-types-in-windows-media-player"></a><span data-ttu-id="b55f0-167">Windows Media Player 中的自訂檔案類型</span><span class="sxs-lookup"><span data-stu-id="b55f0-167">Custom File Types in Windows Media Player</span></span>

<span data-ttu-id="b55f0-168">Windows Media Player 會使用一組額外的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="b55f0-168">Windows Media Player uses an additional set of registry entries.</span></span> <span data-ttu-id="b55f0-169">如需詳細資訊，請參閱 Windows Media Player SDK 中的 [副檔名登錄設定](../wmp/file-name-extension-registry-settings.md) 。</span><span class="sxs-lookup"><span data-stu-id="b55f0-169">For more information, see [File Name Extension Registry Settings](../wmp/file-name-extension-registry-settings.md) in the Windows Media Player SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b55f0-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="b55f0-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b55f0-171">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="b55f0-171">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 
