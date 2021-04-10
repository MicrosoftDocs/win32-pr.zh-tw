---
title: 建立讀取器並開啟檔案
description: 建立讀取器並開啟檔案
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Advanced Systems Format (ASF) ，建立讀取器
- ASF (Advanced Systems Format) ，建立讀取器
- Advanced Systems Format (ASF) ，開啟檔案
- ASF (Advanced Systems Format) ，開啟檔案
- 非同步讀取器，建立
- 非同步讀取器，開啟檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681555"
---
# <a name="to-create-a-reader-and-open-a-file"></a><span data-ttu-id="cd285-109">建立讀取器並開啟檔案</span><span class="sxs-lookup"><span data-stu-id="cd285-109">To Create a Reader and Open a File</span></span>

<span data-ttu-id="cd285-110">在您可以使用讀取器執行任何工作之前，您必須先建立讀取器物件，並載入檔案進行讀取。</span><span class="sxs-lookup"><span data-stu-id="cd285-110">Before you can do any work with the reader, you will need to create a reader object and load a file for reading.</span></span> <span data-ttu-id="cd285-111">若要初始化讀取器並開啟檔案，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="cd285-111">To initialize the reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="cd285-112">藉由呼叫 [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) 函數來建立讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="cd285-112">Create a reader object by calling the [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) function.</span></span> <span data-ttu-id="cd285-113">您必須為新的讀取器物件指定所需的版權管理層級。</span><span class="sxs-lookup"><span data-stu-id="cd285-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="cd285-114">可用的模式會列在 [**WMT \_ 許可權**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) 列舉型別中。</span><span class="sxs-lookup"><span data-stu-id="cd285-114">The available modes are listed in the [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) enumeration type.</span></span>
2.  <span data-ttu-id="cd285-115">藉由呼叫 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)，指定要讀取的檔案。</span><span class="sxs-lookup"><span data-stu-id="cd285-115">Specify a file to read by calling [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span></span> <span data-ttu-id="cd285-116">您必須指定讀取器回呼介面，讓讀取器使用。</span><span class="sxs-lookup"><span data-stu-id="cd285-116">You must specify a reader callback interface for the reader to use.</span></span> <span data-ttu-id="cd285-117">如需讀取器回呼的詳細資訊，請參閱 [在 OnStatus 回呼中執行讀取器訊息](to-implement-reader-messages-in-the-onstatus-callback.md)。</span><span class="sxs-lookup"><span data-stu-id="cd285-117">For more information about the reader callback, see [To Implement Reader Messages in the OnStatus Callback](to-implement-reader-messages-in-the-onstatus-callback.md).</span></span>
3.  <span data-ttu-id="cd285-118">等候讀取器開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="cd285-118">Wait for the reader to open the file.</span></span> <span data-ttu-id="cd285-119">當您呼叫 **Open** 來載入檔案時，它幾乎會立即傳回，並且在另一個執行緒上繼續處理。</span><span class="sxs-lookup"><span data-stu-id="cd285-119">When you call **Open** to load a file, it returns almost immediately and continues processing on another thread.</span></span> <span data-ttu-id="cd285-120">您應等候作業完成，方法是在 **OnStatus** 回呼收到 WMT 開啟的狀態訊息時，發出事件的信號 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cd285-120">You should wait for operations to complete, by signaling an event when the **OnStatus** callback receives the WMT\_OPENED status message.</span></span>

<span data-ttu-id="cd285-121">讀取器也支援使用 **IStream** COM 介面來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="cd285-121">The reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="cd285-122">您可以選擇任何方式來執行 **IStream** 介面。</span><span class="sxs-lookup"><span data-stu-id="cd285-122">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="cd285-123">在 **IStream** 中開啟所需的檔案之後，您可以依照上面所列的步驟，但您必須在步驟2中呼叫 [**IWMReaderAdvanced2：： OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) 而不是 **IWMReader：： Open** 。</span><span class="sxs-lookup"><span data-stu-id="cd285-123">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMReaderAdvanced2::OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) instead of **IWMReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd285-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd285-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd285-125">**IWMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="cd285-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="cd285-126">**IWMReaderAdvanced2 介面**</span><span class="sxs-lookup"><span data-stu-id="cd285-126">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="cd285-127">**IWMStatusCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="cd285-127">**IWMStatusCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[<span data-ttu-id="cd285-128">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="cd285-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="cd285-129">**使用回呼方法**</span><span class="sxs-lookup"><span data-stu-id="cd285-129">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




