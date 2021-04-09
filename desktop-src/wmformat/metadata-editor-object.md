---
title: 中繼資料編輯器物件
description: 中繼資料編輯器物件
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Media Format SDK，中繼資料編輯器物件
- Advanced Systems Format (ASF) 的中繼資料編輯器物件
- ASF (Advanced 系統格式) ，中繼資料編輯器物件
- 物件，中繼資料編輯器物件
- 中繼資料編輯器物件，關於
- 中繼資料、編輯器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681557"
---
# <a name="metadata-editor-object"></a><span data-ttu-id="57b33-109">中繼資料編輯器物件</span><span class="sxs-lookup"><span data-stu-id="57b33-109">Metadata Editor Object</span></span>

<span data-ttu-id="57b33-110">中繼資料編輯器物件是用來編輯儲存在 ASF 檔案標頭區段中的資訊。</span><span class="sxs-lookup"><span data-stu-id="57b33-110">The metadata editor object is used to edit information stored in the header section of ASF files.</span></span> <span data-ttu-id="57b33-111">此物件最常操作的專案是中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="57b33-111">The most common things manipulated by this object are metadata attributes.</span></span> <span data-ttu-id="57b33-112">此外，中繼資料編輯器會處理 [*標記*](wmformat-glossary.md) 和指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="57b33-112">Additionally, the metadata editor deals with [*markers*](wmformat-glossary.md) and script commands.</span></span> <span data-ttu-id="57b33-113">只有當您想要編輯現有檔案的標頭而不播放時，才需要使用 [中繼資料編輯器]。</span><span class="sxs-lookup"><span data-stu-id="57b33-113">The only time you need to use the metadata editor is when you want to edit the header of an existing file without playing it.</span></span>

<span data-ttu-id="57b33-114">中繼資料編輯器物件是由函式 [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)所建立，它會將指標設定為 **IWMMetadataEditor** 介面。</span><span class="sxs-lookup"><span data-stu-id="57b33-114">The metadata editor object is created by the function [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), which sets a pointer to an **IWMMetadataEditor** interface.</span></span> <span data-ttu-id="57b33-115">您可以藉由呼叫 **QueryInterface** 方法，取得中繼資料編輯器物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="57b33-115">The other interfaces of the metadata editor object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="57b33-116">中繼資料編輯器物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="57b33-116">The following interfaces are supported by the metadata editor object.</span></span>



| <span data-ttu-id="57b33-117">介面</span><span class="sxs-lookup"><span data-stu-id="57b33-117">Interface</span></span>                                        | <span data-ttu-id="57b33-118">描述</span><span class="sxs-lookup"><span data-stu-id="57b33-118">Description</span></span>                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57b33-119">**IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="57b33-119">**IWMDRMEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | <span data-ttu-id="57b33-120">可讓編輯應用程式檢查 ASF 檔案的 [*DRM*](wmformat-glossary.md) 屬性，而不需要任何許可權來播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="57b33-120">Enables editing applications to examine the [*DRM*](wmformat-glossary.md) properties of an ASF file without having any rights to play the protected content.</span></span> |
| [<span data-ttu-id="57b33-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="57b33-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="57b33-122">操縱標頭中的屬性、標記和指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="57b33-122">Manipulates attributes, markers, and script commands in the header.</span></span>                                                                                                                                    |
| [<span data-ttu-id="57b33-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="57b33-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | <span data-ttu-id="57b33-124">抓取編解碼器資訊。</span><span class="sxs-lookup"><span data-stu-id="57b33-124">Retrieves codec information.</span></span> <span data-ttu-id="57b33-125">繼承 **IWMHeaderInfo** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="57b33-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                                                         |
| [<span data-ttu-id="57b33-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="57b33-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | <span data-ttu-id="57b33-127">提供屬性的先進支援，包括大型屬性、多語言和重複的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="57b33-127">Provides advanced support for attributes, including large attributes, multiple languages, and duplicate attribute names.</span></span> <span data-ttu-id="57b33-128">繼承 **IWMHeaderInfo** 和 **IWMHeaderInfo2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="57b33-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>      |
| [<span data-ttu-id="57b33-129">**IWMMetadataEditor**</span><span class="sxs-lookup"><span data-stu-id="57b33-129">**IWMMetadataEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | <span data-ttu-id="57b33-130">開啟、關閉，並將變更儲存至 ASF 檔案的標頭。</span><span class="sxs-lookup"><span data-stu-id="57b33-130">Opens, closes, and saves changes to the header of an ASF file.</span></span>                                                                                                                                         |
| [<span data-ttu-id="57b33-131">**IWMMetadataEditor2**</span><span class="sxs-lookup"><span data-stu-id="57b33-131">**IWMMetadataEditor2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | <span data-ttu-id="57b33-132">使用多個檔案存取和共用選項開啟 ASF 檔案以進行標頭編輯。</span><span class="sxs-lookup"><span data-stu-id="57b33-132">Opens an ASF file for header editing with multiple file access and sharing options.</span></span> <span data-ttu-id="57b33-133">繼承 **IWMMetadataEditor** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="57b33-133">Inherits all of the methods of **IWMMetadataEditor**.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="57b33-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="57b33-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57b33-135">**標記**</span><span class="sxs-lookup"><span data-stu-id="57b33-135">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="57b33-136">**中繼資料**</span><span class="sxs-lookup"><span data-stu-id="57b33-136">**Metadata**</span></span>](metadata.md)
</dt> <dt>

[<span data-ttu-id="57b33-137">**物件**</span><span class="sxs-lookup"><span data-stu-id="57b33-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="57b33-138">**指令碼命令**</span><span class="sxs-lookup"><span data-stu-id="57b33-138">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="57b33-139">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="57b33-139">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




