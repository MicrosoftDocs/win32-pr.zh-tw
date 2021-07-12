---
description: 程式庫說明檔是定義程式庫的 XML 檔。
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: 程式庫描述架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a6da99820e81c55e5d705c72d4d0509ea271a4a
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581736"
---
# <a name="library-description-schema"></a><span data-ttu-id="46b0d-103">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="46b0d-103">Library Description Schema</span></span>

<span data-ttu-id="46b0d-104">程式庫說明檔是定義程式庫的 XML 檔。</span><span class="sxs-lookup"><span data-stu-id="46b0d-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="46b0d-105">程式庫會將本機和遠端儲存位置的專案匯總成 Windows 檔案總管中的單一視圖。</span><span class="sxs-lookup"><span data-stu-id="46b0d-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="46b0d-106">程式庫描述檔案會遵循程式庫描述架構，並儲存為連結 \* 庫-ms 檔案。</span><span class="sxs-lookup"><span data-stu-id="46b0d-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="46b0d-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="46b0d-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="46b0d-108">程式庫描述架構的總覽</span><span class="sxs-lookup"><span data-stu-id="46b0d-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="46b0d-109">命名空間版本控制</span><span class="sxs-lookup"><span data-stu-id="46b0d-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="46b0d-110">程式庫描述檔案的範例</span><span class="sxs-lookup"><span data-stu-id="46b0d-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="46b0d-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="46b0d-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="46b0d-112">程式庫描述架構的總覽</span><span class="sxs-lookup"><span data-stu-id="46b0d-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="46b0d-113">程式庫包含儲存在一或多個儲存位置中的檔案。</span><span class="sxs-lookup"><span data-stu-id="46b0d-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="46b0d-114">程式庫不會實際儲存這些檔案;相反地，他們會監視包含檔案的資料夾，並讓使用者以不同的方式存取和排列檔案。</span><span class="sxs-lookup"><span data-stu-id="46b0d-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="46b0d-115">例如，使用者可以將音樂檔案放在本機硬碟上的多個資料夾中，也可以在外部硬碟上。</span><span class="sxs-lookup"><span data-stu-id="46b0d-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="46b0d-116">使用 **音樂媒體** 櫃時，使用者可以同時存取所有的檔案，並以演出者名稱或專輯標題將其全部以單一群組進行排序。</span><span class="sxs-lookup"><span data-stu-id="46b0d-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="46b0d-117">程式庫描述架構包含三個主要部分，如下表所述：</span><span class="sxs-lookup"><span data-stu-id="46b0d-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



| <span data-ttu-id="46b0d-118">部分</span><span class="sxs-lookup"><span data-stu-id="46b0d-118">Part</span></span>                        | <span data-ttu-id="46b0d-119">描述</span><span class="sxs-lookup"><span data-stu-id="46b0d-119">Description</span></span>                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46b0d-120">一般程式庫資訊</span><span class="sxs-lookup"><span data-stu-id="46b0d-120">General library information</span></span> | <span data-ttu-id="46b0d-121">程式庫顯示給使用者時，Windows 檔案總管可以使用的程式庫相關資訊，例如名稱、擁有者、版本、圖示。</span><span class="sxs-lookup"><span data-stu-id="46b0d-121">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="46b0d-122">程式庫屬性</span><span class="sxs-lookup"><span data-stu-id="46b0d-122">Library properties</span></span>          | <span data-ttu-id="46b0d-123">描述程式庫的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="46b0d-123">One or more properties that describe the library.</span></span> <span data-ttu-id="46b0d-124">這些自訂屬性是程式庫特有的。</span><span class="sxs-lookup"><span data-stu-id="46b0d-124">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="46b0d-125">程式庫位置</span><span class="sxs-lookup"><span data-stu-id="46b0d-125">Library locations</span></span>           | <span data-ttu-id="46b0d-126">一或多個搜尋連接器，用來識別要包含在程式庫中的存放位置。</span><span class="sxs-lookup"><span data-stu-id="46b0d-126">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="46b0d-127">每個位置也可以有一組唯一的屬性。</span><span class="sxs-lookup"><span data-stu-id="46b0d-127">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="46b0d-128">Windows 7 中的程式庫檔案會儲存在已知的資料夾 FOLDERID 連結 \_ 庫中。</span><span class="sxs-lookup"><span data-stu-id="46b0d-128">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="46b0d-129">依預設，[FOLDERID 連結 \_ 庫] 資料夾位於% USERPROFILE% \\ AppData \\ 漫遊 \\ Microsoft \\ Windows 連結 \\ 庫。</span><span class="sxs-lookup"><span data-stu-id="46b0d-129">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="46b0d-130">命名空間版本控制</span><span class="sxs-lookup"><span data-stu-id="46b0d-130">Namespace Versioning</span></span>

<span data-ttu-id="46b0d-131">程式庫描述檔案格式 (程式庫 \* -ms) 的版本是藉由變更命名空間來追蹤。</span><span class="sxs-lookup"><span data-stu-id="46b0d-131">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="46b0d-132">針對 Windows 7，檔案格式具有下列預設命名空間： https://schemas.microsoft.com/windows/2009/library 。</span><span class="sxs-lookup"><span data-stu-id="46b0d-132">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="46b0d-133">不過，您可以使用特定程式庫描述檔案中的專案來追蹤文件庫內容的版本 [<version>](schema-library-version.md) 。</span><span class="sxs-lookup"><span data-stu-id="46b0d-133">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="46b0d-134">程式庫描述檔案的範例</span><span class="sxs-lookup"><span data-stu-id="46b0d-134">Example of a Library Description File</span></span>

<span data-ttu-id="46b0d-135">以下是程式庫描述檔案的範例，此檔案會定義檔檔案的程式庫。</span><span class="sxs-lookup"><span data-stu-id="46b0d-135">The following is an example of a Library Description file that defines a library for document files.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="46b0d-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="46b0d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46b0d-137">folderType 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-137">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="46b0d-138">iconReference 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-138">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="46b0d-139">isLibraryPinned 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-139">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="46b0d-140">libraryDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-140">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="46b0d-141"> (程式庫架構的 name 元素) </span><span class="sxs-lookup"><span data-stu-id="46b0d-141">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="46b0d-142">ownerSID 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-142">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="46b0d-143">property 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-143">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="46b0d-144">propertyStore 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-144">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="46b0d-145">searchConnectorDescription 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-145">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="46b0d-146">searchConnectorDescriptionList 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-146">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="46b0d-147">templateInfo 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-147">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="46b0d-148">version 元素 (程式庫架構) </span><span class="sxs-lookup"><span data-stu-id="46b0d-148">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="46b0d-149">搜尋連接器描述架構</span><span class="sxs-lookup"><span data-stu-id="46b0d-149">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
