---
title: 'IBackgroundCopyFile 介面 (>deliveryoptimization .h) '
description: IBackgroundCopyFile 包含屬於作業一部分之檔案的相關資訊。 例如，您可以使用 IBackgroundCopyFile 方法來取出檔案的本機和遠端名稱，並傳送進度資訊。
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- IBackgroundCopyFile 介面
- IBackgroundCopyFile 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969581"
---
# <a name="ibackgroundcopyfile-interface"></a><span data-ttu-id="7f5c0-106">IBackgroundCopyFile 介面</span><span class="sxs-lookup"><span data-stu-id="7f5c0-106">IBackgroundCopyFile interface</span></span>

<span data-ttu-id="7f5c0-107">**IBackgroundCopyFile** 包含屬於作業一部分之檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f5c0-107">**IBackgroundCopyFile** contains information about a file that is part of a job.</span></span> <span data-ttu-id="7f5c0-108">例如，您可以使用 **IBackgroundCopyFile** 方法來取出檔案的本機和遠端名稱，並傳送進度資訊。</span><span class="sxs-lookup"><span data-stu-id="7f5c0-108">For example, you can use **IBackgroundCopyFile** methods to retrieve the local and remote names of the file and transfer progress information.</span></span>

<span data-ttu-id="7f5c0-109">若要取得 **IBackgroundCopyFile** 介面指標，請呼叫 [**IBackgroundCopyError：： GetFile**](ibackgroundcopyerror-getfile-method.md) 方法或 [**IEnumBackgroundCopyFiles：： Next**](ienumbackgroundcopyfiles-next.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7f5c0-109">To get an **IBackgroundCopyFile** interface pointer, call the [**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md) method or the [**IEnumBackgroundCopyFiles::Next**](ienumbackgroundcopyfiles-next.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="7f5c0-110">成員</span><span class="sxs-lookup"><span data-stu-id="7f5c0-110">Members</span></span>

<span data-ttu-id="7f5c0-111">**IBackgroundCopyFile** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7f5c0-111">The **IBackgroundCopyFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7f5c0-112">**IBackgroundCopyFile** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7f5c0-112">**IBackgroundCopyFile** also has these types of members:</span></span>

-   [<span data-ttu-id="7f5c0-113">方法</span><span class="sxs-lookup"><span data-stu-id="7f5c0-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7f5c0-114">方法</span><span class="sxs-lookup"><span data-stu-id="7f5c0-114">Methods</span></span>

<span data-ttu-id="7f5c0-115">**IBackgroundCopyFile** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7f5c0-115">The **IBackgroundCopyFile** interface has these methods.</span></span>



| <span data-ttu-id="7f5c0-116">方法</span><span class="sxs-lookup"><span data-stu-id="7f5c0-116">Method</span></span>                                                            | <span data-ttu-id="7f5c0-117">描述</span><span class="sxs-lookup"><span data-stu-id="7f5c0-117">Description</span></span>                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="7f5c0-118">**GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="7f5c0-118">**GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)   | <span data-ttu-id="7f5c0-119">抓取檔案的本機名稱。</span><span class="sxs-lookup"><span data-stu-id="7f5c0-119">Retrieves the local name of the file.</span></span><br/>        |
| [<span data-ttu-id="7f5c0-120">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="7f5c0-120">**GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)     | <span data-ttu-id="7f5c0-121">捕獲檔案傳輸的進度。</span><span class="sxs-lookup"><span data-stu-id="7f5c0-121">Retrieves the progress of the file transfer.</span></span><br/> |
| [<span data-ttu-id="7f5c0-122">**GetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="7f5c0-122">**GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md) | <span data-ttu-id="7f5c0-123">抓取檔案的遠端名稱。</span><span class="sxs-lookup"><span data-stu-id="7f5c0-123">Retrieves the remote name of the file.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="7f5c0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f5c0-124">Requirements</span></span>



| <span data-ttu-id="7f5c0-125">需求</span><span class="sxs-lookup"><span data-stu-id="7f5c0-125">Requirement</span></span> | <span data-ttu-id="7f5c0-126">值</span><span class="sxs-lookup"><span data-stu-id="7f5c0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f5c0-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f5c0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7f5c0-128">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f5c0-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7f5c0-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f5c0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7f5c0-130">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f5c0-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7f5c0-131">標頭</span><span class="sxs-lookup"><span data-stu-id="7f5c0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f5c0-132"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f5c0-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f5c0-133">Idl</span><span class="sxs-lookup"><span data-stu-id="7f5c0-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f5c0-134"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f5c0-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7f5c0-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f5c0-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f5c0-136"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f5c0-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7f5c0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7f5c0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f5c0-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f5c0-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7f5c0-139">IID</span><span class="sxs-lookup"><span data-stu-id="7f5c0-139">IID</span></span><br/>                      | <span data-ttu-id="7f5c0-140">IID_IBackgroundCopyFile 定義為01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="7f5c0-140">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="7f5c0-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f5c0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f5c0-142">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="7f5c0-142">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="7f5c0-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="7f5c0-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> <dt>

[<span data-ttu-id="7f5c0-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="7f5c0-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="7f5c0-145">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="7f5c0-145">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

