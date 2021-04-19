---
description: Encoder-Specific 登錄專案
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific 登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984589"
---
# <a name="encoder-specific-registry-entries"></a><span data-ttu-id="3070b-103">Encoder-Specific 登錄專案</span><span class="sxs-lookup"><span data-stu-id="3070b-103">Encoder-Specific Registry Entries</span></span>


<span data-ttu-id="3070b-104">除了上述針對編碼器所列的專案之外，您還必須在 Windows 影像處理元件 (WIC) 編碼器的類別下註冊您的編碼器，讓探索引擎可以找到它。</span><span class="sxs-lookup"><span data-stu-id="3070b-104">In addition to the entries listed above for encoder, you must also register your encoder under the category of Windows Imaging Component (WIC) encoders so the discovery engine can find it.</span></span> <span data-ttu-id="3070b-105">您可以藉由建立下列登錄專案來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="3070b-105">You do this by making the following registry entries.</span></span> <span data-ttu-id="3070b-106">下列專案中的第一個 GUID 是 WICBitmapEncoders)  (CATID 的分類識別碼。</span><span class="sxs-lookup"><span data-stu-id="3070b-106">The first GUID in the following entries is the category identifier (CATID) for WICBitmapEncoders.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a><span data-ttu-id="3070b-107">使用中繼資料寫入器註冊容器格式</span><span class="sxs-lookup"><span data-stu-id="3070b-107">Registering a Container Format with Metadata Writers</span></span>

<span data-ttu-id="3070b-108">如果您為編解碼器建立新的容器格式，則也必須建立登錄專案，以支援您影像中中繼資料區塊的中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="3070b-108">If you create a new container format for your codec, you must also create registry entries to support metadata writers for the metadata blocks in your images.</span></span> <span data-ttu-id="3070b-109">下列專案必須根據您的容器格式所支援的每個元資料格式，在中繼資料寫入器 (CLSID) 的類別識別碼底下建立。</span><span class="sxs-lookup"><span data-stu-id="3070b-109">The following entries need to be created under the class identifier (CLSID) of the metadata writer for each metadata format supported in your container format.</span></span> <span data-ttu-id="3070b-110">如果您的編解碼器使用標記的影像檔案格式 (TIFF) 容器，則這項資訊已在登錄中，因此您不需要建立這些專案。</span><span class="sxs-lookup"><span data-stu-id="3070b-110">If your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry and you don't need to create these entries.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

<span data-ttu-id="3070b-111">如果您使用 TIFF 樣式或 JPEG 樣式的容器格式，則必須在容器與該容器格式之間註冊關聯。</span><span class="sxs-lookup"><span data-stu-id="3070b-111">If you use a TIFF-style or JPEG-style container format, you must register an association between your container and that container format.</span></span> <span data-ttu-id="3070b-112">如需詳細資訊，請參閱 [整合 Windows 影像中心和 Windows 檔案總管](-wic-integrationregentries.md)的簡介。</span><span class="sxs-lookup"><span data-stu-id="3070b-112">For more information, see the introduction in [Integration with Windows Photo Gallery and Windows Explorer](-wic-integrationregentries.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3070b-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="3070b-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3070b-114">**概念**</span><span class="sxs-lookup"><span data-stu-id="3070b-114">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3070b-115">一般登錄專案</span><span class="sxs-lookup"><span data-stu-id="3070b-115">General Registry Entries</span></span>](-wic-generalregentries.md)
</dt> <dt>

[<span data-ttu-id="3070b-116">編碼器特定的登錄專案</span><span class="sxs-lookup"><span data-stu-id="3070b-116">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="3070b-117">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="3070b-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="3070b-118">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="3070b-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



