---
title: 非同步複合檔案
description: 非同步複合檔案是系統提供的非同步儲存體執行，可讓您在一般情況下有效率地從網際網路下載複合檔案。
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04de2162b50283b12bc8deed6ec908d92e7584d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376269"
---
# <a name="asynchronous-compound-files"></a><span data-ttu-id="2486a-103">非同步複合檔案</span><span class="sxs-lookup"><span data-stu-id="2486a-103">Asynchronous Compound Files</span></span>

<span data-ttu-id="2486a-104">非同步複合檔案是系統提供的非同步儲存體執行，可讓您在一般情況下有效率地從網際網路下載複合檔案。</span><span class="sxs-lookup"><span data-stu-id="2486a-104">Asynchronous Compound Files, the system-provided implementation of asynchronous storage, enables the efficient downloading of compound files from the Internet in general and the Web in particular.</span></span> <span data-ttu-id="2486a-105">非同步複合檔案的基本架構如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="2486a-105">The basic architecture of Asynchronous Compound Files is shown in the following diagram.</span></span>

![非同步複合檔案基本架構](images/asy-stor.png)

<span data-ttu-id="2486a-107">非同步複合檔案執行可以使用新的非同步標記型別，以瞭解網際網路通訊協定，並且可以系結至 URL 所識別的物件。</span><span class="sxs-lookup"><span data-stu-id="2486a-107">The Asynchronous Compound Files implementation can work with new asynchronous moniker types that understand Internet protocols and can bind to an object identified by a URL.</span></span> <span data-ttu-id="2486a-108">這類的標記會從用戶端對 [**IMoniker：： BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)的呼叫傳回非同步 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)或 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)指標。</span><span class="sxs-lookup"><span data-stu-id="2486a-108">Such a moniker would return an asynchronous [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) or [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer from the client's call to [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage).</span></span>

<span data-ttu-id="2486a-109">一般的複合檔案會在位元組陣列物件之上執行，這是以一般位元組陣列表示物件資料的檔案抽象概念。</span><span class="sxs-lookup"><span data-stu-id="2486a-109">Compound Files in general are implemented on top of a byte array object, an abstraction of a file that represents an object's data as a flat byte array.</span></span> <span data-ttu-id="2486a-110">位元組陣列物件會透過 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) 介面公開其功能。</span><span class="sxs-lookup"><span data-stu-id="2486a-110">The byte array object exposes its functionality through the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) interface.</span></span> <span data-ttu-id="2486a-111">如果位元組陣列支援非封鎖式非同步存放裝置，它會將暫止的檔案 \_ 傳回給複合檔案的執行，然後再將錯誤傳播回呼叫端。</span><span class="sxs-lookup"><span data-stu-id="2486a-111">If a byte array supports nonblocking asynchronous storage, it returns E\_PENDING to the compound-file implementation, which in turn propagates the error back to the caller.</span></span>

<span data-ttu-id="2486a-112">若要追蹤在下載期間可用的資料，支援非同步儲存的位元組陣列會在系統提供的包裝函式物件上公開 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 介面，這是專為此用途而設計的。</span><span class="sxs-lookup"><span data-stu-id="2486a-112">To keep track of the data available during a download, a byte array that supports asynchronous storage exposes the [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) interface on a wrapper object provided by the system specifically for this purpose.</span></span> <span data-ttu-id="2486a-113">非同步標記所提供的下載程式代碼會呼叫這個介面，以非同步方式填滿位元組陣列，因為資料可供使用。</span><span class="sxs-lookup"><span data-stu-id="2486a-113">The downloading code provided by an asynchronous moniker calls this interface to fill the byte array asynchronously, as data is available.</span></span> <span data-ttu-id="2486a-114">包裝函式物件也會公開 **ILockBytes** 介面，而非同步複合檔案的執行會使用此介面來讀取和寫入陣列中的資料。</span><span class="sxs-lookup"><span data-stu-id="2486a-114">The wrapper object also exposes an **ILockBytes** interface, which the Asynchronous Compound Files implementation uses to read and write data from and to the array.</span></span>

<span data-ttu-id="2486a-115">非同步儲存和資料流程物件提供 [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) 介面的連接點，該介面是由非同步標記下載程式代碼所執行。</span><span class="sxs-lookup"><span data-stu-id="2486a-115">Asynchronous storage and stream objects provide a connection point for the [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) interface, which is implemented by the asynchronous moniker's downloading code.</span></span> <span data-ttu-id="2486a-116">非同步複合檔案執行會呼叫 **IProgressNotify** ，以提供下載作業狀態相關資訊給下載程式。</span><span class="sxs-lookup"><span data-stu-id="2486a-116">The Asynchronous Compound Files implementation calls **IProgressNotify** to provide the downloader with information about the status of the downloading operation.</span></span>

 

 