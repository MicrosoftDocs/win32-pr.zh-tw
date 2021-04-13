---
title: 加入 ContentDistributor 屬性
description: 加入 ContentDistributor 屬性
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player 線上商店，加入 ContentDistributor 屬性
- 線上商店，加入 ContentDistributor 屬性
- 輸入1個線上商店，加入 ContentDistributor 屬性
- 輸入2個線上商店，加入 ContentDistributor 屬性
- Windows Media Player 線上商店，ContentDistributor 屬性
- 線上商店、ContentDistributor 屬性
- 輸入1個線上商店，ContentDistributor 屬性
- 類型2線上商店，ContentDistributor 屬性
- 加入 ContentDistributor 屬性
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300928"
---
# <a name="adding-the-contentdistributor-attribute"></a><span data-ttu-id="35e6b-113">加入 ContentDistributor 屬性</span><span class="sxs-lookup"><span data-stu-id="35e6b-113">Adding the ContentDistributor Attribute</span></span>

<span data-ttu-id="35e6b-114">當使用者嘗試播放線上商店內容或將內容複寫到 CD 或裝置時，Windows Media Player 會呼叫 COM 物件中的特定方法。</span><span class="sxs-lookup"><span data-stu-id="35e6b-114">When the user attempts to play online store content or to copy the content to a CD or device, Windows Media Player calls certain methods in your COM object.</span></span> <span data-ttu-id="35e6b-115">若要這樣做，播放程式需要一種方式來區別您的內容與其他線上商店提供者的內容。</span><span class="sxs-lookup"><span data-stu-id="35e6b-115">To do this, the Player needs a way to differentiate your content from that of other online store providers.</span></span> <span data-ttu-id="35e6b-116">藉由將您的線上商店金鑰名稱新增為 **ContentDistributor** (的值，這是 Windows MEDIA Format SDK 屬性的別名（名為 **WM/ContentDistributor**) Attribute）至 windows media 內容，您可以確定播放程式可以識別與您的服務相關聯的內容。</span><span class="sxs-lookup"><span data-stu-id="35e6b-116">By adding your online store key name as the value for the **ContentDistributor** (which is an alias for the Windows Media Format SDK attribute named **WM/ContentDistributor**) attribute to your Windows Media-based content, you ensure that the Player can identify the content associated with your service.</span></span>

<span data-ttu-id="35e6b-117">為 **ContentDistributor** 新增值也可確保 Windows Media Player 將會在程式庫中為您提供的內容建立節點。</span><span class="sxs-lookup"><span data-stu-id="35e6b-117">Adding a value for **ContentDistributor** also ensures that Windows Media Player will create a node in the library for content you provide.</span></span> <span data-ttu-id="35e6b-118">請參閱連結 [庫整合](library-integration.md)。</span><span class="sxs-lookup"><span data-stu-id="35e6b-118">See [Library Integration](library-integration.md).</span></span>

<span data-ttu-id="35e6b-119">您可以透過兩種方式來指定此值：</span><span class="sxs-lookup"><span data-stu-id="35e6b-119">You can specify this value two ways:</span></span>

-   <span data-ttu-id="35e6b-120">使用 Windows Media Player 物件模型。</span><span class="sxs-lookup"><span data-stu-id="35e6b-120">Use the Windows Media Player object model.</span></span> <span data-ttu-id="35e6b-121">當您這樣做時，Windows Media Player 會將您指定的值加入至程式庫資料庫。</span><span class="sxs-lookup"><span data-stu-id="35e6b-121">When you do this, Windows Media Player adds the value you specify to the library database.</span></span> <span data-ttu-id="35e6b-122">最後，播放玩家也會將屬性值寫入數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="35e6b-122">Eventually, the Player will also write the attribute value to the digital media file.</span></span>
-   <span data-ttu-id="35e6b-123">使用 Windows Media Format SDK 以程式設計方式新增 **WM/ContentDistributor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="35e6b-123">Use the Windows Media Format SDK to programmatically add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="35e6b-124">當您這樣做時，Windows Media Player 會在將數位媒體檔案新增至程式庫時，讀取屬性值並將它新增至資料庫。</span><span class="sxs-lookup"><span data-stu-id="35e6b-124">When you do this, Windows Media Player reads the attribute value and adds it to the database when the digital media file is added to the library.</span></span>

<span data-ttu-id="35e6b-125">建立您的線上商店 COM 物件時，您為 **ContentDistributor** 設定的檔案屬性值以及指派給 yourproject。中常數 kszContentDistributorID 的值必須完全相符。</span><span class="sxs-lookup"><span data-stu-id="35e6b-125">When creating your online store COM object, the file attribute value you set for **ContentDistributor** and the value assigned to the constant kszContentDistributorID in YourProject.h must match exactly.</span></span> <span data-ttu-id="35e6b-126">回想一下，當您使用專案嚮導建立專案時，您已為 COM 物件指定此常數值。</span><span class="sxs-lookup"><span data-stu-id="35e6b-126">Recall that you specified this constant value for your COM object when you created the project by using the project wizard.</span></span> <span data-ttu-id="35e6b-127">您可以手動變更此值。</span><span class="sxs-lookup"><span data-stu-id="35e6b-127">You can change this value manually.</span></span> <span data-ttu-id="35e6b-128">請務必使用可唯一識別服務的字串。</span><span class="sxs-lookup"><span data-stu-id="35e6b-128">Just be sure to use a string that uniquely identifies your service.</span></span>

## <a name="using-the-windows-media-player-object-model"></a><span data-ttu-id="35e6b-129">使用 Windows Media Player 物件模型</span><span class="sxs-lookup"><span data-stu-id="35e6b-129">Using the Windows Media Player Object Model</span></span>

