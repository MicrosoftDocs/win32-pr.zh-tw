---
title: 將腳本資料新增至標頭
description: 將腳本資料新增至標頭
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media Format SDK，將腳本資料新增至標頭
- Advanced Systems Format (ASF) ，將腳本資料新增至標頭
- ASF (Advanced Systems Format) ，將腳本資料新增至標頭
- 腳本，將資料加入至標頭
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106969893"
---
# <a name="to-add-script-data-to-the-header"></a><span data-ttu-id="88fe1-107">將腳本資料新增至標頭</span><span class="sxs-lookup"><span data-stu-id="88fe1-107">To Add Script Data to the Header</span></span>

<span data-ttu-id="88fe1-108">您可以在 ASF 檔案的標頭中包含指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="88fe1-108">You can include script commands in the header of an ASF file.</span></span> <span data-ttu-id="88fe1-109">若要在編碼時將指令碼命令寫入標頭，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="88fe1-109">To write script commands to the header at the time of encoding, perform the following steps.</span></span> <span data-ttu-id="88fe1-110">在呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)之前，請先執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="88fe1-110">Perform these steps prior to calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

1.  <span data-ttu-id="88fe1-111">藉由呼叫 **IWMWriter：： QueryInterface** 來取得 **IWMHeaderInfo** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="88fe1-111">Obtain a pointer to the **IWMHeaderInfo** interface by calling **IWMWriter::QueryInterface**.</span></span>
2.  <span data-ttu-id="88fe1-112">藉由呼叫 [**IWMHeaderInfo：： AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript)來新增每個所需的指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="88fe1-112">Add each desired script command by calling [**IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span></span> <span data-ttu-id="88fe1-113">每個呼叫會分別採用兩個字串，並將呈現時間用於命令作為參數。</span><span class="sxs-lookup"><span data-stu-id="88fe1-113">Each call takes the two strings separately and the presentation time to be used for the command as parameters.</span></span>

<span data-ttu-id="88fe1-114">當應用程式讀取檔案時，它將需要取出所有的指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="88fe1-114">When an application reads the file, it will need to retrieve all of the script commands.</span></span> <span data-ttu-id="88fe1-115">若要在檔案的標頭中尋找所有指令碼命令，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="88fe1-115">To find all script commands in the header of a file, perform the following steps.</span></span> <span data-ttu-id="88fe1-116">這應該會在開始播放之前完成。</span><span class="sxs-lookup"><span data-stu-id="88fe1-116">This should be done before starting playback.</span></span>

1.  <span data-ttu-id="88fe1-117">藉由呼叫物件中另一個介面的 **QueryInterface** 方法，取得讀取器物件 (或同步讀取器物件) 的 **IWMHeaderInfo** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="88fe1-117">Obtain a pointer to the **IWMHeaderInfo** interface of the reader object (or synchronous reader object) by calling the **QueryInterface** method of another interface in the object.</span></span>
2.  <span data-ttu-id="88fe1-118">藉由呼叫 [**IWMHeaderInfo：： GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount)，取得標頭中的腳本總數。</span><span class="sxs-lookup"><span data-stu-id="88fe1-118">Get the total number of scripts in the header by calling [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span></span>
3.  <span data-ttu-id="88fe1-119">使用 [**IWMHeaderInfo：： >getscript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript)的呼叫，以迴圈方式逐一查看標頭中的所有腳本。</span><span class="sxs-lookup"><span data-stu-id="88fe1-119">Loop through all of the scripts in the header one at a time using calls to [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span></span>
4.  <span data-ttu-id="88fe1-120">建立展示時間清單，讓您的應用程式可以在適當的時間回應命令。</span><span class="sxs-lookup"><span data-stu-id="88fe1-120">Create a list of the presentation times so that your application can react to the commands at the appropriate time.</span></span>

> [!Note]  
> <span data-ttu-id="88fe1-121">使用 DRM 加密檔案時，沒有指令碼命令可以有0的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="88fe1-121">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="88fe1-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="88fe1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88fe1-123">**IWMHeaderInfo 介面**</span><span class="sxs-lookup"><span data-stu-id="88fe1-123">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="88fe1-124">**IWMWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="88fe1-124">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="88fe1-125">**使用指令碼命令**</span><span class="sxs-lookup"><span data-stu-id="88fe1-125">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




