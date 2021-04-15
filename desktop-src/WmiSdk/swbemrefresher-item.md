---
description: SWbemRefresher 方法會從集合傳回指定的 SWbemRefreshableItem。從集合 SWbemRefreshableItem。
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: 'SWbemRefresher 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195734"
---
# <a name="swbemrefresheritem-method"></a><span data-ttu-id="30a5b-103">SWbemRefresher 專案方法</span><span class="sxs-lookup"><span data-stu-id="30a5b-103">SWbemRefresher.Item method</span></span>

<span data-ttu-id="30a5b-104">**SWbemRefresher** 方法會從集合傳回指定的 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 。</span><span class="sxs-lookup"><span data-stu-id="30a5b-104">The **SWbemRefresher.Item** method returns the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) from the collection.</span></span>

<span data-ttu-id="30a5b-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="30a5b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30a5b-106">語法</span><span class="sxs-lookup"><span data-stu-id="30a5b-106">Syntax</span></span>


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="30a5b-107">參數</span><span class="sxs-lookup"><span data-stu-id="30a5b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a5b-108">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="30a5b-108">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="30a5b-109">集合中專案的索引值。</span><span class="sxs-lookup"><span data-stu-id="30a5b-109">Index value of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a5b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="30a5b-110">Return value</span></span>

<span data-ttu-id="30a5b-111">如果呼叫成功，則會傳回指定的 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="30a5b-111">If the call is successful, the specified [**SWbemRefreshableItem**](swbemrefreshableitem.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30a5b-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="30a5b-112">Error codes</span></span>

<span data-ttu-id="30a5b-113">如果重新整理程式沒有具有指定之索引的專案，就會產生 **wbemErrNotFound** 。</span><span class="sxs-lookup"><span data-stu-id="30a5b-113">If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a5b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="30a5b-114">Requirements</span></span>



| <span data-ttu-id="30a5b-115">需求</span><span class="sxs-lookup"><span data-stu-id="30a5b-115">Requirement</span></span> | <span data-ttu-id="30a5b-116">值</span><span class="sxs-lookup"><span data-stu-id="30a5b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30a5b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30a5b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30a5b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30a5b-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30a5b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30a5b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30a5b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30a5b-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30a5b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="30a5b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="30a5b-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="30a5b-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="30a5b-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="30a5b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="30a5b-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30a5b-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30a5b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="30a5b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30a5b-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30a5b-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="30a5b-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="30a5b-127">CLSID</span></span><br/>                    | <span data-ttu-id="30a5b-128">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="30a5b-128">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="30a5b-129">IID</span><span class="sxs-lookup"><span data-stu-id="30a5b-129">IID</span></span><br/>                      | <span data-ttu-id="30a5b-130">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="30a5b-130">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="30a5b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30a5b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a5b-132">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="30a5b-132">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




