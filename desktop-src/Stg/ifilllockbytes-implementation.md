---
title: IFillLockBytes-實
description: 系統會提供 IFillLockBytes 的實作為複合檔案執行的一部分。
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd Stg.，執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932183"
---
# <a name="ifilllockbytes---implementation"></a><span data-ttu-id="4fe90-104">IFillLockBytes-實</span><span class="sxs-lookup"><span data-stu-id="4fe90-104">IFillLockBytes - Implementation</span></span>

<span data-ttu-id="4fe90-105">系統會提供 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 的實作為複合檔案執行的一部分。</span><span class="sxs-lookup"><span data-stu-id="4fe90-105">The system provides an [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation as part of the Compound Files implementation.</span></span>

<span data-ttu-id="4fe90-106">下載程式代碼可以藉由呼叫 [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)來建立異步複合檔案物件的實例。</span><span class="sxs-lookup"><span data-stu-id="4fe90-106">Downloading code can create an instance of an asynchronous Compound File object by calling [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span></span> <span data-ttu-id="4fe90-107">下載程式代碼也可以藉由呼叫 [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) 函數或 [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) 函數，在現有的檔案或位元組陣列上建立異步位元組陣列包裝函式物件的實例。</span><span class="sxs-lookup"><span data-stu-id="4fe90-107">Downloading code can also create an instance of an asynchronous byte array wrapper object on an existing file or byte array by calling either the [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) function or the [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) function.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4fe90-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="4fe90-108">When to Use</span></span>

<span data-ttu-id="4fe90-109">目前，URL 名字標記是 COM 非同步存放裝置執行的唯一使用者。</span><span class="sxs-lookup"><span data-stu-id="4fe90-109">Currently, URL monikers are the only users of the COM asynchronous storage implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fe90-110">備註</span><span class="sxs-lookup"><span data-stu-id="4fe90-110">Remarks</span></span>

<span data-ttu-id="4fe90-111">以下是 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 執行的四個方法。</span><span class="sxs-lookup"><span data-stu-id="4fe90-111">The following are the four methods of the [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation.</span></span>

<dl> <dt>

<span data-ttu-id="4fe90-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span><span class="sxs-lookup"><span data-stu-id="4fe90-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span></span>
</dt> <dd>

<span data-ttu-id="4fe90-113">將新的位元組區塊寫入位元組陣列的結尾。</span><span class="sxs-lookup"><span data-stu-id="4fe90-113">Writes a new block of bytes to the end of a byte array.</span></span> <span data-ttu-id="4fe90-114">區塊的大小會指定為 [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend)的參數。</span><span class="sxs-lookup"><span data-stu-id="4fe90-114">The size of the block is specified as a parameter to [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span></span>

</dd> <dt>

<span data-ttu-id="4fe90-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span><span class="sxs-lookup"><span data-stu-id="4fe90-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span></span>
</dt> <dd>

<span data-ttu-id="4fe90-116">將新的資料區塊寫入位元組陣列中的指定位置。</span><span class="sxs-lookup"><span data-stu-id="4fe90-116">Writes a new block of data to a specified location in the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="4fe90-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span><span class="sxs-lookup"><span data-stu-id="4fe90-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span></span>
</dt> <dd>

<span data-ttu-id="4fe90-118">設定位元組陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="4fe90-118">Sets the size of the byte array.</span></span> <span data-ttu-id="4fe90-119">\_從呼叫 [**ILockBytes：： ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat)傳回 E 失敗，嘗試存取超過方法所指定之上限的資料。</span><span class="sxs-lookup"><span data-stu-id="4fe90-119">Returns E\_FAIL from calls to [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) that attempt to access data beyond the upper limit specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="4fe90-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes：： Terminate**</span><span class="sxs-lookup"><span data-stu-id="4fe90-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**</span></span>
</dt> <dd>

<span data-ttu-id="4fe90-121">通知位元組陣列，已成功或失敗的下載已終止。</span><span class="sxs-lookup"><span data-stu-id="4fe90-121">Informs the byte array that a download has been terminated, either successfully or unsuccessfully.</span></span>

</dd> </dl>

 

 




