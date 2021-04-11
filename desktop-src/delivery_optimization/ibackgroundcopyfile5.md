---
title: 'IBackgroundCopyFile5 介面 (>deliveryoptimization .h) '
description: 您可以使用這個介面來取得或設定傳遞最佳化 (執行) 檔案傳輸的一般屬性。
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- IBackgroundCopyFile5 介面
- IBackgroundCopyFile5 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094455"
---
# <a name="ibackgroundcopyfile5-interface"></a><span data-ttu-id="21a16-105">IBackgroundCopyFile5 介面</span><span class="sxs-lookup"><span data-stu-id="21a16-105">IBackgroundCopyFile5 interface</span></span>

<span data-ttu-id="21a16-106">您可以使用這個介面來取得或設定傳遞最佳化 (執行) 檔案傳輸的一般屬性。</span><span class="sxs-lookup"><span data-stu-id="21a16-106">Use this interface to get or set generic properties of Delivery Optimization (DO) file transfers.</span></span>

<span data-ttu-id="21a16-107">若要取得 **IBackgroundCopyFile5** 介面指標，請針對介面識別碼使用 __Uuidof (IBackgroundCopyFile5) 來呼叫 **IBackgroundCopyFile：： QueryInterface** 方法。</span><span class="sxs-lookup"><span data-stu-id="21a16-107">To get an **IBackgroundCopyFile5** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile5) for the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="21a16-108">成員</span><span class="sxs-lookup"><span data-stu-id="21a16-108">Members</span></span>

<span data-ttu-id="21a16-109">**IBackgroundCopyFile5** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="21a16-109">The **IBackgroundCopyFile5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="21a16-110">**IBackgroundCopyFile5** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="21a16-110">**IBackgroundCopyFile5** also has these types of members:</span></span>

-   [<span data-ttu-id="21a16-111">方法</span><span class="sxs-lookup"><span data-stu-id="21a16-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21a16-112">方法</span><span class="sxs-lookup"><span data-stu-id="21a16-112">Methods</span></span>

<span data-ttu-id="21a16-113">**IBackgroundCopyFile5** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="21a16-113">The **IBackgroundCopyFile5** interface has these methods.</span></span>



| <span data-ttu-id="21a16-114">方法</span><span class="sxs-lookup"><span data-stu-id="21a16-114">Method</span></span>                                                  | <span data-ttu-id="21a16-115">描述</span><span class="sxs-lookup"><span data-stu-id="21a16-115">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="21a16-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="21a16-116">**GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md) | <span data-ttu-id="21a16-117">取得泛型 BackgroundCopyFile 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="21a16-117">Gets the value of a generic BackgroundCopyFile property.</span></span><br/> |
| [<span data-ttu-id="21a16-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="21a16-118">**SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md) | <span data-ttu-id="21a16-119">設定泛型 BackgroundCopyFile 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="21a16-119">Sets the value of a generic BackgroundCopyFile property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21a16-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="21a16-120">Requirements</span></span>



| <span data-ttu-id="21a16-121">需求</span><span class="sxs-lookup"><span data-stu-id="21a16-121">Requirement</span></span> | <span data-ttu-id="21a16-122">值</span><span class="sxs-lookup"><span data-stu-id="21a16-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21a16-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21a16-123">Minimum supported client</span></span><br/> | <span data-ttu-id="21a16-124">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21a16-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="21a16-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21a16-125">Minimum supported server</span></span><br/> | <span data-ttu-id="21a16-126">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21a16-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="21a16-127">標頭</span><span class="sxs-lookup"><span data-stu-id="21a16-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="21a16-128"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="21a16-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="21a16-129">Idl</span><span class="sxs-lookup"><span data-stu-id="21a16-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21a16-130"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="21a16-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="21a16-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="21a16-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="21a16-132"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21a16-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="21a16-133">DLL</span><span class="sxs-lookup"><span data-stu-id="21a16-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21a16-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21a16-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="21a16-135">IID</span><span class="sxs-lookup"><span data-stu-id="21a16-135">IID</span></span><br/>                      | <span data-ttu-id="21a16-136">IID_IBackgroundCopyFile5 定義為85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="21a16-136">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="21a16-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21a16-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a16-138">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="21a16-138">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="21a16-139">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="21a16-139">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

