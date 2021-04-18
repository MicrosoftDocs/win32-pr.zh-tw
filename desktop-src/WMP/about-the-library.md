---
title: 關於程式庫
description: 關於程式庫
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player 程式庫，關於
- 程式庫，關於
- 中繼資料，Windows Media Player 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965772"
---
# <a name="about-the-library"></a><span data-ttu-id="fa14e-113">關於程式庫</span><span class="sxs-lookup"><span data-stu-id="fa14e-113">About the Library</span></span>

<span data-ttu-id="fa14e-114">程式庫是有關可 Windows Media Player 之數位媒體內容的資訊或 *中繼資料* 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="fa14e-114">The library is a database of information, or *metadata*, about the digital media content that is available to Windows Media Player.</span></span> <span data-ttu-id="fa14e-115">部分資訊會顯示在播放程式的 [連結 **庫** ] 窗格中;它有更多可透過程式碼來使用。</span><span class="sxs-lookup"><span data-stu-id="fa14e-115">Some of the information is displayed in the **Library** pane in the Player; more of it is available through code.</span></span>

<span data-ttu-id="fa14e-116"> (在 Windows Media Player 9 系列及更早版本中，這項功能稱為 **Media Library**。 ) </span><span class="sxs-lookup"><span data-stu-id="fa14e-116">(In Windows Media Player 9 Series and earlier, this feature is called **Media Library**.)</span></span>

<span data-ttu-id="fa14e-117">程式庫可讓使用者輕鬆地組織及存取數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="fa14e-117">The library gives users an easy way to organize and access digital media content.</span></span> <span data-ttu-id="fa14e-118">例如，使用者可以依專輯、演出者、內容類型或單純的所有音樂清單，來查看所組織的音樂。</span><span class="sxs-lookup"><span data-stu-id="fa14e-118">For example, users can view music organized by album, by artist, by genre, or simply as a list of all music.</span></span> <span data-ttu-id="fa14e-119">您可以使用 Windows Media Player SDK 物件模型來存取程式庫，以播放內容、取出播放清單、新增內容、移除內容，以及變更相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fa14e-119">You can use the Windows Media Player SDK object model to access the library to play content, retrieve playlists, add content, remove content, and change the associated metadata.</span></span> <span data-ttu-id="fa14e-120">Windows Media Player 在某些情況下，限制從程式碼存取程式庫的能力，以保護使用者的隱私權。</span><span class="sxs-lookup"><span data-stu-id="fa14e-120">Windows Media Player protects users' privacy by restricting your ability to access the library from code under certain conditions.</span></span> <span data-ttu-id="fa14e-121">如需存取權限的詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="fa14e-121">For more information about access rights, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="fa14e-122">程式庫會儲存兩種基本數位媒體內容類型的相關中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fa14e-122">The library stores metadata about two basic types of digital media content.</span></span> <span data-ttu-id="fa14e-123">第一種類型的數位媒體專案是個別的內容檔案，例如音樂軌或相片。</span><span class="sxs-lookup"><span data-stu-id="fa14e-123">The first type, digital media items, are individual content files, such as a music track or a photo.</span></span> <span data-ttu-id="fa14e-124">第二種類型（播放清單）是代表數位媒體專案群組的檔案，通常是以指定的順序播放。</span><span class="sxs-lookup"><span data-stu-id="fa14e-124">The second type, playlists, are files that represent a group of digital media items, typically intended to be played in a specified order.</span></span> <span data-ttu-id="fa14e-125">與數位媒體內容相關聯的中繼資料會儲存為名稱/值配對。</span><span class="sxs-lookup"><span data-stu-id="fa14e-125">The metadata associated with digital media content is stored as name-value pairs.</span></span> <span data-ttu-id="fa14e-126">例如，描述執行歌曲之人員的中繼資料名稱為「演出者」，而與其相關聯的值通常是包含執行者名稱的文字字串。</span><span class="sxs-lookup"><span data-stu-id="fa14e-126">For example, the metadata that describes the person who performed a song is named "Artist" and the value associated with it typically is a text string containing the performer's name.</span></span> <span data-ttu-id="fa14e-127">每個唯一的中繼資料名稱稱為 *屬性*。</span><span class="sxs-lookup"><span data-stu-id="fa14e-127">Each unique metadata name is called an *attribute*.</span></span> <span data-ttu-id="fa14e-128">如需支援的屬性清單，請參閱 [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="fa14e-128">For a listing of supported attributes, see the [Attribute Reference](attribute-reference.md).</span></span> <span data-ttu-id="fa14e-129">如需在程式碼中使用屬性的詳細資訊，請參閱 [媒體專案屬性](media-item-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="fa14e-129">For information about using attributes in code, see [Media Item Attributes](media-item-attributes.md).</span></span>

<span data-ttu-id="fa14e-130">下列各節提供使用程式庫的詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="fa14e-130">The following sections provide more information about working with the library:</span></span>

-   [<span data-ttu-id="fa14e-131">以程式設計方式存取程式庫</span><span class="sxs-lookup"><span data-stu-id="fa14e-131">Accessing the Library Programmatically</span></span>](accessing-the-library-programmatically.md)
-   [<span data-ttu-id="fa14e-132">關於程式庫服務</span><span class="sxs-lookup"><span data-stu-id="fa14e-132">About Library Services</span></span>](about-library-services.md)

## <a name="related-topics"></a><span data-ttu-id="fa14e-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa14e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa14e-134">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="fa14e-134">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




