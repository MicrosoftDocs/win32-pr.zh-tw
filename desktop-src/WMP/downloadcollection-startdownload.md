---
title: DownloadCollection. startDownload 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 StartDownload 方法會將下載排在佇列中。
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- startDownload 方法 Windows Media Player
- startDownload 方法 Windows Media Player，DownloadCollection 類別
- DownloadCollection 類別 Windows Media Player，startDownload 方法
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990958"
---
# <a name="downloadcollectionstartdownload-method"></a><span data-ttu-id="9e817-108">DownloadCollection. startDownload 方法</span><span class="sxs-lookup"><span data-stu-id="9e817-108">DownloadCollection.startDownload method</span></span>

> [!Note]  
> <span data-ttu-id="9e817-109">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="9e817-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9e817-110">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="9e817-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9e817-111">**StartDownload** 方法會將下載排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="9e817-111">The **startDownload** method queues a download.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e817-112">語法</span><span class="sxs-lookup"><span data-stu-id="9e817-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a><span data-ttu-id="9e817-113">參數</span><span class="sxs-lookup"><span data-stu-id="9e817-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e817-114">*sourceURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e817-114">*sourceURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e817-115">**字串** ，指定下載的 URL。</span><span class="sxs-lookup"><span data-stu-id="9e817-115">**String** specifying the URL of the download.</span></span>

</dd> <dt>

<span data-ttu-id="9e817-116">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e817-116">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e817-117">指定下載類型的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="9e817-117">**String** specifying the type of download.</span></span> <span data-ttu-id="9e817-118">包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9e817-118">Contains one of the following values.</span></span>



| <span data-ttu-id="9e817-119">值</span><span class="sxs-lookup"><span data-stu-id="9e817-119">Value</span></span>      | <span data-ttu-id="9e817-120">描述</span><span class="sxs-lookup"><span data-stu-id="9e817-120">Description</span></span>                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e817-121">背景資訊</span><span class="sxs-lookup"><span data-stu-id="9e817-121">background</span></span> | <span data-ttu-id="9e817-122"> (Windows XP 及更新版本。 ) 下載會在處理器時間變成可用時，做為背景進程。</span><span class="sxs-lookup"><span data-stu-id="9e817-122">(Windows XP and later.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="9e817-123">即使在 Windows Media Player 或 Windows XP 關閉時，下載狀態仍會保存。</span><span class="sxs-lookup"><span data-stu-id="9e817-123">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="9e817-124">即時</span><span class="sxs-lookup"><span data-stu-id="9e817-124">real time</span></span>  | <span data-ttu-id="9e817-125"> (所有支援的作業系統。 ) 下載會一次完成。</span><span class="sxs-lookup"><span data-stu-id="9e817-125">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="9e817-126">會話之間不會保存任何下載狀態。</span><span class="sxs-lookup"><span data-stu-id="9e817-126">No download states persist between sessions.</span></span>                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e817-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e817-127">Return value</span></span>

<span data-ttu-id="9e817-128">這個方法會傳回 **DownloadItem** 物件。</span><span class="sxs-lookup"><span data-stu-id="9e817-128">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e817-129">備註</span><span class="sxs-lookup"><span data-stu-id="9e817-129">Remarks</span></span>

<span data-ttu-id="9e817-130">當新的下載開始時，下載管理員會將它以專案的形式新增至起始下載的下載集合。</span><span class="sxs-lookup"><span data-stu-id="9e817-130">When a new download is started, Download Manager adds it as an item to the download collection that initiated the download.</span></span>

<span data-ttu-id="9e817-131">只有下列數位媒體格式可供下載：</span><span class="sxs-lookup"><span data-stu-id="9e817-131">Only the following digital media formats can be downloaded:</span></span>

