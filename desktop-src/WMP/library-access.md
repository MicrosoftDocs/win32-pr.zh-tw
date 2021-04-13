---
title: 程式庫存取
description: 程式庫存取
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player 程式庫，存取
- 程式庫，存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300816"
---
# <a name="library-access"></a><span data-ttu-id="5552f-112">程式庫存取</span><span class="sxs-lookup"><span data-stu-id="5552f-112">Library Access</span></span>

<span data-ttu-id="5552f-113">存取程式庫 Windows Media Player 物件模型的屬性和方法，需要資料庫的唯讀或讀取/寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="5552f-113">Properties and methods of the Windows Media Player object model that access the library require either read-only or read/write access to the database.</span></span> <span data-ttu-id="5552f-114">此程式庫包含某些使用者想要保持私密的資訊，而且應該只透過其同意來存取或更改。</span><span class="sxs-lookup"><span data-stu-id="5552f-114">The library contains information that some users want to keep private and that should be accessed or altered only with their consent.</span></span>

<span data-ttu-id="5552f-115">針對 Windows Media Player 9 系列或更新版本，您可以透過程式設計的方式決定存取層級。</span><span class="sxs-lookup"><span data-stu-id="5552f-115">For Windows Media Player 9 Series or later, you can programmatically determine access level.</span></span> <span data-ttu-id="5552f-116">若要判斷授與您程式碼的目前存取層級，請取出 *設定*。**mediaAccessRights** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5552f-116">To determine the current level of access granted to your code, retrieve the *Settings*.**mediaAccessRights** property.</span></span> <span data-ttu-id="5552f-117">該屬性會傳回「無」、「讀取」或「完整」 (讀取/寫入) 。</span><span class="sxs-lookup"><span data-stu-id="5552f-117">That property returns "none", "read", or "full" (read/write).</span></span> <span data-ttu-id="5552f-118">若要要求特定的存取權限，請呼叫 *設定*。**requestMediaAccessRights** 方法，傳遞指定您所要求層級的參數。</span><span class="sxs-lookup"><span data-stu-id="5552f-118">To request specific access rights, call the *Settings*.**requestMediaAccessRights** method, passing a parameter that specifies the level you are requesting.</span></span> <span data-ttu-id="5552f-119">方法會顯示訊息給使用者，說明所要求的存取層級，並傳回 **布林** 值，指出是否已授與存取權。</span><span class="sxs-lookup"><span data-stu-id="5552f-119">The method displays a message to the user explaining the requested level of access, and returns a **Boolean** value indicating whether the access was granted.</span></span>

<span data-ttu-id="5552f-120">系統會根據您的程式碼相對於使用者電腦的執行位置，自動授與特定存取權限。</span><span class="sxs-lookup"><span data-stu-id="5552f-120">Certain access rights are granted automatically depending on where your code is running relative to the user's computer.</span></span>

-   <span data-ttu-id="5552f-121">如果您的網頁或程式位於使用者的電腦上，則預設會授與完整存取權限。</span><span class="sxs-lookup"><span data-stu-id="5552f-121">If your webpage or program is located on the user's computer, full access rights are granted by default.</span></span>
-   <span data-ttu-id="5552f-122">Web pages 具有 *播放玩家* 的讀取權限。**currentMedia**、 *Player*。**currentPlaylist**，以及 *媒體*。當網頁位於與媒體專案或播放清單的安全性區域相同或更受限制的 Internet Explorer 安全性區域中時， **sourceURL** 。</span><span class="sxs-lookup"><span data-stu-id="5552f-122">Web pages have read access to *Player*.**currentMedia**, *Player*.**currentPlaylist**, and *Media*.**sourceURL** when the webpage is located in an Internet Explorer security zone that is the same as or less restricted than the security zone of the media item or playlist.</span></span>

    <span data-ttu-id="5552f-123">從最低限制到最受限制的範圍，安全性區域是 **受信任** 的區域 (包括使用者的本機電腦) 、近端 **內部** 網路區域、 **網際網路** 區域和 **受限** 的區域。</span><span class="sxs-lookup"><span data-stu-id="5552f-123">Ranging from least restricted to most restricted, the security zones are the **Trusted** zone (including the user's local computer), the **Local intranet** zone, the **Internet** zone, and the **Restricted** zone.</span></span>

    <span data-ttu-id="5552f-124">例如，近端 **內部** 網路區域中的網頁具有 *播放* 程式的完整存取權限。**currentMedia** 對應的媒體專案位於近端內部網路或網際網路時，但必須針對位於使用者本機電腦或 **受信任** 區域中網站上的媒體專案要求存取權。</span><span class="sxs-lookup"><span data-stu-id="5552f-124">For example, a webpage in the **Local intranet** zone has full access rights to *Player*.**currentMedia** when the corresponding media item is on the local intranet or the Internet, but access rights must be requested for media items located on a user's local computer or on a website in the **Trusted** zone.</span></span>

<span data-ttu-id="5552f-125">您應該在其可能遇到的所有安全性區域中測試您的 Web 型或 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5552f-125">You should test your Web-based or Windows-based application in all of the security zones it may encounter.</span></span> <span data-ttu-id="5552f-126">應用程式應設計為可適當地處理拒絕存取要求。</span><span class="sxs-lookup"><span data-stu-id="5552f-126">The application should be designed to handle denial of an access request correctly.</span></span>

<span data-ttu-id="5552f-127">Windows Media Player 9 系列之前 Windows Media Player 物件模型版本不包含 **mediaAccessRights** 或 **requestMediaAccessRights**。</span><span class="sxs-lookup"><span data-stu-id="5552f-127">Windows Media Player object model versions prior to Windows Media Player 9 Series do not include **mediaAccessRights** or **requestMediaAccessRights**.</span></span> <span data-ttu-id="5552f-128">這些舊版的 Windows Media Player 可讓使用者使用 [ **選項** ] 對話方塊來設定存取層級。</span><span class="sxs-lookup"><span data-stu-id="5552f-128">These earlier versions of Windows Media Player enable the user to set access levels using the **Options** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5552f-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="5552f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5552f-130">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="5552f-130">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="5552f-131">**使用程式庫**</span><span class="sxs-lookup"><span data-stu-id="5552f-131">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




