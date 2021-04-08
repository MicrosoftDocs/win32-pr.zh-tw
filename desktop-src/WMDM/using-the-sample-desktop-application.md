---
title: 使用範例桌面應用程式
description: 使用範例桌面應用程式
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Media 裝置管理員，範例
- 裝置管理員，範例
- 桌面應用程式、範例
- Windows Media 裝置管理員，桌面應用程式範例
- 裝置管理員，桌面應用程式範例
- 範例，桌面應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672031"
---
# <a name="using-the-sample-desktop-application"></a><span data-ttu-id="328f3-109">使用範例桌面應用程式</span><span class="sxs-lookup"><span data-stu-id="328f3-109">Using the Sample Desktop Application</span></span>

<span data-ttu-id="328f3-110">桌面應用程式範例是一個基本的雙窗格視窗，類似 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="328f3-110">The sample desktop application is a basic two-paned window somewhat like Windows Explorer.</span></span> <span data-ttu-id="328f3-111">它可讓您流覽裝置的內容，使用左窗格中資料夾的樹狀檢視顯示，以及右窗格中的檔案。</span><span class="sxs-lookup"><span data-stu-id="328f3-111">It allows you to browse the contents of a device, using a tree view display of folders in the left pane, and files in the right pane.</span></span> <span data-ttu-id="328f3-112">每個資料夾樹狀結構的根目錄都會以邏輯方式被視為不同的裝置，不過某些裝置可能會將自己表示為多個物件 (每個根儲存體) 各有一個物件。</span><span class="sxs-lookup"><span data-stu-id="328f3-112">The root of each folder tree is logically considered a different device, although some devices might represent themselves as several objects (one for each root storage).</span></span> <span data-ttu-id="328f3-113">若要讀取資料夾或檔案的基本屬性，請以滑鼠右鍵按一下物件，然後選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="328f3-113">To read the basic properties of either a folder or a file, right-click the object and select **Properties**.</span></span>

<span data-ttu-id="328f3-114">您可以在右窗格中選取檔案，然後在 [檔案 **] 功能表上選取 [** **刪除**]，以刪除裝置上的檔案。</span><span class="sxs-lookup"><span data-stu-id="328f3-114">You can delete files on the device by selecting a file in the right pane and selecting **Delete** on the **File** menu.</span></span> <span data-ttu-id="328f3-115">若要將媒體檔案新增至裝置，您可以將檔案從桌面拖曳至程式的右窗格。</span><span class="sxs-lookup"><span data-stu-id="328f3-115">To add media files to the device, you can drag files from the desktop onto the right pane of the program.</span></span> <span data-ttu-id="328f3-116">請注意，檔案必須是裝置支援的媒體格式;無法接受的格式檔案 (非媒體檔案，例如 .txt 檔案，或裝置) 不支援的媒體格式，將不會傳送到裝置。</span><span class="sxs-lookup"><span data-stu-id="328f3-116">Note that files must be of a media format supported by the device; files of unacceptable formats (non-media files such as .txt files, or media formats not supported by the device) will not be sent to the device.</span></span> <span data-ttu-id="328f3-117"> (請注意，這項限制是程式的;Windows Media 裝置管理員可讓您將任何檔案傳送至裝置（如果裝置會接受）。 ) </span><span class="sxs-lookup"><span data-stu-id="328f3-117">(Note that this restriction is the program's; Windows Media Device Manager enables you to send any file to a device if the device will accept it.)</span></span>

<span data-ttu-id="328f3-118">若要捕捉傳送至 [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) 介面的回呼事件，您必須核取 [ **選項** ] 功能表中的 [使用操作介面] 選項。</span><span class="sxs-lookup"><span data-stu-id="328f3-118">To capture callback events sent to the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) interface, you must check the "Use Operation Interface" option in the **Options** menu.</span></span>

<span data-ttu-id="328f3-119">[ **選項** ] 功能表也可讓您選擇是否要使用更多的 advanced 介面，以及 advanced 裝置所支援的功能。</span><span class="sxs-lookup"><span data-stu-id="328f3-119">The **Options** menu also enables you to choose whether to use several more advanced interfaces with features supported by advanced devices.</span></span>

<span data-ttu-id="328f3-120">[ **容器** ] 功能表具有可讓您建立播放清單或專輯的選項。</span><span class="sxs-lookup"><span data-stu-id="328f3-120">The **Containers** menu has options to allow you to create a playlist or an album.</span></span> <span data-ttu-id="328f3-121">若要建立播放清單，請選取裝置上的一或多個歌曲，然後按一下 [**容器**] 功能表上的 [**建立播放清單**]。</span><span class="sxs-lookup"><span data-stu-id="328f3-121">To create a playlist, select one or more songs on the device and click **Create Playlist** on the **Containers** menu.</span></span> <span data-ttu-id="328f3-122">這項功能僅適用于 MTP 裝置，因為程式碼僅支援建立「虛擬」播放清單檔案。</span><span class="sxs-lookup"><span data-stu-id="328f3-122">This feature only works on MTP devices, because the code only supports the creation of an "virtual" playlist file.</span></span> <span data-ttu-id="328f3-123"> (虛擬播放清單是僅由中繼資料值指定的播放清單，而不是以實體檔案指定，例如 .WPL 檔。 ) 裝置必須支援空白播放清單才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="328f3-123">(A virtual playlist is a playlist that is specified only by metadata values, rather than by a physical file, for example a WPL file.) The device must support empty playlists to use this feature.</span></span>

<span data-ttu-id="328f3-124">若要建立專輯 (具有相關聯影像) 的播放清單，請選取裝置上的一或多個歌曲，然後按一下 [**容器**] 功能表上的 [**建立專輯**]。</span><span class="sxs-lookup"><span data-stu-id="328f3-124">To create an album (a playlist with an associated image), select one or more songs on the device and click **Create Album** on the **Containers** menu.</span></span> <span data-ttu-id="328f3-125">對話方塊可讓您流覽至電腦上的圖片檔案，以與專輯建立關聯。</span><span class="sxs-lookup"><span data-stu-id="328f3-125">A dialog box allows you to browse to a picture file on your computer to associate with the album.</span></span> <span data-ttu-id="328f3-126">類似于建立播放清單的方式，應用程式會建立「空白」的專輯檔案;如果裝置不支援空的專輯，這項功能將無法運作。</span><span class="sxs-lookup"><span data-stu-id="328f3-126">Similarly to the way it creates playlists, the application creates an "empty" album file; if the device does not support empty albums, this feature will not work.</span></span>

## <a name="related-topics"></a><span data-ttu-id="328f3-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="328f3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="328f3-128">**桌面應用程式範例**</span><span class="sxs-lookup"><span data-stu-id="328f3-128">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