<span data-ttu-id="35e6b-130">若要使用 Windows Media Player 物件模型指定 **ContentDistributor** 的值，請使用 [setItemInfo](media-setiteminfo.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="35e6b-130">To specify a value for **ContentDistributor** using the Windows Media Player object model, use the [Media.setItemInfo](media-setiteminfo.md) method.</span></span> <span data-ttu-id="35e6b-131">下列程式碼範例會針對目前播放的媒體專案，指定 **ContentDistributor** 的 "Proseware" 值：</span><span class="sxs-lookup"><span data-stu-id="35e6b-131">The following example code specifies the value "Proseware" for **ContentDistributor** for the currently playing media item:</span></span>


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a><span data-ttu-id="35e6b-132">使用 Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="35e6b-132">Using the Windows Media Format SDK</span></span>

<span data-ttu-id="35e6b-133">Windows Media Player SDK 包含名為 SetContentDistributor 的範例 c + + 檔案，其示範如何使用 Windows Media Format 9 系列 SDK 來新增 **WM/ContentDistributor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="35e6b-133">The Windows Media Player SDK includes a sample C++ file, named SetContentDistributor.cpp, which demonstrates how to use the Windows Media Format 9 Series SDK to add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="35e6b-134">您可以在安裝 SDK 的名稱為 Metadata 的資料夾中找到這個範例檔案。</span><span class="sxs-lookup"><span data-stu-id="35e6b-134">You can locate this sample file in the folder named Metadata where you installed the SDK.</span></span> <span data-ttu-id="35e6b-135">若要使用此程式碼，您必須遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="35e6b-135">To use this code you must follow these steps:</span></span>

1.  <span data-ttu-id="35e6b-136">安裝 Windows Media Format 9 系列 SDK 並設定執行時間，如檔中所述。</span><span class="sxs-lookup"><span data-stu-id="35e6b-136">Install the Windows Media Format 9 Series SDK and configure the runtime as described in the documentation.</span></span>
2.  <span data-ttu-id="35e6b-137">在 Visual Studio 中建立新的空白 c + + 專案，並將名為 SetContentDistributor 的範例檔案新增至專案。</span><span class="sxs-lookup"><span data-stu-id="35e6b-137">Create a new empty C++ project in Visual Studio and add the sample file named SetContentDistributor.cpp to the project.</span></span>
3.  <span data-ttu-id="35e6b-138">將 Windows Media Format 9 系列 SDK Lib 資料夾的路徑新增至您的檔案路徑清單。</span><span class="sxs-lookup"><span data-stu-id="35e6b-138">Add the path to the Windows Media Format 9 Series SDK Lib folders to your list of file paths.</span></span> <span data-ttu-id="35e6b-139">從 [工具]  功能表選擇 [選項] 。</span><span class="sxs-lookup"><span data-stu-id="35e6b-139">From the **Tools** menu, choose **Options**.</span></span>
4.  <span data-ttu-id="35e6b-140">在 [ **選項** ] 對話方塊中，按一下 [ **專案**]，然後按一下 [ **VC + + 目錄**]。</span><span class="sxs-lookup"><span data-stu-id="35e6b-140">In the **Options** dialog box, click **Projects**, and then click **VC++ Directories**.</span></span>
5.  <span data-ttu-id="35e6b-141">在 [ **顯示目錄** ] 下拉式清單方塊中，按一下 [連結 **庫** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="35e6b-141">In the **Show Directories for** drop-down list box, click **Library files**.</span></span>
6.  <span data-ttu-id="35e6b-142">使用按鈕將路徑新增至清單方塊。</span><span class="sxs-lookup"><span data-stu-id="35e6b-142">Use the buttons to add the paths to the list boxes.</span></span>
7.  <span data-ttu-id="35e6b-143">開啟專案的 [屬性頁] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="35e6b-143">Open the property pages dialog box for your project.</span></span> <span data-ttu-id="35e6b-144">選擇 [設定 **屬性**]、[ **連結器**]，然後 **輸入**。</span><span class="sxs-lookup"><span data-stu-id="35e6b-144">Choose **Configuration Properties**, then **Linker**, and then **Input**.</span></span> <span data-ttu-id="35e6b-145">在 [ **其他** 相依性] 文字方塊中輸入 "wmvcore"。</span><span class="sxs-lookup"><span data-stu-id="35e6b-145">Type "wmvcore.lib" in the **Additional Dependencies** text box.</span></span>

<span data-ttu-id="35e6b-146">範例程式碼會建立命令列程式。</span><span class="sxs-lookup"><span data-stu-id="35e6b-146">The sample code creates a command-line program.</span></span> <span data-ttu-id="35e6b-147">您在執行程式時提供的引數會指定要修改之數位媒體檔案的路徑，以及 **ContentDistributor** 屬性值的字串。</span><span class="sxs-lookup"><span data-stu-id="35e6b-147">The arguments you provide when running the program specify the path to the digital media file to modify and a string for the **ContentDistributor** attribute value.</span></span> <span data-ttu-id="35e6b-148">程式碼會使用 **IWMHeaderInfo：： SetAttribute** ，將屬性新增至您指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="35e6b-148">The code uses **IWMHeaderInfo::SetAttribute** to add the attribute to the file you specified.</span></span> <span data-ttu-id="35e6b-149">您可以使用此範例，或使用它作為您自己的程式的起點。</span><span class="sxs-lookup"><span data-stu-id="35e6b-149">You can use this sample as is or use it as a starting point for your own program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35e6b-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="35e6b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35e6b-151">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="35e6b-151">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




