---
description: 釋放 IWiaPreview：： GetNewPreview 方法所快取的未篩選映射。 它也會釋放影像處理篩選。
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'IWiaPreview：： Clear 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972428"
---
# <a name="iwiapreviewclear-method"></a><span data-ttu-id="9c8cd-104">IWiaPreview：： Clear 方法</span><span class="sxs-lookup"><span data-stu-id="9c8cd-104">IWiaPreview::Clear method</span></span>

<span data-ttu-id="9c8cd-105">釋放 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法所快取的未篩選映射。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-105">Releases the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="9c8cd-106">它也會釋放影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-106">It also releases the image processing filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c8cd-107">語法</span><span class="sxs-lookup"><span data-stu-id="9c8cd-107">Syntax</span></span>


```C++
void Clear();
```



## <a name="parameters"></a><span data-ttu-id="9c8cd-108">參數</span><span class="sxs-lookup"><span data-stu-id="9c8cd-108">Parameters</span></span>

<span data-ttu-id="9c8cd-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c8cd-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c8cd-110">Return value</span></span>

<span data-ttu-id="9c8cd-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c8cd-112">備註</span><span class="sxs-lookup"><span data-stu-id="9c8cd-112">Remarks</span></span>

<span data-ttu-id="9c8cd-113">在 **IWiaPreview：： Clear** Windows 映像取得 (WIA) 2.0 Preview 元件會釋放它所儲存的所有介面指標。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-113">On **IWiaPreview::Clear** the Windows Image Acquisition (WIA) 2.0 Preview Component releases all interface pointers that it stores.</span></span> <span data-ttu-id="9c8cd-114">WIA 2.0 Preview 元件會保留傳遞給 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)的 *pWiaItem2* 和 *pWiaTransferCallback* 參考。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-114">The WIA 2.0 Preview Component keeps references to *pWiaItem2* and *pWiaTransferCallback* passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="9c8cd-115">為了精確起見，WIA 2.0 Preview 元件會保留 *pWiaItem2* 的參考和驅動程式的影像處理篩選，進而保留 *pWiaTransferCallback* 的參考。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-115">To be precise, the WIA 2.0 Preview Component keeps a reference to *pWiaItem2* and the driver's image processing filter, which in turn keeps a reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="9c8cd-116">在 **IWiaPreview：： Clear** 上，WIA 2.0 Preview 元件也會釋放其對 *pWiaItem2* 和影像處理篩選的參考，然後再釋放其對 *pWiaTransferCallback* 的參考。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-116">On **IWiaPreview::Clear**, the WIA 2.0 Preview Component also releases its reference to *pWiaItem2* and to the image processing filter, which in turn releases its reference to *pWiaTransferCallback*.</span></span> <span data-ttu-id="9c8cd-117">WIA 2.0 Preview 元件會刪除其儲存在內部的快取、未篩選的影像。</span><span class="sxs-lookup"><span data-stu-id="9c8cd-117">The WIA 2.0 Preview Component deletes the cached, unfiltered image that it stores internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8cd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c8cd-118">Requirements</span></span>



| <span data-ttu-id="9c8cd-119">需求</span><span class="sxs-lookup"><span data-stu-id="9c8cd-119">Requirement</span></span> | <span data-ttu-id="9c8cd-120">值</span><span class="sxs-lookup"><span data-stu-id="9c8cd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8cd-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c8cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9c8cd-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c8cd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9c8cd-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c8cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9c8cd-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c8cd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9c8cd-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9c8cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c8cd-126"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="9c8cd-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c8cd-127">Idl</span><span class="sxs-lookup"><span data-stu-id="9c8cd-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c8cd-128"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c8cd-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




