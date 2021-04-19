---
description: Get \_ \_ NewEnum 方法會傳回集合的列舉值。
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: 'ITTimeCollection：： get__NewEnum 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3fbd171696b81bf5bd67c99b9a91294f4581d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001813"
---
# <a name="ittimecollectionget__newenum-method"></a><span data-ttu-id="c1531-103">ITTimeCollection：： get \_ \_ NewEnum 方法</span><span class="sxs-lookup"><span data-stu-id="c1531-103">ITTimeCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="c1531-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="c1531-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c1531-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c1531-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c1531-106">**Get \_ \_ NewEnum** 方法會傳回集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="c1531-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1531-107">語法</span><span class="sxs-lookup"><span data-stu-id="c1531-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c1531-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1531-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1531-109">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c1531-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1531-110">集合之列舉值物件的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="c1531-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="c1531-111">在傳回的 **IUnknown** 介面上呼叫 [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法，以取得集合上 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)列舉介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c1531-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="c1531-112">**IEnumVARIANT** 提供數種方法，可讓您用來逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="c1531-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="c1531-113">如需詳細資訊，請參閱接下來的＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="c1531-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1531-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1531-114">Return value</span></span>

<span data-ttu-id="c1531-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c1531-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c1531-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c1531-116">Return code</span></span>                                                                                   | <span data-ttu-id="c1531-117">Description</span><span class="sxs-lookup"><span data-stu-id="c1531-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c1531-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c1531-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c1531-119">方法成功。</span><span class="sxs-lookup"><span data-stu-id="c1531-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c1531-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c1531-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c1531-121">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="c1531-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="c1531-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c1531-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1531-123">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c1531-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c1531-124"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="c1531-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c1531-125">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1531-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c1531-126"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c1531-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c1531-127">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="c1531-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="c1531-128">備註</span><span class="sxs-lookup"><span data-stu-id="c1531-128">Remarks</span></span>

<span data-ttu-id="c1531-129">這個方法可以與 [**get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) 互換，不同之處在于它會傳回 **IUnknown** 而不是 [**IEnumTime**](ienumtime.md)。</span><span class="sxs-lookup"><span data-stu-id="c1531-129">This method is interchangeable with [**get\_EnumerationIf**](ittimecollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumTime**](ienumtime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1531-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1531-130">Requirements</span></span>



| <span data-ttu-id="c1531-131">需求</span><span class="sxs-lookup"><span data-stu-id="c1531-131">Requirement</span></span> | <span data-ttu-id="c1531-132">值</span><span class="sxs-lookup"><span data-stu-id="c1531-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1531-133">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c1531-133">TAPI version</span></span><br/> | <span data-ttu-id="c1531-134">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c1531-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c1531-135">標頭</span><span class="sxs-lookup"><span data-stu-id="c1531-135">Header</span></span><br/>       | <dl> <span data-ttu-id="c1531-136"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1531-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1531-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1531-137">Library</span></span><br/>      | <dl> <span data-ttu-id="c1531-138"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="c1531-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c1531-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c1531-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="c1531-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1531-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1531-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1531-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1531-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="c1531-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="c1531-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="c1531-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

