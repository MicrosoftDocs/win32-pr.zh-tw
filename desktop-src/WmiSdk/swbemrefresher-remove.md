---
description: SWbemRefresher 方法會從複習中移除具有指定索引的 SWbemRefreshableItem 物件。
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: 'SWbemRefresher： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945676"
---
# <a name="swbemrefresherremove-method"></a><span data-ttu-id="41e4d-103">SWbemRefresher 方法</span><span class="sxs-lookup"><span data-stu-id="41e4d-103">SWbemRefresher.Remove method</span></span>

<span data-ttu-id="41e4d-104">**SWbemRefresher** 方法會從複習中移除具有指定索引的 [**SWbemRefreshableItem**](swbemrefreshableitem.md)物件。</span><span class="sxs-lookup"><span data-stu-id="41e4d-104">The **SWbemRefresher.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object with the specified index from the refresher.</span></span> <span data-ttu-id="41e4d-105">**SWbemRefreshableItem** 物件可以是單一物件或物件集。</span><span class="sxs-lookup"><span data-stu-id="41e4d-105">The **SWbemRefreshableItem** object can represent either a single object or an object set.</span></span>

<span data-ttu-id="41e4d-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="41e4d-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="41e4d-107">語法</span><span class="sxs-lookup"><span data-stu-id="41e4d-107">Syntax</span></span>


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="41e4d-108">參數</span><span class="sxs-lookup"><span data-stu-id="41e4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e4d-109">*LIndex*</span><span class="sxs-lookup"><span data-stu-id="41e4d-109">*LIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="41e4d-110">[**SWbemRefresher**](swbemrefresher.md)物件中專案的索引。</span><span class="sxs-lookup"><span data-stu-id="41e4d-110">Index of the item in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="41e4d-111">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="41e4d-111">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41e4d-112">旗標必須設定為 t0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="41e4d-112">Flags must be set t0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="41e4d-113">*objWbemNamedvalueSet* \[選\]</span><span class="sxs-lookup"><span data-stu-id="41e4d-113">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41e4d-114">Null。</span><span class="sxs-lookup"><span data-stu-id="41e4d-114">Null.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e4d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="41e4d-115">Return value</span></span>

<span data-ttu-id="41e4d-116">這個方法沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="41e4d-116">This method has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e4d-117">備註</span><span class="sxs-lookup"><span data-stu-id="41e4d-117">Remarks</span></span>

<span data-ttu-id="41e4d-118">**錯誤碼** 如果重新整理程式沒有具有指定之索引的專案，就會產生 **wbemErrNotFound** 。</span><span class="sxs-lookup"><span data-stu-id="41e4d-118">**Error codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="41e4d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="41e4d-119">Requirements</span></span>



| <span data-ttu-id="41e4d-120">需求</span><span class="sxs-lookup"><span data-stu-id="41e4d-120">Requirement</span></span> | <span data-ttu-id="41e4d-121">值</span><span class="sxs-lookup"><span data-stu-id="41e4d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41e4d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41e4d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="41e4d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41e4d-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41e4d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41e4d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="41e4d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41e4d-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41e4d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="41e4d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="41e4d-127"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="41e4d-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="41e4d-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="41e4d-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="41e4d-129"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="41e4d-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="41e4d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="41e4d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41e4d-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41e4d-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="41e4d-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="41e4d-132">CLSID</span></span><br/>                    | <span data-ttu-id="41e4d-133">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="41e4d-133">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="41e4d-134">IID</span><span class="sxs-lookup"><span data-stu-id="41e4d-134">IID</span></span><br/>                      | <span data-ttu-id="41e4d-135">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="41e4d-135">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="41e4d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41e4d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e4d-137">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="41e4d-137">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