-   <span data-ttu-id="9e817-132">進階系統格式 (ASF)</span><span class="sxs-lookup"><span data-stu-id="9e817-132">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="9e817-133">MP3</span><span class="sxs-lookup"><span data-stu-id="9e817-133">MP3</span></span>
-   <span data-ttu-id="9e817-134">Windows Media 音訊 (WMA)</span><span class="sxs-lookup"><span data-stu-id="9e817-134">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="9e817-135">Windows Media 視訊 (WMV)</span><span class="sxs-lookup"><span data-stu-id="9e817-135">Windows Media Video (WMV)</span></span>

<span data-ttu-id="9e817-136">*SourceURL* 參數不支援 Unicode 編碼字串。</span><span class="sxs-lookup"><span data-stu-id="9e817-136">The *sourceURL* parameter does not support Unicode-encoded strings.</span></span> <span data-ttu-id="9e817-137">它必須指向有效的內容。</span><span class="sxs-lookup"><span data-stu-id="9e817-137">It must point to valid content.</span></span> <span data-ttu-id="9e817-138">不支援重新導向。</span><span class="sxs-lookup"><span data-stu-id="9e817-138">Redirects are not supported.</span></span>

<span data-ttu-id="9e817-139">使用 Windows XP 時，會根據檔案層級的中繼資料值，將音訊檔案自動放入適當的「 **我的音樂** 」子資料夾。</span><span class="sxs-lookup"><span data-stu-id="9e817-139">When using Windows XP, audio files are automatically placed into appropriate **My Music** subfolders based upon file-level metadata values.</span></span> <span data-ttu-id="9e817-140">影片檔案會放入 \\ 我的音樂 \\ 下載 \\ *亂數* \\ *型* 別，其中 *亂數字* 是每個使用者 Windows Media Player 所產生的隨機值，而 *類型* 則為 "real time" 或 "background" （視下載類型而定）。</span><span class="sxs-lookup"><span data-stu-id="9e817-140">Video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by Windows Media Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="9e817-141">在 windows 98 和 windows Millennium Edition (ME) 中使用 Windows Media Player 9 系列時，會將音訊和影片檔案放入 \\ 我的音樂 \\ 下載的 \\ *亂數字* \\ *類型*，其中 *亂數字* 是播放程式為每位使用者產生的隨機值，而 *類型* 則為 "real time" 或 "background" （視下載類型而定）。</span><span class="sxs-lookup"><span data-stu-id="9e817-141">When using Windows Media Player 9 Series with Windows 98 and Windows Millennium Edition (ME), audio and video files are placed into \\My Music\\download\\*random number*\\*type*, where *random number* is a random value generated by the Player for each user, and *type* is either "real time" or "background", depending upon the download type.</span></span>

<span data-ttu-id="9e817-142">請注意，檔案可能會根據檔案中包含的中繼資料屬性，以及使用者在 [ **選項** ] 對話方塊中指定的規則來重新命名。</span><span class="sxs-lookup"><span data-stu-id="9e817-142">Note that files may be renamed based upon metadata attributes contained in the file and rules specified by the user in the **Options** dialog box.</span></span> <span data-ttu-id="9e817-143">未包含中繼資料的檔案（如 **專輯** 或 **演出者**）可能會移至標示為「未知演出者」或「未知專輯」的資料夾。</span><span class="sxs-lookup"><span data-stu-id="9e817-143">Files that don't contain metadata, such as **Album** or **Artist**, may be moved to folders labeled Unknown Artist or Unknown Album.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e817-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e817-144">Requirements</span></span>



| <span data-ttu-id="9e817-145">需求</span><span class="sxs-lookup"><span data-stu-id="9e817-145">Requirement</span></span> | <span data-ttu-id="9e817-146">值</span><span class="sxs-lookup"><span data-stu-id="9e817-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e817-147">版本</span><span class="sxs-lookup"><span data-stu-id="9e817-147">Version</span></span><br/> | <span data-ttu-id="9e817-148">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="9e817-148">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="9e817-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9e817-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e817-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e817-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e817-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e817-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e817-152">**DownloadCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="9e817-152">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="9e817-153">**DownloadItem 物件**</span><span class="sxs-lookup"><span data-stu-id="9e817-153">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





