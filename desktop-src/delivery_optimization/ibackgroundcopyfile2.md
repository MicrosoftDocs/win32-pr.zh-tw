---
title: 'IBackgroundCopyFile2 介面 (>deliveryoptimization .h) '
description: 使用 IBackgroundCopyFile2 介面指定檔案的新遠端名稱，並取出要下載的範圍清單。
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- IBackgroundCopyFile2 介面
- IBackgroundCopyFile2 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025008"
---
# <a name="ibackgroundcopyfile2-interface"></a><span data-ttu-id="e6696-105">IBackgroundCopyFile2 介面</span><span class="sxs-lookup"><span data-stu-id="e6696-105">IBackgroundCopyFile2 interface</span></span>

<span data-ttu-id="e6696-106">使用 **IBackgroundCopyFile2** 介面指定檔案的新遠端名稱，並取出要下載的範圍清單。</span><span class="sxs-lookup"><span data-stu-id="e6696-106">Use the **IBackgroundCopyFile2** interface to specify a new remote name for the file and retrieve the list of ranges to download.</span></span>

<span data-ttu-id="e6696-107">**IBackgroundCopyFile2** 介面繼承自 [**IBackgroundCopyFile**](ibackgroundcopyfile.md)介面。</span><span class="sxs-lookup"><span data-stu-id="e6696-107">The **IBackgroundCopyFile2** interface inherits from the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface.</span></span>

<span data-ttu-id="e6696-108">若要取得 **IBackgroundCopyFile2** 介面指標，請針對介面識別碼使用 __Uuidof (IBackgroundCopyFile2) 來呼叫 **IBackgroundCopyFile：： QueryInterface** 方法。</span><span class="sxs-lookup"><span data-stu-id="e6696-108">To get an **IBackgroundCopyFile2** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile2) for the interface identifier.</span></span> <span data-ttu-id="e6696-109">使用 **IBackgroundCopyFile2** 介面指標來呼叫 [**IBackgroundCopyFile**](ibackgroundcopyfile.md) 和 **IBackgroundCopyFile2** 方法。</span><span class="sxs-lookup"><span data-stu-id="e6696-109">Use the **IBackgroundCopyFile2** interface pointer to call both the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) and **IBackgroundCopyFile2** methods.</span></span>

## <a name="members"></a><span data-ttu-id="e6696-110">成員</span><span class="sxs-lookup"><span data-stu-id="e6696-110">Members</span></span>

<span data-ttu-id="e6696-111">**IBackgroundCopyFile2** 介面繼承自 [**IBackgroundCopyFile**](ibackgroundcopyfile.md)。</span><span class="sxs-lookup"><span data-stu-id="e6696-111">The **IBackgroundCopyFile2** interface inherits from [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span></span> <span data-ttu-id="e6696-112">**IBackgroundCopyFile2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e6696-112">**IBackgroundCopyFile2** also has these types of members:</span></span>

-   [<span data-ttu-id="e6696-113">方法</span><span class="sxs-lookup"><span data-stu-id="e6696-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e6696-114">方法</span><span class="sxs-lookup"><span data-stu-id="e6696-114">Methods</span></span>

<span data-ttu-id="e6696-115">**IBackgroundCopyFile2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e6696-115">The **IBackgroundCopyFile2** interface has these methods.</span></span>



| <span data-ttu-id="e6696-116">方法</span><span class="sxs-lookup"><span data-stu-id="e6696-116">Method</span></span>                                                             | <span data-ttu-id="e6696-117">描述</span><span class="sxs-lookup"><span data-stu-id="e6696-117">Description</span></span>                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="e6696-118">**GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="e6696-118">**GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md) | <span data-ttu-id="e6696-119">抓取您要從 URL 下載的範圍陣列。</span><span class="sxs-lookup"><span data-stu-id="e6696-119">Retrieves the array of ranges that you want to download from the URL.</span></span><br/> |
| [<span data-ttu-id="e6696-120">**SetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="e6696-120">**SetRemoteName**</span></span>](ibackgroundcopyfile2-setremotename-method.md) | <span data-ttu-id="e6696-121">將遠端名稱變更為新的 URL。</span><span class="sxs-lookup"><span data-stu-id="e6696-121">Changes the remote name to a new URL.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="e6696-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6696-122">Requirements</span></span>



| <span data-ttu-id="e6696-123">需求</span><span class="sxs-lookup"><span data-stu-id="e6696-123">Requirement</span></span> | <span data-ttu-id="e6696-124">值</span><span class="sxs-lookup"><span data-stu-id="e6696-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6696-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6696-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e6696-126">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6696-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e6696-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6696-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e6696-128">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6696-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e6696-129">標頭</span><span class="sxs-lookup"><span data-stu-id="e6696-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6696-130"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6696-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6696-131">Idl</span><span class="sxs-lookup"><span data-stu-id="e6696-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6696-132"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6696-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e6696-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6696-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6696-134"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6696-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e6696-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e6696-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6696-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6696-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e6696-137">IID</span><span class="sxs-lookup"><span data-stu-id="e6696-137">IID</span></span><br/>                      | <span data-ttu-id="e6696-138">IID_IBackgroundCopyFile2 定義為83E81B93-0873-474D-8A8C-F2018B1A939C</span><span class="sxs-lookup"><span data-stu-id="e6696-138">IID_IBackgroundCopyFile2 is defined as 83E81B93-0873-474D-8A8C-F2018B1A939C</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e6696-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6696-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6696-140">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="e6696-140">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> </dl>

 

 





