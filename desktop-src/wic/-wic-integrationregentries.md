---
description: 本主題適用于 Windows Vista 和更新版本。
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: 與 Windows 影像中心和 Windows 檔案總管整合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994396"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a><span data-ttu-id="64004-103">與 Windows 影像中心和 Windows 檔案總管整合</span><span class="sxs-lookup"><span data-stu-id="64004-103">Integration with Windows Photo Gallery and Windows Explorer</span></span>

<span data-ttu-id="64004-104">本主題適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="64004-104">This topic applies to Windows Vista and later.</span></span> <span data-ttu-id="64004-105">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="64004-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="64004-106">簡介</span><span class="sxs-lookup"><span data-stu-id="64004-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="64004-107">與 Windows 屬性儲存區整合</span><span class="sxs-lookup"><span data-stu-id="64004-107">Integration with the Windows Property Store</span></span>](#integration-with-the-windows-property-store)
-   [<span data-ttu-id="64004-108">與 Windows 影像中心整合</span><span class="sxs-lookup"><span data-stu-id="64004-108">Integration with the Windows Photo Gallery</span></span>](#integration-with-the-windows-photo-gallery)
-   [<span data-ttu-id="64004-109">與 Windows 縮圖快取整合</span><span class="sxs-lookup"><span data-stu-id="64004-109">Integration with the Windows Thumbnail Cache</span></span>](#integration-with-the-windows-thumbnail-cache)
-   [<span data-ttu-id="64004-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="64004-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="64004-111">簡介</span><span class="sxs-lookup"><span data-stu-id="64004-111">Introduction</span></span>

<span data-ttu-id="64004-112">若要讓 Windows 影像中心和 Windows 檔案總管顯示縮圖和搜尋和更新標準影像中繼資料，編解碼器必須具有與其相關聯的 [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) 和 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的執行。</span><span class="sxs-lookup"><span data-stu-id="64004-112">To enable Windows Photo Gallery and Windows Explorer to display thumbnails and search and update standard image metadata, a codec must have an implementation of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) and [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces associated with it.</span></span> <span data-ttu-id="64004-113">IThumbnailProvider 介面是用來抓取縮圖並填入縮圖快取，而 IPropertyStore 介面是用來搜尋和更新與檔案相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="64004-113">The IThumbnailProvider interface is used to retrieve thumbnails and populate the thumbnail cache, and the IPropertyStore interface is used for searching and updating metadata associated with a file.</span></span> <span data-ttu-id="64004-114">在 Windows Vista 中，所有檔案類型都有縮圖和中繼資料，但不同的檔案類型需要這些介面的不同執行，以抓取或產生它們的縮圖和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="64004-114">As of Windows Vista, all file types have thumbnails and metadata, but different file types require different implementations of these interfaces to retrieve or generate the thumbnails and metadata for them.</span></span> <span data-ttu-id="64004-115">系統會提供這些介面的預設執行。</span><span class="sxs-lookup"><span data-stu-id="64004-115">The system provides default implementations of these interfaces.</span></span> <span data-ttu-id="64004-116">IThumbnailProvider 的預設執行可用於任何 Windows 影像處理元件 (WIC) 啟用的映射格式。</span><span class="sxs-lookup"><span data-stu-id="64004-116">The default implementation of IThumbnailProvider can be used for any Windows Imaging Component (WIC)–enabled image format.</span></span> <span data-ttu-id="64004-117">IPropertyStore 的預設執行可搭配任何已啟用 WIC 的映射格式使用，此格式以標記的影像檔案格式為基礎， (TIFF) 或 JPEG 容器。</span><span class="sxs-lookup"><span data-stu-id="64004-117">The default implementation of IPropertyStore can be used with any WIC-enabled image format that is based on a Tagged Image File Format (TIFF) or JPEG container.</span></span> <span data-ttu-id="64004-118">若要將映射格式與這兩個介面的預設執行建立關聯，您必須只新增一些登錄專案。</span><span class="sxs-lookup"><span data-stu-id="64004-118">To associate your image format with the default implementations of both of these interfaces, you must add just a few registry entries.</span></span>

<span data-ttu-id="64004-119">下列專案指出 Windows 影像中心，並 Windows 檔案總管副檔名 () 及其相關聯的 MIME 類型與影像格式相關聯。</span><span class="sxs-lookup"><span data-stu-id="64004-119">The following entries indicate to the Windows Photo Gallery and Windows Explorer that a file name extension (.ext) and its associated MIME type are associated with an image format.</span></span>

<span data-ttu-id="64004-120">下列專案表示使用內容類型 (也稱為 mime 類型的 Windows 和應用程式) 具有指定副檔名 ( 的檔案。 ext) 是影像格式。</span><span class="sxs-lookup"><span data-stu-id="64004-120">The following entry indicates to Windows and applications that use content type (also known as mime type) that a file with a given extension (.ext) is an image format.</span></span> <span data-ttu-id="64004-121">檔案類型擁有者必須選擇可 `<image sub type value>` 唯一識別檔案格式的，且此內容類型值必須向 IANA 註冊。</span><span class="sxs-lookup"><span data-stu-id="64004-121">The file type owner needs to choose a `<image sub type value>` that uniquely identifies the file format and this content type value needs to be register with IANA.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

<span data-ttu-id="64004-122">下列專案 [指出使用 system.string 的 windows](../properties/props-system-kind.md) 、windows 搜尋和應用程式（副檔名)  (）應該視為一張圖片。</span><span class="sxs-lookup"><span data-stu-id="64004-122">The following entry indicates to Windows, Windows search and applications that use [System.Kind](../properties/props-system-kind.md) that a file name extension (.ext) should be treated as a picture.</span></span> <span data-ttu-id="64004-123">具體而言，它會指出副檔名的 System.object 屬性應該設定為 Picture。</span><span class="sxs-lookup"><span data-stu-id="64004-123">Specifically, it indicates that the file extension’s System.Kind property should be set to Picture.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a><span data-ttu-id="64004-124">與 Windows 屬性儲存區整合</span><span class="sxs-lookup"><span data-stu-id="64004-124">Integration with the Windows Property Store</span></span>

<span data-ttu-id="64004-125">有時候，相同的中繼資料屬性會在不同的中繼資料架構中公開，通常會有不同的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="64004-125">Sometimes the same metadata properties are exposed in different metadata schemas, often with different property names.</span></span> <span data-ttu-id="64004-126">當更新其中一個屬性，但其他屬性不是時，檔案內的中繼資料可能會不同步。Photo 屬性處理常式會提供映射的預設 **IPropertyStore** 執行，並由應用程式以及 windows 影像中心和 Windows 檔案總管確保影像中的所有中繼資料都保持同步，而且應用程式所顯示的屬性與 Windows 影像中心和 Windows 檔案總管所顯示的屬性一致。</span><span class="sxs-lookup"><span data-stu-id="64004-126">When one of these properties is updated, but the others are not, the metadata within the file can get out of sync. The photo property handler provides the default **IPropertyStore** implementation for images, and is used by applications as well as by the Windows Photo Gallery and Windows Explorer to ensure that all the metadata in an image stays in sync, and that the properties displayed by applications are consistent with those displayed by the Windows Photo Gallery and Windows Explorer.</span></span> <span data-ttu-id="64004-127">當相片屬性處理常式更新中繼資料時，會確定這些屬性會在檔案中的所有通用元資料格式中一致更新。</span><span class="sxs-lookup"><span data-stu-id="64004-127">When the photo property handler updates metadata, it makes sure that these properties are updated consistently across all the common metadata formats that are present in the file.</span></span>

<span data-ttu-id="64004-128">Photo 屬性處理常式必須瞭解容器格式，以及如何找出其內的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="64004-128">The photo property handler must understand the container format and how to locate the various properties within it.</span></span> <span data-ttu-id="64004-129">一般而言，相片屬性處理常式不可能知道如何以專屬的容器格式來配置各種不同的中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="64004-129">In general, it isn’t possible for the photo property handler to know how the various metadata blocks are laid out in a proprietary container format.</span></span> <span data-ttu-id="64004-130">但是，如果您的容器格式中繼資料的配置方式與 TIFF 容器格式或 JPEG 容器格式的中繼資料相同，則相片屬性處理常式也可以利用該知識，以一致的方式更新您的容器格式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="64004-130">However, if the metadata in your container format is laid out the same way as the metadata in either a TIFF container format or a JPEG container format, the photo property handler can take advantage of that knowledge to update metadata consistently in your container format as well.</span></span>

<span data-ttu-id="64004-131">您可以藉由建立下列登錄專案來註冊此關聯。</span><span class="sxs-lookup"><span data-stu-id="64004-131">You can register this association by creating the following registry entry.</span></span> <span data-ttu-id="64004-132">此專案會通知相片屬性處理常式，此 GUID 所識別的容器格式可理解與具有 GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 的容器格式相同的中繼資料查詢語言路徑。</span><span class="sxs-lookup"><span data-stu-id="64004-132">This entry notifies the photo property handler that the container format identified by this GUID understands the same metadata query language paths as the container format with the GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span></span> <span data-ttu-id="64004-133"> (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 是 TIFF 容器格式的 GUID。 ) </span><span class="sxs-lookup"><span data-stu-id="64004-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 is the GUID for the TIFF container format.)</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

<span data-ttu-id="64004-134">下列專案會將相片屬性處理常式的預設實 **IPropertyStore** 與副檔名為 "ext" 的檔案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="64004-134">The following entry associates the photo property handler’s default implementation of **IPropertyStore** with files that have the extension ".ext".</span></span> <span data-ttu-id="64004-135">第一個 GUID 是 **IPropertyStore** 介面的 IID，而第二個則是相片屬性處理常式之執行的 guid。</span><span class="sxs-lookup"><span data-stu-id="64004-135">The first GUID is the IID of the **IPropertyStore** interface, and the second is the GUID of the photo property handler’s implementation of it.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

<span data-ttu-id="64004-136">使用與 TIFF 或 JPEG 容器格式不相容之專屬格式的編解碼器必須撰寫自己的 **IPropertyStore** 執行。</span><span class="sxs-lookup"><span data-stu-id="64004-136">Codecs that use a proprietary format that is not compatible with either the TIFF or JPEG container format must write their own **IPropertyStore** implementation.</span></span>

## <a name="integration-with-the-windows-photo-gallery"></a><span data-ttu-id="64004-137">與 Windows 影像中心整合</span><span class="sxs-lookup"><span data-stu-id="64004-137">Integration with the Windows Photo Gallery</span></span>

<span data-ttu-id="64004-138">Windows 影像中心是以 WIC 為基礎建立的，而且可以顯示已安裝任何已啟用 WIC 之編解碼器的映射格式。</span><span class="sxs-lookup"><span data-stu-id="64004-138">Windows Photo Gallery is built on WIC and can display any WIC-enabled image format for which the codec is installed.</span></span> <span data-ttu-id="64004-139">若要通知系統您的映射格式可在 Windows 影像中心中開啟，您必須建立下列登錄專案來建立檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="64004-139">To notify the system that your image format can be opened in Windows Photo Gallery, you need to create a file association by creating the following registry entries.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

<span data-ttu-id="64004-140">ProgID 通常是附加在 "file" 這個字的副檔名。</span><span class="sxs-lookup"><span data-stu-id="64004-140">The ProgID is usually the file name extension appended with the word "file".</span></span> <span data-ttu-id="64004-141"> (例如，如果副檔名為 .txt，則 ProgID 通常會是 "txtfile"。 ) </span><span class="sxs-lookup"><span data-stu-id="64004-141">(For example, if the file name extension is .txt, the ProgID would usually be "txtfile".)</span></span>

<span data-ttu-id="64004-142">您可能需要建立其他標準登錄專案來支援檔案關聯;不過，因為 the'y 不是 WIC 專屬的，所以它們已超出本主題的範圍。</span><span class="sxs-lookup"><span data-stu-id="64004-142">There are other standard registry entries you may need to create to support file associations; however, because the’y are not specific to WIC, they are beyond the scope of this topic.</span></span>

## <a name="integration-with-the-windows-thumbnail-cache"></a><span data-ttu-id="64004-143">與 Windows 縮圖快取整合</span><span class="sxs-lookup"><span data-stu-id="64004-143">Integration with the Windows Thumbnail Cache</span></span>

<span data-ttu-id="64004-144">下列兩個專案表示標準 WIC 縮圖提供者實作為此副檔名的檔案，可以用來取得縮圖。</span><span class="sxs-lookup"><span data-stu-id="64004-144">The following two entries indicate that the standard WIC thumbnail provider implementation can be used to retrieve thumbnails for files with this extension.</span></span> <span data-ttu-id="64004-145">第一個 GUID 是 [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) 介面的 IID，而第二個 guid 是此介面標準系統實作為的 guid。</span><span class="sxs-lookup"><span data-stu-id="64004-145">The first GUID is the IID of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) interface, and the second is the GUID of the standard system implementation of this interface.</span></span> <span data-ttu-id="64004-146"> (HLCR 下的所有專案 \\ \\ 都會在 \\ HKCR \\ SystemFileAssociations \\ . ext ShellEx 下重複 \\ 。 \\ ) </span><span class="sxs-lookup"><span data-stu-id="64004-146">(All entries under HLCR\\.ext\\ShellEx\\ are repeated under HKCR\\SystemFileAssociations\\.ext\\ShellEx\\.)</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a><span data-ttu-id="64004-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="64004-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64004-148">**概念**</span><span class="sxs-lookup"><span data-stu-id="64004-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="64004-149">編碼器特定的登錄專案</span><span class="sxs-lookup"><span data-stu-id="64004-149">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="64004-150">編解碼器安裝和註冊</span><span class="sxs-lookup"><span data-stu-id="64004-150">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="64004-151">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="64004-151">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="64004-152">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="64004-152">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
