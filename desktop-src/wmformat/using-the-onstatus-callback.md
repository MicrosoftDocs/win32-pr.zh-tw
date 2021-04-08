---
title: 使用 OnStatus 回呼
description: 使用 OnStatus 回呼
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media Format SDK，OnStatus 回呼方法
- Windows Media Format SDK，IWMStatusCallback 介面
- OnStatus 回呼方法，關於
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932910"
---
# <a name="using-the-onstatus-callback"></a><span data-ttu-id="32de0-107">使用 OnStatus 回呼</span><span class="sxs-lookup"><span data-stu-id="32de0-107">Using the OnStatus Callback</span></span>

<span data-ttu-id="32de0-108">Windows Media 格式 SDK 中的數個物件會呼叫 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法。</span><span class="sxs-lookup"><span data-stu-id="32de0-108">The [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method is called by several objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="32de0-109">**OnStatus** 會接收表示 SDK 作業狀態變更的訊息。</span><span class="sxs-lookup"><span data-stu-id="32de0-109">**OnStatus** receives messages that represent changes in the status of SDK operations.</span></span>

<span data-ttu-id="32de0-110">若要使用 **OnStatus** 回呼方法，您必須在應用程式中執行繼承自 [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="32de0-110">To use the **OnStatus** callback method, you must implement a class in your application that inherits from the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface.</span></span> <span data-ttu-id="32de0-111">在類別中包含 **OnStatus** 版本的程式碼。</span><span class="sxs-lookup"><span data-stu-id="32de0-111">Include code for your version of **OnStatus** in the class.</span></span> <span data-ttu-id="32de0-112">您可以在此 SDK 隨附的範例中找到數個 **OnStatus** 的範例。</span><span class="sxs-lookup"><span data-stu-id="32de0-112">Several examples of **OnStatus** implementations can be found in the samples included with this SDK.</span></span> <span data-ttu-id="32de0-113">如需範例的詳細資訊，請參閱 [範例應用程式](sample-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="32de0-113">For more information about the samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="32de0-114">您必須將狀態回呼的執行與 Windows Media Format SDK 的各種物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="32de0-114">You must associate your implementation of the status callback with various objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="32de0-115">每個物件都有不同的方式來建立此關聯。</span><span class="sxs-lookup"><span data-stu-id="32de0-115">Each object has a different way of making this association.</span></span> <span data-ttu-id="32de0-116">如需關聯特定物件的方法清單，請參閱 **IWMStatusCallback** 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="32de0-116">For a list of the methods that associate specific objects, see the **IWMStatusCallback** reference page.</span></span>

<span data-ttu-id="32de0-117">**OnStatus** 可接收的狀態訊息是在 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)列舉類型中定義。</span><span class="sxs-lookup"><span data-stu-id="32de0-117">The status messages that can be received by **OnStatus** are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

<span data-ttu-id="32de0-118">您可以選擇要設陷的訊息，以及要忽略的訊息。</span><span class="sxs-lookup"><span data-stu-id="32de0-118">You can choose which messages to trap and which to ignore.</span></span> <span data-ttu-id="32de0-119">不過，某些功能需要回應某些狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="32de0-119">However, responding to some status messages is required for certain features.</span></span> <span data-ttu-id="32de0-120">例如，使用非同步讀取器時， [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 方法會以非同步方式開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="32de0-120">For example, when using the asynchronous reader, the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method opens a file asynchronously.</span></span> <span data-ttu-id="32de0-121">要知道檔案何時開啟的唯一方法，就是將 MWT-DS 開啟的訊息設為陷阱 \_ 。</span><span class="sxs-lookup"><span data-stu-id="32de0-121">The only way to tell when the file has been opened is to trap the MWT\_OPENED message.</span></span> <span data-ttu-id="32de0-122">一般來說，您回應的訊息是非同步工作完成的通知。</span><span class="sxs-lookup"><span data-stu-id="32de0-122">Typically, the messages you respond to are notifications of the completion of asynchronous tasks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32de0-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="32de0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32de0-124">**使用回呼方法**</span><span class="sxs-lookup"><span data-stu-id="32de0-124">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




