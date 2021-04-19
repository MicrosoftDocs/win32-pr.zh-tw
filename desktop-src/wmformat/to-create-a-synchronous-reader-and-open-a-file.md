---
title: 建立同步讀取器並開啟檔案
description: 建立同步讀取器並開啟檔案
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Advanced Systems Format (ASF) ，建立讀取器
- ASF (Advanced Systems Format) ，建立讀取器
- Advanced Systems Format (ASF) ，開啟檔案
- ASF (Advanced Systems Format) ，開啟檔案
- 同步讀取器，建立
- 同步讀取器，開啟檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106969696"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a><span data-ttu-id="98e12-109">建立同步讀取器並開啟檔案</span><span class="sxs-lookup"><span data-stu-id="98e12-109">To Create a Synchronous Reader and Open a File</span></span>

<span data-ttu-id="98e12-110">在您可以使用同步讀取器執行任何工作之前，您必須先建立同步讀取器物件，並載入要讀取的檔案。</span><span class="sxs-lookup"><span data-stu-id="98e12-110">Before you can do any work with the synchronous reader, you will need to create a synchronous reader object and load a file for reading.</span></span> <span data-ttu-id="98e12-111">若要初始化同步讀取器並開啟檔案，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="98e12-111">To initialize the synchronous reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="98e12-112">藉由呼叫 [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) 函數來建立同步讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="98e12-112">Create a synchronous reader object by calling the [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) function.</span></span> <span data-ttu-id="98e12-113">您必須為新的讀取器物件指定所需的版權管理層級。</span><span class="sxs-lookup"><span data-stu-id="98e12-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="98e12-114">可用的模式會列在 **WMT \_ 許可權** 列舉型別中。</span><span class="sxs-lookup"><span data-stu-id="98e12-114">The available modes are listed in the **WMT\_RIGHTS** enumeration type.</span></span>
2.  <span data-ttu-id="98e12-115">藉由呼叫 [**IWMSyncReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open)，指定要讀取的檔案。</span><span class="sxs-lookup"><span data-stu-id="98e12-115">Specify a file to read by calling [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span></span>

<span data-ttu-id="98e12-116">同步讀取器也支援使用 **IStream** COM 介面來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="98e12-116">The synchronous reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="98e12-117">您可以選擇任何方式來執行 **IStream** 介面。</span><span class="sxs-lookup"><span data-stu-id="98e12-117">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="98e12-118">在 **IStream** 中開啟所需的檔案之後，您可以依照上面所列的步驟，但您必須在步驟2中呼叫 [**IWMSyncReader：： OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) 而不是 **IWMSyncReader：： Open** 。</span><span class="sxs-lookup"><span data-stu-id="98e12-118">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) instead of **IWMSyncReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98e12-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="98e12-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98e12-120">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="98e12-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="98e12-121">**使用同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="98e12-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




