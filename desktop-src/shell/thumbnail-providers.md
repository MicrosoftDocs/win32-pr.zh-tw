---
description: Windows Vista 比舊版 Windows 更容易使用檔案專屬的縮圖影像。
title: 縮圖處理常式
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194429"
---
# <a name="thumbnail-handlers"></a><span data-ttu-id="b723b-103">縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="b723b-103">Thumbnail Handlers</span></span>

<span data-ttu-id="b723b-104">Windows Vista 比舊版 Windows 更容易使用檔案專屬的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="b723b-104">Windows Vista makes greater use of file-specific thumbnail images than earlier versions of Windows.</span></span> <span data-ttu-id="b723b-105">Windows Vista 在所有的視圖、對話方塊以及提供它們的任何檔案類型中使用它們。</span><span class="sxs-lookup"><span data-stu-id="b723b-105">Windows Vista uses them in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="b723b-106">其他應用程式也可以使用您的縮圖。</span><span class="sxs-lookup"><span data-stu-id="b723b-106">Other applications can consume your thumbnail as well.</span></span> <span data-ttu-id="b723b-107">縮圖顯示也已變更。</span><span class="sxs-lookup"><span data-stu-id="b723b-107">Thumbnail display has also changed.</span></span> <span data-ttu-id="b723b-108">現在可以使用連續的使用者可選取大小，而不是 Windows XP 中提供的各種不同大小，例如圖示和縮圖。</span><span class="sxs-lookup"><span data-stu-id="b723b-108">Now, a continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails provided in Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="b723b-109">您可能會聽到這些縮圖稱為「即時」圖示。</span><span class="sxs-lookup"><span data-stu-id="b723b-109">You might hear these thumbnails referred to as Live Icons.</span></span>

 

<span data-ttu-id="b723b-110">Windows Vista UI 中通常會使用32位解析的縮圖，且大小為256x256 圖元。</span><span class="sxs-lookup"><span data-stu-id="b723b-110">Thumbnails of 32-bit resolution and as large as 256x256 pixels are often used in Windows Vista UI.</span></span> <span data-ttu-id="b723b-111">檔案格式擁有者應該準備好以該大小顯示其縮圖。</span><span class="sxs-lookup"><span data-stu-id="b723b-111">File format owners should be prepared to display their thumbnails at that size.</span></span> <span data-ttu-id="b723b-112">它們也應該針對反映特定檔案內容的縮圖提供非靜態影像。</span><span class="sxs-lookup"><span data-stu-id="b723b-112">They should also provide non-static images for their thumbnails that reflect the particular file's contents.</span></span> <span data-ttu-id="b723b-113">例如，文字檔的縮圖應顯示檔的縮圖版本，包括其文字。</span><span class="sxs-lookup"><span data-stu-id="b723b-113">For example, a text file's thumbnail should show a miniature version of the document, including its text.</span></span>

<span data-ttu-id="b723b-114">已引進 [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) 介面，可讓您更輕鬆且更直接地提供縮圖，而不是使用 [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) 。</span><span class="sxs-lookup"><span data-stu-id="b723b-114">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface has been introduced to make providing a thumbnail easier and more straightforward than in the past, when [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) would have been used instead.</span></span> <span data-ttu-id="b723b-115">請注意，在 Windows Vista 下，使用 **IExtractImage** 的現有程式碼仍然有效。</span><span class="sxs-lookup"><span data-stu-id="b723b-115">Note, that existing code that uses **IExtractImage** is still valid under Windows Vista.</span></span> <span data-ttu-id="b723b-116">不過，在 **詳細資料** 窗格中不支援 **IExtractImage** 。</span><span class="sxs-lookup"><span data-stu-id="b723b-116">However, **IExtractImage** is not supported in the **Details** pane.</span></span>

<span data-ttu-id="b723b-117">本主題將討論下列內容：</span><span class="sxs-lookup"><span data-stu-id="b723b-117">This topic discusses the following:</span></span>

