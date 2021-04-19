---
description: SWbemRefreshableItem 方法會從父 SWbemRefresher 物件中移除 SWbemRefreshableItem 物件。父 SWbemRefresher 物件的 SWbemRefreshableItem 物件。
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: 'SWbemRefreshableItem： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106989116"
---
# <a name="swbemrefreshableitemremove-method"></a><span data-ttu-id="2db8c-103">SWbemRefreshableItem 方法</span><span class="sxs-lookup"><span data-stu-id="2db8c-103">SWbemRefreshableItem.Remove method</span></span>

<span data-ttu-id="2db8c-104">**SWbemRefreshableItem** 方法會從父 [**SWbemRefresher**](swbemrefresher.md)物件中移除 [**SWbemRefreshableItem**](swbemrefreshableitem.md)物件。</span><span class="sxs-lookup"><span data-stu-id="2db8c-104">The **SWbemRefreshableItem.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="2db8c-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2db8c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2db8c-106">語法</span><span class="sxs-lookup"><span data-stu-id="2db8c-106">Syntax</span></span>


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2db8c-107">參數</span><span class="sxs-lookup"><span data-stu-id="2db8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db8c-108">*lFlags* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="2db8c-108">*lFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2db8c-109">此參數必須設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="2db8c-109">This parameter must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db8c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="2db8c-110">Return value</span></span>

<span data-ttu-id="2db8c-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2db8c-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db8c-112">備註</span><span class="sxs-lookup"><span data-stu-id="2db8c-112">Remarks</span></span>

<span data-ttu-id="2db8c-113">**錯誤碼** 如果重新整理程式沒有具有指定之索引的專案，就會產生 **wbemErrNotFound** 。</span><span class="sxs-lookup"><span data-stu-id="2db8c-113">**Error Codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="2db8c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2db8c-114">Requirements</span></span>



| <span data-ttu-id="2db8c-115">需求</span><span class="sxs-lookup"><span data-stu-id="2db8c-115">Requirement</span></span> | <span data-ttu-id="2db8c-116">值</span><span class="sxs-lookup"><span data-stu-id="2db8c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2db8c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2db8c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2db8c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2db8c-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2db8c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2db8c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2db8c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2db8c-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2db8c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2db8c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db8c-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2db8c-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2db8c-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2db8c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="2db8c-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2db8c-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2db8c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2db8c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2db8c-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2db8c-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2db8c-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="2db8c-127">CLSID</span></span><br/>                    | <span data-ttu-id="2db8c-128">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="2db8c-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="2db8c-129">IID</span><span class="sxs-lookup"><span data-stu-id="2db8c-129">IID</span></span><br/>                      | <span data-ttu-id="2db8c-130">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="2db8c-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="2db8c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2db8c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db8c-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="2db8c-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="2db8c-133">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="2db8c-133">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




