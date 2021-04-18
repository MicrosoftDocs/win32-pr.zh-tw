---
title: 'IEnumBackgroundCopyFiles 介面 (>deliveryoptimization .h) '
description: 您可以使用 IEnumBackgroundCopyFiles 介面來列舉作業所包含的檔案。 若要取得 IEnumBackgroundCopyFiles 介面指標，請呼叫 IBackgroundCopyJob EnumFiles 方法。
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，說明
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965489"
---
# <a name="ienumbackgroundcopyfiles-interface"></a><span data-ttu-id="4f851-106">IEnumBackgroundCopyFiles 介面</span><span class="sxs-lookup"><span data-stu-id="4f851-106">IEnumBackgroundCopyFiles interface</span></span>

<span data-ttu-id="4f851-107">您可以使用 **IEnumBackgroundCopyFiles** 介面來列舉作業所包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="4f851-107">Use the **IEnumBackgroundCopyFiles** interface to enumerate the files that a job contains.</span></span> <span data-ttu-id="4f851-108">若要取得 **IEnumBackgroundCopyFiles** 介面指標，請呼叫 [**IBackgroundCopyJob：： EnumFiles**](ibackgroundcopyjob-enumfiles.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4f851-108">To get an **IEnumBackgroundCopyFiles** interface pointer, call the [**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="4f851-109">成員</span><span class="sxs-lookup"><span data-stu-id="4f851-109">Members</span></span>

<span data-ttu-id="4f851-110">**IEnumBackgroundCopyFiles** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="4f851-110">The **IEnumBackgroundCopyFiles** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4f851-111">**IEnumBackgroundCopyFiles** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4f851-111">**IEnumBackgroundCopyFiles** also has these types of members:</span></span>

-   [<span data-ttu-id="4f851-112">方法</span><span class="sxs-lookup"><span data-stu-id="4f851-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4f851-113">方法</span><span class="sxs-lookup"><span data-stu-id="4f851-113">Methods</span></span>

<span data-ttu-id="4f851-114">**IEnumBackgroundCopyFiles** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4f851-114">The **IEnumBackgroundCopyFiles** interface has these methods.</span></span>



| <span data-ttu-id="4f851-115">方法</span><span class="sxs-lookup"><span data-stu-id="4f851-115">Method</span></span>                                                | <span data-ttu-id="4f851-116">描述</span><span class="sxs-lookup"><span data-stu-id="4f851-116">Description</span></span>                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="4f851-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="4f851-117">**GetCount**</span></span>](ienumbackgroundcopyfiles-getcount.md) | <span data-ttu-id="4f851-118">捕獲列舉中的專案數。</span><span class="sxs-lookup"><span data-stu-id="4f851-118">Retrieves the number of items in the enumeration.</span></span><br/>                  |
| [<span data-ttu-id="4f851-119">**下一步**</span><span class="sxs-lookup"><span data-stu-id="4f851-119">**Next**</span></span>](ienumbackgroundcopyfiles-next.md)         | <span data-ttu-id="4f851-120">擷取列舉型別序列中指定的項目數目。</span><span class="sxs-lookup"><span data-stu-id="4f851-120">Retrieves a specified number of items in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="4f851-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="4f851-121">**Reset**</span></span>](ienumbackgroundcopyfiles-reset.md)       | <span data-ttu-id="4f851-122">將列舉序列重設為開頭。</span><span class="sxs-lookup"><span data-stu-id="4f851-122">Resets the enumeration sequence to the beginning.</span></span><br/>                  |
| [<span data-ttu-id="4f851-123">**跳過**</span><span class="sxs-lookup"><span data-stu-id="4f851-123">**Skip**</span></span>](ienumbackgroundcopyfiles-skip.md)         | <span data-ttu-id="4f851-124">略過列舉序列中指定的項目數目。</span><span class="sxs-lookup"><span data-stu-id="4f851-124">Skips a specified number of items in the enumeration sequence.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="4f851-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f851-125">Requirements</span></span>



| <span data-ttu-id="4f851-126">需求</span><span class="sxs-lookup"><span data-stu-id="4f851-126">Requirement</span></span> | <span data-ttu-id="4f851-127">值</span><span class="sxs-lookup"><span data-stu-id="4f851-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f851-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f851-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4f851-129">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f851-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4f851-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f851-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4f851-131">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f851-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4f851-132">標頭</span><span class="sxs-lookup"><span data-stu-id="4f851-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f851-133"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f851-133"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f851-134">Idl</span><span class="sxs-lookup"><span data-stu-id="4f851-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f851-135"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f851-135"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4f851-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="4f851-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f851-137"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f851-137"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4f851-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4f851-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f851-139"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f851-139"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4f851-140">IID</span><span class="sxs-lookup"><span data-stu-id="4f851-140">IID</span></span><br/>                      | <span data-ttu-id="4f851-141">IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="4f851-141">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="4f851-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f851-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f851-143">**IBackgroundCopyJob：： EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="4f851-143">**IBackgroundCopyJob::EnumFiles**</span></span>](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