-   [<span data-ttu-id="b723b-118">縮圖流程</span><span class="sxs-lookup"><span data-stu-id="b723b-118">Thumbnail Processes</span></span>](#thumbnail-processes)
-   [<span data-ttu-id="b723b-119">縮圖快取和調整大小</span><span class="sxs-lookup"><span data-stu-id="b723b-119">Thumbnail Cache and Sizing</span></span>](#thumbnail-cache-and-sizing)
-   [<span data-ttu-id="b723b-120">縮圖覆蓋</span><span class="sxs-lookup"><span data-stu-id="b723b-120">Thumbnail Overlays</span></span>](#thumbnail-overlays)
-   [<span data-ttu-id="b723b-121">縮圖裝飾</span><span class="sxs-lookup"><span data-stu-id="b723b-121">Thumbnail Adornments</span></span>](#thumbnail-adornments)
-   [<span data-ttu-id="b723b-122">註冊您的縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="b723b-122">Registering Your Thumbnail Handler</span></span>](#registering-your-thumbnail-handler)
-   [<span data-ttu-id="b723b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="b723b-123">Related topics</span></span>](#related-topics)

## <a name="thumbnail-processes"></a><span data-ttu-id="b723b-124">縮圖流程</span><span class="sxs-lookup"><span data-stu-id="b723b-124">Thumbnail Processes</span></span>

<span data-ttu-id="b723b-125">處理常式（包括縮圖處理常式）依預設會在個別進程中執行。</span><span class="sxs-lookup"><span data-stu-id="b723b-125">Handlers, including thumbnail handlers, run by default in a separate process.</span></span> <span data-ttu-id="b723b-126">您可以在 [**IShellItem：： BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler)的呼叫中傳遞 **Null** 值作為系結內容，以強制處理常式在同進程執行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b723b-126">You can force the handler to run in-process by passing a **NULL** value as the bind context in a call to [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) as shown here:</span></span>


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



<span data-ttu-id="b723b-127">您也可以藉由在登錄中設定 DisableProcessIsolation 專案，選擇不使用進程外的程式，如本範例所示。</span><span class="sxs-lookup"><span data-stu-id="b723b-127">You can also opt out of running out of process by default by setting the DisableProcessIsolation entry in the registry as shown in this example.</span></span> <span data-ttu-id="b723b-128">) {E357FCCD-A995-4576-B01F-234630154E96} (CLSID 的類別識別碼是 [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) 執行的 clsid。</span><span class="sxs-lookup"><span data-stu-id="b723b-128">The class identifier (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} is the CLSID for [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) implementations.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a><span data-ttu-id="b723b-129">縮圖快取和調整大小</span><span class="sxs-lookup"><span data-stu-id="b723b-129">Thumbnail Cache and Sizing</span></span>

<span data-ttu-id="b723b-130">需要縮圖時，Windows 會先檢查影像的縮圖快取。</span><span class="sxs-lookup"><span data-stu-id="b723b-130">When a thumbnail is needed, Windows first checks the thumbnail cache for the image.</span></span> <span data-ttu-id="b723b-131">如果在快取中找不到影像，則會呼叫縮圖解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="b723b-131">The thumbnail extractor is called if the image is not found in the cache.</span></span> <span data-ttu-id="b723b-132">當映射的上次修改時間晚于快取中的複本時，也會呼叫它。</span><span class="sxs-lookup"><span data-stu-id="b723b-132">It is also called when the last modified time of the image is later than that of the copy in the cache.</span></span>

<span data-ttu-id="b723b-133">此快取中的縮圖影像會儲存成一組不同的大小。</span><span class="sxs-lookup"><span data-stu-id="b723b-133">The thumbnail images in this cache are stored in a set of discrete sizes.</span></span> <span data-ttu-id="b723b-134">所有大小都會以圖元為單位。</span><span class="sxs-lookup"><span data-stu-id="b723b-134">All sizes are given in pixels.</span></span>

-   <span data-ttu-id="b723b-135">32x32</span><span class="sxs-lookup"><span data-stu-id="b723b-135">32x32</span></span>
-   <span data-ttu-id="b723b-136">96x96</span><span class="sxs-lookup"><span data-stu-id="b723b-136">96x96</span></span>
-   <span data-ttu-id="b723b-137">256 x 256</span><span class="sxs-lookup"><span data-stu-id="b723b-137">256x256</span></span>
-   <span data-ttu-id="b723b-138">1024x1024</span><span class="sxs-lookup"><span data-stu-id="b723b-138">1024x1024</span></span>

> [!Note]  
> <span data-ttu-id="b723b-139">這些值可能會變更。</span><span class="sxs-lookup"><span data-stu-id="b723b-139">These values are subject to change.</span></span> <span data-ttu-id="b723b-140">您的程式碼不應假設一律會使用任何特定的大小。</span><span class="sxs-lookup"><span data-stu-id="b723b-140">You code should not assume that any particular size will always be used.</span></span>

 

<span data-ttu-id="b723b-141">如果影像不是正方形，您就不應該自行填補。</span><span class="sxs-lookup"><span data-stu-id="b723b-141">If an image is not square, you should not pad it yourself.</span></span> <span data-ttu-id="b723b-142">Windows 負責遵循原始的外觀比例，並將影像填補為正方形大小。</span><span class="sxs-lookup"><span data-stu-id="b723b-142">Windows is responsible for respecting the original aspect ratio and padding the image to a square size.</span></span>

<span data-ttu-id="b723b-143">當系統要求特定大小的影像時，除非找到完全相符的映射，否則 Windows Vista 一律會抓取下一個最大的影像，並將其向下調整為所要求的大小。</span><span class="sxs-lookup"><span data-stu-id="b723b-143">When an image of a particular size is asked for, unless an exact match is found, Windows Vista always retrieves the next largest image and scales it down to the requested size.</span></span> <span data-ttu-id="b723b-144">在舊版的 Windows 中，映射的大小絕對不會像這樣。</span><span class="sxs-lookup"><span data-stu-id="b723b-144">An image is never scaled up in size as was the case in previous versions of Windows.</span></span>

<span data-ttu-id="b723b-145">下表提供所要求大小和可用大小之間關聯性的一些範例。</span><span class="sxs-lookup"><span data-stu-id="b723b-145">The following table gives some examples of the relationship between requested size and available size.</span></span>



| <span data-ttu-id="b723b-146">您提供的映射大小上限</span><span class="sxs-lookup"><span data-stu-id="b723b-146">Maximum Image Size You Provide</span></span> | <span data-ttu-id="b723b-147">解壓縮程式要求的大小</span><span class="sxs-lookup"><span data-stu-id="b723b-147">Size Requested by the Extractor</span></span> | <span data-ttu-id="b723b-148">您提供</span><span class="sxs-lookup"><span data-stu-id="b723b-148">You Provide</span></span>                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| <span data-ttu-id="b723b-149">156x120</span><span class="sxs-lookup"><span data-stu-id="b723b-149">156x120</span></span>                        | <span data-ttu-id="b723b-150">256 x 256</span><span class="sxs-lookup"><span data-stu-id="b723b-150">256x256</span></span>                         | <span data-ttu-id="b723b-151">156x120 (不要填補、維持外觀比例) </span><span class="sxs-lookup"><span data-stu-id="b723b-151">156x120 (Do not pad, maintain aspect ratio)</span></span> |
| <span data-ttu-id="b723b-152">2048x1024</span><span class="sxs-lookup"><span data-stu-id="b723b-152">2048x1024</span></span>                      | <span data-ttu-id="b723b-153">256 x 256</span><span class="sxs-lookup"><span data-stu-id="b723b-153">256x256</span></span>                         | <span data-ttu-id="b723b-154">256x128 (不要填補、維持外觀比例) </span><span class="sxs-lookup"><span data-stu-id="b723b-154">256x128 (Do not pad, maintain aspect ratio)</span></span> |



 

<span data-ttu-id="b723b-155">您可以在登錄中將截止點宣告為相關聯應用程式的程式識別碼專案的一部分。</span><span class="sxs-lookup"><span data-stu-id="b723b-155">You can declare a cutoff point as part of the program ID entry of the associated app in the registry.</span></span> <span data-ttu-id="b723b-156">在此大小以下時，不會使用縮圖。</span><span class="sxs-lookup"><span data-stu-id="b723b-156">Below this size, thumbnails are not used.</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

<span data-ttu-id="b723b-157">ThumbnailCutoff 專案是這些 REG DWORD 值的其中一個 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b723b-157">The ThumbnailCutoff entry is one of these REG\_DWORD values.</span></span>

| <span data-ttu-id="b723b-158">值</span><span class="sxs-lookup"><span data-stu-id="b723b-158">Value</span></span> | <span data-ttu-id="b723b-159">Cutoff</span><span class="sxs-lookup"><span data-stu-id="b723b-159">Cutoff</span></span> | <span data-ttu-id="b723b-160">HighDPI 敏感性</span><span class="sxs-lookup"><span data-stu-id="b723b-160">HighDPI Sensitive</span></span> |
|-------|--------|-------------------|
| <span data-ttu-id="b723b-161">0</span><span class="sxs-lookup"><span data-stu-id="b723b-161">0</span></span>     | <span data-ttu-id="b723b-162">32x32</span><span class="sxs-lookup"><span data-stu-id="b723b-162">32x32</span></span>  | <span data-ttu-id="b723b-163">是</span><span class="sxs-lookup"><span data-stu-id="b723b-163">Yes</span></span>               |
| <span data-ttu-id="b723b-164">1</span><span class="sxs-lookup"><span data-stu-id="b723b-164">1</span></span>     | <span data-ttu-id="b723b-165">16x16</span><span class="sxs-lookup"><span data-stu-id="b723b-165">16x16</span></span>  | <span data-ttu-id="b723b-166">Yes</span><span class="sxs-lookup"><span data-stu-id="b723b-166">Yes</span></span>               |
| <span data-ttu-id="b723b-167">2</span><span class="sxs-lookup"><span data-stu-id="b723b-167">2</span></span>     | <span data-ttu-id="b723b-168">48x48</span><span class="sxs-lookup"><span data-stu-id="b723b-168">48x48</span></span>  | <span data-ttu-id="b723b-169">Yes</span><span class="sxs-lookup"><span data-stu-id="b723b-169">Yes</span></span>               |
| <span data-ttu-id="b723b-170">3</span><span class="sxs-lookup"><span data-stu-id="b723b-170">3</span></span>     | <span data-ttu-id="b723b-171">16x16</span><span class="sxs-lookup"><span data-stu-id="b723b-171">16x16</span></span>  | <span data-ttu-id="b723b-172">Yes</span><span class="sxs-lookup"><span data-stu-id="b723b-172">Yes</span></span>               |


<span data-ttu-id="b723b-173">每英寸的高點 (DPI) 敏感度表示縮圖的圖元尺寸會自動調整為較大的 DPI。</span><span class="sxs-lookup"><span data-stu-id="b723b-173">High dots per inch (dpi) sensitivity means that the pixel dimensions of the thumbnail automatically adjust for the greater dpi.</span></span> <span data-ttu-id="b723b-174">例如，在 96 DPI 的32x32 影像會是 120 DPI 的40x40 影像。</span><span class="sxs-lookup"><span data-stu-id="b723b-174">For instance, a 32x32 image at 96 dpi would be a 40x40 image at 120 dpi.</span></span>

<span data-ttu-id="b723b-175">如果未指定 ThumbnailCutoff 專案，預設的截止值會是 20x20 (不會區分 DPI) 。</span><span class="sxs-lookup"><span data-stu-id="b723b-175">If the ThumbnailCutoff entry is not specified, the default cutoff is 20x20 (not dpi-sensitive).</span></span>

## <a name="thumbnail-overlays"></a><span data-ttu-id="b723b-176">縮圖覆蓋</span><span class="sxs-lookup"><span data-stu-id="b723b-176">Thumbnail Overlays</span></span>

<span data-ttu-id="b723b-177">縮圖覆迭是在縮圖右下角顯示的小型影像，讓開發人員有機會將品牌辨識套用至縮圖。</span><span class="sxs-lookup"><span data-stu-id="b723b-177">Thumbnail overlays, a small image displayed over the lower right corner of the thumbnail, provide an opportunity for developers to apply brand identification to their thumbnails.</span></span> <span data-ttu-id="b723b-178">覆迭會在登錄中宣告為相關聯應用程式的程式識別碼專案的一部分，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b723b-178">Overlays are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

<span data-ttu-id="b723b-179">TypeOverlay 專案包含的 REG \_ SZ 值會解讀如下：</span><span class="sxs-lookup"><span data-stu-id="b723b-179">The TypeOverlay entry contains a REG\_SZ value interpreted as follows:</span></span>

-   <span data-ttu-id="b723b-180">如果此值是資源參考 (內嵌于 DLL 中的 **.ico** 檔案) 例如 `ISVComponent.dll,-155` ，該映射會用來做為具有該副檔名之檔案的覆迭。</span><span class="sxs-lookup"><span data-stu-id="b723b-180">If the value is a resource reference (a **.ico** file embedded in the DLL) such as `ISVComponent.dll,-155`, that image is used as the overlay for files with that file name extension.</span></span> <span data-ttu-id="b723b-181">請注意，在此範例中， **155** 是資源識別碼，如果 DLL 不存在於標準路徑中 (例如 **C：/Windows/System32**) ，則需要完整路徑，而不只是 dll 名稱。</span><span class="sxs-lookup"><span data-stu-id="b723b-181">Note that in this example, **155** is the resouce ID, and if the DLL is not present in a standard path (such as **C:/Windows/System32**), the full path is required instead of just the DLL name.</span></span>
-   <span data-ttu-id="b723b-182">如果此值為空字串，則不會對影像套用任何覆迭。</span><span class="sxs-lookup"><span data-stu-id="b723b-182">If the value is an empty string, no overlay is applied to the image.</span></span>
-   <span data-ttu-id="b723b-183">如果值不存在，則會使用相關聯應用程式的預設圖示。</span><span class="sxs-lookup"><span data-stu-id="b723b-183">If the value is not present, the default icon of the associated application is used.</span></span>

<span data-ttu-id="b723b-184">縮圖的重迭只能透過此機制提供，並由 Windows 套用。</span><span class="sxs-lookup"><span data-stu-id="b723b-184">Overlays for your thumbnails should only be provided through this mechanism and applied by Windows.</span></span> <span data-ttu-id="b723b-185">請勿自行套用覆迭。</span><span class="sxs-lookup"><span data-stu-id="b723b-185">Do not apply overlays yourself.</span></span>

## <a name="thumbnail-adornments"></a><span data-ttu-id="b723b-186">縮圖裝飾</span><span class="sxs-lookup"><span data-stu-id="b723b-186">Thumbnail Adornments</span></span>

<span data-ttu-id="b723b-187">像是陰影的裝飾會根據使用者目前選取的主題套用至縮圖。</span><span class="sxs-lookup"><span data-stu-id="b723b-187">Adornments such as drop shadows are applied to thumbnails based on the user's currently selected theme.</span></span> <span data-ttu-id="b723b-188">裝飾是由 Windows 提供;請勿自行建立。</span><span class="sxs-lookup"><span data-stu-id="b723b-188">Adornments are provided by Windows; do not create them yourself.</span></span> <span data-ttu-id="b723b-189">Windows 可能會隨時變更特定裝飾的外觀，因此，如果您擁有自己的擁有者，就會發生與系統同步的風險。</span><span class="sxs-lookup"><span data-stu-id="b723b-189">Windows could change the look of particular adornments at any time, so if you provided you own you would risk falling out of sync with the system.</span></span> <span data-ttu-id="b723b-190">您的縮圖可能會看似已過期或不存在。</span><span class="sxs-lookup"><span data-stu-id="b723b-190">Your thumbnails could wind up looking dated or out of place.</span></span>

<span data-ttu-id="b723b-191">可能的裝飾會在登錄中宣告為相關聯應用程式的程式識別碼專案的一部分，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b723b-191">Potential adornments are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

<span data-ttu-id="b723b-192">處理專案包含下列其中一個 REG \_ DWORD 值：</span><span class="sxs-lookup"><span data-stu-id="b723b-192">The Treatment entry contains one of these REG\_DWORD values:</span></span>



| <span data-ttu-id="b723b-193">值</span><span class="sxs-lookup"><span data-stu-id="b723b-193">Value</span></span> | <span data-ttu-id="b723b-194">意義</span><span class="sxs-lookup"><span data-stu-id="b723b-194">Meaning</span></span>         |
|-------|-----------------|
| <span data-ttu-id="b723b-195">0</span><span class="sxs-lookup"><span data-stu-id="b723b-195">0</span></span>     | <span data-ttu-id="b723b-196">無裝飾</span><span class="sxs-lookup"><span data-stu-id="b723b-196">No Adornment</span></span>    |
| <span data-ttu-id="b723b-197">1</span><span class="sxs-lookup"><span data-stu-id="b723b-197">1</span></span>     | <span data-ttu-id="b723b-198">陰影</span><span class="sxs-lookup"><span data-stu-id="b723b-198">Drop Shadow</span></span>     |
| <span data-ttu-id="b723b-199">2</span><span class="sxs-lookup"><span data-stu-id="b723b-199">2</span></span>     | <span data-ttu-id="b723b-200">相片框線</span><span class="sxs-lookup"><span data-stu-id="b723b-200">Photo Border</span></span>    |
| <span data-ttu-id="b723b-201">3</span><span class="sxs-lookup"><span data-stu-id="b723b-201">3</span></span>     | <span data-ttu-id="b723b-202">影片 Sprockets</span><span class="sxs-lookup"><span data-stu-id="b723b-202">Video Sprockets</span></span> |


<span data-ttu-id="b723b-203">根據預設，陰影會套用至影像。</span><span class="sxs-lookup"><span data-stu-id="b723b-203">A drop shadow is applied to images by default.</span></span>

## <a name="registering-your-thumbnail-handler"></a><span data-ttu-id="b723b-204">註冊您的縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="b723b-204">Registering Your Thumbnail Handler</span></span>

<span data-ttu-id="b723b-205">縮圖處理常式的註冊是以標準檔案關聯為基礎。</span><span class="sxs-lookup"><span data-stu-id="b723b-205">Registration of a thumbnail handler is based on standard file associations.</span></span>

<span data-ttu-id="b723b-206">縮圖處理常式 Shell 延伸模組的 GUID 為 `E357FCCD-A995-4576-B01F-234630154E96` 。</span><span class="sxs-lookup"><span data-stu-id="b723b-206">The GUID for the thumbnail handler Shell extension is `E357FCCD-A995-4576-B01F-234630154E96`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b723b-207">相關主題</span><span class="sxs-lookup"><span data-stu-id="b723b-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b723b-208">**IThumbnailProvider**</span><span class="sxs-lookup"><span data-stu-id="b723b-208">**IThumbnailProvider**</span></span>](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[<span data-ttu-id="b723b-209">建立縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="b723b-209">Building Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="b723b-210">縮圖處理常式指導方針</span><span class="sxs-lookup"><span data-stu-id="b723b-210">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



