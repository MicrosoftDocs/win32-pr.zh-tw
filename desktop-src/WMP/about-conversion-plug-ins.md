---
title: 關於轉換外掛程式
description: 關於轉換外掛程式
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player，轉換外掛程式
- Windows Media Player 外掛程式，轉換
- 外掛程式，轉換
- 轉換外掛程式，關於
- 進階系統格式 (ASF)
- 'ASF (Advanced Systems 格式) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671568"
---
# <a name="about-conversion-plug-ins"></a><span data-ttu-id="5c613-109">關於轉換外掛程式</span><span class="sxs-lookup"><span data-stu-id="5c613-109">About Conversion Plug-ins</span></span>

<span data-ttu-id="5c613-110">您可以建立 Windows Media Player 外掛程式，將使用 Microsoft 未提供的技術所建立的數位媒體檔案轉換成 Advanced Systems 格式 (ASF) 。</span><span class="sxs-lookup"><span data-stu-id="5c613-110">You can create a Windows Media Player plug-in to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="5c613-111">轉換外掛程式是元件物件模型 (COM) 物件，這些物件會封裝並散發為可執行檔 ( .exe) 檔。</span><span class="sxs-lookup"><span data-stu-id="5c613-111">Conversion plug-ins are Component Object Model (COM) objects that are packaged and distributed as executable (.exe) files.</span></span> <span data-ttu-id="5c613-112">在下列案例中，Windows Media Player 具現化轉換外掛程式以轉換協力廠商數位媒體格式：</span><span class="sxs-lookup"><span data-stu-id="5c613-112">Windows Media Player instantiates conversion plug-ins to convert third-party digital media formats in the following scenarios:</span></span>

-   <span data-ttu-id="5c613-113">數位媒體內容會從可攜式裝置複製到電腦上。</span><span class="sxs-lookup"><span data-stu-id="5c613-113">Digital media content is copied to the computer from a portable device.</span></span>
-   <span data-ttu-id="5c613-114">使用 **IWMPMediaCollection：： add**，將數位媒體內容新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="5c613-114">Digital media content is added to the library by using **IWMPMediaCollection::add**.</span></span>
-   <span data-ttu-id="5c613-115">數位媒體內容會使用 Windows Media Player 的搜尋功能新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="5c613-115">Digital media content is added to the library by using the search feature of Windows Media Player.</span></span>
-   <span data-ttu-id="5c613-116">數位媒體內容會依 Windows Media Player 的資料夾監控功能新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="5c613-116">Digital media content is added to the library by the folder monitoring feature of Windows Media Player.</span></span>
-   <span data-ttu-id="5c613-117">當使用者拖放檔案時，數位媒體內容會新增至同步處理清單。</span><span class="sxs-lookup"><span data-stu-id="5c613-117">Digital media content is added to the sync list when the user drags and drops a file.</span></span>

<span data-ttu-id="5c613-118">在 Windows Media Player 建立轉換外掛程式的實例之後，外掛程式必須將提供的檔案轉換成 ASF 或 WMA，並新增相關的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5c613-118">After Windows Media Player creates an instance of a conversion plug-in, the plug-in must convert the supplied file to ASF or WMA and add relevant metadata.</span></span> <span data-ttu-id="5c613-119"> (不使用轉換外掛程式轉碼檔案。 ) 外掛程式必須將已轉換的檔案複製到指定的資料夾，並將新檔案的路徑傳回給 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="5c613-119">(Do not use the conversion plug-in to transcode the file.) The plug-in must then copy the converted file to the specified folder and return the path to the new file to Windows Media Player.</span></span>

<span data-ttu-id="5c613-120">轉換外掛程式必須執行 **IWMPConvert** 介面。</span><span class="sxs-lookup"><span data-stu-id="5c613-120">Conversion plug-ins must implement the **IWMPConvert** interface.</span></span> <span data-ttu-id="5c613-121">請參閱 [轉換外掛程式程式設計參考](conversion-plug-ins-programming-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="5c613-121">See [Conversion Plug-ins Programming Reference](conversion-plug-ins-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c613-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c613-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c613-123">**關於轉換流程**</span><span class="sxs-lookup"><span data-stu-id="5c613-123">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="5c613-124">**將中繼資料新增至轉換的檔案**</span><span class="sxs-lookup"><span data-stu-id="5c613-124">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="5c613-125">**Windows Media Player 轉換外掛程式**</span><span class="sxs-lookup"><span data-stu-id="5c613-125">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




