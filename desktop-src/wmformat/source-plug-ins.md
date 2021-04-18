---
title: 來源外掛程式
description: 來源外掛程式
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows Media Format SDK，來源外掛程式
- Advanced Systems Format (ASF) 、source 外掛程式
- ASF (Advanced Systems Format) 、source 外掛程式
- 來源外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965218"
---
# <a name="source-plug-ins"></a><span data-ttu-id="a58cf-107">來源外掛程式</span><span class="sxs-lookup"><span data-stu-id="a58cf-107">Source Plug-ins</span></span>

<span data-ttu-id="a58cf-108">來源外掛程式是一種可供開發人員使用的選項，可讓想要為 Windows Media®檔執行自己的儲存系統。</span><span class="sxs-lookup"><span data-stu-id="a58cf-108">A source plug-in is an option available to developers who wish to implement their own storage system for Windows Media® files.</span></span> <span data-ttu-id="a58cf-109">來源外掛程式可讓您透過執行稱為 **IStream** 的 COM 介面，這是提供資料的標準介面。</span><span class="sxs-lookup"><span data-stu-id="a58cf-109">A source plug-in enables this through the implementation of a COM interface called **IStream**, which is a standard interface for providing data.</span></span>

<span data-ttu-id="a58cf-110">來源外掛程式應以 dll 的形式寫入，而 SDK 會透過登錄專案對其提供已知的狀態。</span><span class="sxs-lookup"><span data-stu-id="a58cf-110">The source plug-in should be written as a dll, and its presence is made known to the SDK through a registry entry.</span></span> <span data-ttu-id="a58cf-111">您可以用這種方式來執行任何數量的來源外掛程式。</span><span class="sxs-lookup"><span data-stu-id="a58cf-111">There can be any number of source plug-ins implemented this way.</span></span> <span data-ttu-id="a58cf-112">來源外掛程式必須匯出 [**WMCreateStreamForURL**](wmcreatestreamforurl.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="a58cf-112">The source plug-in must export the [**WMCreateStreamForURL**](wmcreatestreamforurl.md) function.</span></span>

<span data-ttu-id="a58cf-113">若要註冊來源外掛程式，應新增下列登錄專案：</span><span class="sxs-lookup"><span data-stu-id="a58cf-113">To register a source plug-in, the following registry entry should be added:</span></span>

<span data-ttu-id="a58cf-114">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Media \\ WMSDK \\ 來源</span><span class="sxs-lookup"><span data-stu-id="a58cf-114">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Media\\WMSDK\\sources</span></span>

<span data-ttu-id="a58cf-115">Name = "任何唯一名稱"</span><span class="sxs-lookup"><span data-stu-id="a58cf-115">Name = "any unique name"</span></span>

<span data-ttu-id="a58cf-116">值 = 來源外掛程式 dll 的路徑名稱</span><span class="sxs-lookup"><span data-stu-id="a58cf-116">Value = pathname of the source plug-in dll</span></span>

<span data-ttu-id="a58cf-117">註冊 dll 之後，應用程式可以使用 **IWMReader：： Open** 方法 (搭配適當的 URL 做為參數) 來存取串流資料，而這些資料可以儲存在檔案或使用者定義的資料容器中。</span><span class="sxs-lookup"><span data-stu-id="a58cf-117">Once the dll has been registered, the application can use the **IWMReader::Open** method (with the appropriate URL as a parameter) to access stream data, which can be stored in files or user-defined data containers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a58cf-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a58cf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a58cf-119">**IWMReader：： Open**</span><span class="sxs-lookup"><span data-stu-id="a58cf-119">**IWMReader::Open**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[<span data-ttu-id="a58cf-120">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="a58cf-120">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="a58cf-121">**WMCreateStreamForURL**</span><span class="sxs-lookup"><span data-stu-id="a58cf-121">**WMCreateStreamForURL**</span></span>](wmcreatestreamforurl.md)
</dt> </dl>

 

 




