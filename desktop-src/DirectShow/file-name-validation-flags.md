---
description: 這些旗標會指定媒體定位器的行為。
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: '檔案名驗證旗標 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985564"
---
# <a name="file-name-validation-flags"></a><span data-ttu-id="740bc-103">檔案名驗證旗標</span><span class="sxs-lookup"><span data-stu-id="740bc-103">File Name Validation Flags</span></span>

<span data-ttu-id="740bc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="740bc-104">\[Deprecated.</span></span> <span data-ttu-id="740bc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="740bc-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="740bc-106">這些旗標會指定媒體定位器的行為。</span><span class="sxs-lookup"><span data-stu-id="740bc-106">These flags specify the behavior of the media locator.</span></span>



| <span data-ttu-id="740bc-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="740bc-107">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="740bc-108">Description</span><span class="sxs-lookup"><span data-stu-id="740bc-108">Description</span></span>                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <span data-ttu-id="740bc-109"><dt>**SFN \_VALIDATEF \_ 檢查**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="740bc-109"><dt>**SFN\_VALIDATEF\_CHECK**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="740bc-110">檢查檔案名的有效性。</span><span class="sxs-lookup"><span data-stu-id="740bc-110">Check the validity of file names.</span></span> <span data-ttu-id="740bc-111">您必須設定這個旗標以驗證檔案名。</span><span class="sxs-lookup"><span data-stu-id="740bc-111">You must set this flag to validate file names.</span></span> <span data-ttu-id="740bc-112">如果不是，則其他旗標沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="740bc-112">If not, the other flags have no effect.</span></span><br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <span data-ttu-id="740bc-113"><dt>**SFN \_VALIDATEF \_ POPUP**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="740bc-113"><dt>**SFN\_VALIDATEF\_POPUP**</dt> <dt>0x02</dt></span></span> </dl>                   | <span data-ttu-id="740bc-114">如果找不到檔案，則會顯示使用者的 [開啟檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="740bc-114">If a file is not located, display an Open File dialog box for the end user.</span></span><br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <span data-ttu-id="740bc-115"><dt>**SFN \_VALIDATEF \_ TELLME**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="740bc-115"><dt>**SFN\_VALIDATEF\_TELLME**</dt> <dt>0x04</dt></span></span> </dl>                | <span data-ttu-id="740bc-116">如果找不到檔案，請使用檔案的名稱和位置來短暫顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="740bc-116">If a missing file is located, briefly display a message box with the name and location of the file.</span></span> <span data-ttu-id="740bc-117">此旗標大多適用于測試用途;訊息方塊可能不適合零售產品。</span><span class="sxs-lookup"><span data-stu-id="740bc-117">This flag is mostly useful for testing purposes; the message box is probably not suitable for a retail product.</span></span><br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <span data-ttu-id="740bc-118"><dt>**SFN \_VALIDATEF \_ REPLACE**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="740bc-118"><dt>**SFN\_VALIDATEF\_REPLACE**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="740bc-119">如果找不到檔案，請更新來源物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="740bc-119">If a missing file is located, update the name of the source object.</span></span> <span data-ttu-id="740bc-120"> (僅適用于 [**IAMTimeline：： ValidateSourceNames**](iamtimeline-validatesourcenames.md) 方法。 ) </span><span class="sxs-lookup"><span data-stu-id="740bc-120">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <span data-ttu-id="740bc-121"><dt>**SFN \_VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="740bc-121"><dt>**SFN\_VALIDATEF\_USELOCAL**</dt> <dt>0x10</dt></span></span> </dl>          | <span data-ttu-id="740bc-122">一律使用本機檔案，即使網路上有檔案版本也一樣。</span><span class="sxs-lookup"><span data-stu-id="740bc-122">Always use a local file, even if a version of the file exists on the network.</span></span><br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <span data-ttu-id="740bc-123"><dt>**SFN \_VALIDATEF \_ NOFIND**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="740bc-123"><dt>**SFN\_VALIDATEF\_NOFIND**</dt> <dt>0x20</dt></span></span> </dl>                | <span data-ttu-id="740bc-124">請勿搜尋遺失的檔案。</span><span class="sxs-lookup"><span data-stu-id="740bc-124">Do not search for missing files.</span></span> <span data-ttu-id="740bc-125">如果您設定 SFN \_ VALIDATEF 檢查旗標，仍會驗證檔案名 \_ 。</span><span class="sxs-lookup"><span data-stu-id="740bc-125">File names are still validated if you set the SFN\_VALIDATEF\_CHECK flag.</span></span><br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <span data-ttu-id="740bc-126"><dt>**SFN \_VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="740bc-126"><dt>**SFN\_VALIDATEF\_IGNOREMUTED**</dt> <dt>0x40</dt></span></span> </dl> | <span data-ttu-id="740bc-127">略過靜音來源物件。</span><span class="sxs-lookup"><span data-stu-id="740bc-127">Ignore muted source objects.</span></span> <span data-ttu-id="740bc-128"> (僅適用于 [**IAMTimeline：： ValidateSourceNames**](iamtimeline-validatesourcenames.md) 方法。 ) </span><span class="sxs-lookup"><span data-stu-id="740bc-128">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                                                                |



## <a name="requirements"></a><span data-ttu-id="740bc-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="740bc-129">Requirements</span></span>



| <span data-ttu-id="740bc-130">需求</span><span class="sxs-lookup"><span data-stu-id="740bc-130">Requirement</span></span> | <span data-ttu-id="740bc-131">值</span><span class="sxs-lookup"><span data-stu-id="740bc-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="740bc-132">標頭</span><span class="sxs-lookup"><span data-stu-id="740bc-132">Header</span></span><br/> | <dl> <span data-ttu-id="740bc-133"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="740bc-133"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="740bc-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="740bc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740bc-135">**IMediaLocator::FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="740bc-135">**IMediaLocator::FindMediaFile**</span></span>](imedialocator-findmediafile.md)
</dt> <dt>

[<span data-ttu-id="740bc-136">**IRenderEngine::SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="740bc-136">**IRenderEngine::SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




