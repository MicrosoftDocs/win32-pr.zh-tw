---
title: 關於轉換流程
description: 關於轉換流程
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player，轉換流程
- Windows Media Player 外掛程式，轉換
- 外掛程式，轉換
- 轉換外掛程式，進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023059"
---
# <a name="about-the-conversion-process"></a><span data-ttu-id="95f60-107">關於轉換流程</span><span class="sxs-lookup"><span data-stu-id="95f60-107">About the Conversion Process</span></span>

<span data-ttu-id="95f60-108">在 Windows Media Player 具現化轉換外掛程式之後，程式會繼續進行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="95f60-108">After Windows Media Player instantiates the conversion plug-in, the process proceeds as follows:</span></span>

1.  <span data-ttu-id="95f60-109">播放機會呼叫 [IWMPConvert：： ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile)。</span><span class="sxs-lookup"><span data-stu-id="95f60-109">The Player calls [IWMPConvert::ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile).</span></span>
2.  <span data-ttu-id="95f60-110">外掛程式會將 *bstrInputFile* 參數中提供的檔案轉換成 ASF 格式。</span><span class="sxs-lookup"><span data-stu-id="95f60-110">The plug-in converts the file provided in the *bstrInputFile* parameter into an ASF format.</span></span>
3.  <span data-ttu-id="95f60-111">如果轉換因某些原因而失敗，外掛程式會傳回適當的失敗代碼，並停止處理常式。</span><span class="sxs-lookup"><span data-stu-id="95f60-111">If the conversion fails for some reason, the plug-in returns an appropriate failure code and the process stops.</span></span>
4.  <span data-ttu-id="95f60-112">如果轉換成功，外掛程式會將轉換後的檔案放入 *bstrDestinationFolder* 參數中提供的資料夾，並透過 *pbstrOutputFile* 參數傳回已轉換之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="95f60-112">If the conversion succeeds, the plug-in places the converted file into the folder provided in the *bstrDestinationFolder* parameter and returns the fully qualified path to the converted file through the *pbstrOutputFile* parameter.</span></span>
5.  <span data-ttu-id="95f60-113">外掛程式會從 **ConvertFile** 傳回成功碼。</span><span class="sxs-lookup"><span data-stu-id="95f60-113">The plug-in returns a success code from **ConvertFile**.</span></span>
6.  <span data-ttu-id="95f60-114">播放程式會將轉換過的檔案複製到使用者的 [音樂] 資料夾階層中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="95f60-114">The Player copies the converted file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="95f60-115">播放玩家複製檔案的確切位置，取決於內容。</span><span class="sxs-lookup"><span data-stu-id="95f60-115">Exactly where the Player copies the file to depends on content.</span></span> <span data-ttu-id="95f60-116">在這個過程中，播放程式可能會重新命名檔案。</span><span class="sxs-lookup"><span data-stu-id="95f60-116">As part of this process, the Player might rename the file.</span></span>
7.  <span data-ttu-id="95f60-117">播放程式會將原始 (未轉換的) 檔案複製到使用者的 [音樂] 資料夾階層中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="95f60-117">The Player copies the original (unconverted) file to a folder in the user's music folder hierarchy.</span></span> <span data-ttu-id="95f60-118">在這個過程中，播放程式可能會重新命名檔案。</span><span class="sxs-lookup"><span data-stu-id="95f60-118">As part of this process, the Player might rename the file.</span></span> <span data-ttu-id="95f60-119">這是使用者將內容從電腦同步處理到需要源檔案格式的裝置時，播放程式所使用的檔案複本。</span><span class="sxs-lookup"><span data-stu-id="95f60-119">This is the copy of the file that the Player uses when the user syncs the content from the computer to a device that requires the original file format.</span></span> <span data-ttu-id="95f60-120">這個檔案稱為「陰影檔案」（ *shadow file*）。</span><span class="sxs-lookup"><span data-stu-id="95f60-120">This file is called a *shadow file*.</span></span>
8.  <span data-ttu-id="95f60-121">播放機會將已轉換之檔案的相關資訊新增至文件庫。</span><span class="sxs-lookup"><span data-stu-id="95f60-121">The Player adds information about the converted file to the library.</span></span> <span data-ttu-id="95f60-122">這包括將 **ShadowFilePath** 屬性的值設定為儲存陰影檔的新位置。</span><span class="sxs-lookup"><span data-stu-id="95f60-122">This includes setting the value for the **ShadowFilePath** attribute to the new location where the shadow file is saved.</span></span>

<span data-ttu-id="95f60-123">如果您需要使用已轉換的檔案，您可以使用 **ContentDistributor** 和 **WM/UniqueFileIdentifier** 屬性，查詢程式庫以取得內容。</span><span class="sxs-lookup"><span data-stu-id="95f60-123">If you need to work with the converted file, you can query the library to retrieve the content by using the **ContentDistributor** and **WM/UniqueFileIdentifier** attributes.</span></span> <span data-ttu-id="95f60-124">如果您需要使用陰影檔案，您仍然必須取出已轉換之檔案的 **媒體** 物件，然後查詢 **ShadowFilePath** 屬性。</span><span class="sxs-lookup"><span data-stu-id="95f60-124">If you need to work with the shadow file, you must still retrieve the **Media** object for the converted file and then query for the **ShadowFilePath** attribute.</span></span> <span data-ttu-id="95f60-125">請參閱 [將中繼資料新增至轉換](adding-metadata-to-converted-files.md)的檔案。</span><span class="sxs-lookup"><span data-stu-id="95f60-125">See [Adding Metadata to Converted Files](adding-metadata-to-converted-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95f60-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="95f60-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f60-127">**關於轉換外掛程式**</span><span class="sxs-lookup"><span data-stu-id="95f60-127">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="95f60-128">**將中繼資料新增至轉換的檔案**</span><span class="sxs-lookup"><span data-stu-id="95f60-128">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="95f60-129">**讀取屬性值**</span><span class="sxs-lookup"><span data-stu-id="95f60-129">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="95f60-130">**ShadowFilePath 屬性**</span><span class="sxs-lookup"><span data-stu-id="95f60-130">**ShadowFilePath Attribute**</span></span>](shadowfilepath-attribute.md)
</dt> <dt>

[<span data-ttu-id="95f60-131">**WM/ContentDistributor 屬性**</span><span class="sxs-lookup"><span data-stu-id="95f60-131">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="95f60-132">**WM/UniqueFileIdentifier 屬性**</span><span class="sxs-lookup"><span data-stu-id="95f60-132">**WM/UniqueFileIdentifier Attribute**</span></span>](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




