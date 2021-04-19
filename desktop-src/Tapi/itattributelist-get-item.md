---
description: Get \_ Item 方法會傳回索引所指定的屬性。
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: 'ITAttributeList：： get_Item 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33745c10bf95fe8a1e9c6d9edc73cad54855a8c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999706"
---
# <a name="itattributelistget_item-method"></a><span data-ttu-id="6d2e1-103">ITAttributeList：： get \_ Item 方法</span><span class="sxs-lookup"><span data-stu-id="6d2e1-103">ITAttributeList::get\_Item method</span></span>

<span data-ttu-id="6d2e1-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6d2e1-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6d2e1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6d2e1-106">**Get \_ Item** 方法會傳回索引所指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-106">The **get\_Item** method returns the attribute specified by the index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2e1-107">語法</span><span class="sxs-lookup"><span data-stu-id="6d2e1-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6d2e1-108">參數</span><span class="sxs-lookup"><span data-stu-id="6d2e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d2e1-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6d2e1-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2e1-110">要取得之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="6d2e1-111">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6d2e1-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d2e1-112">包含專案值之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-112">Pointer to a **BSTR** containing the values of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d2e1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d2e1-113">Return value</span></span>

<span data-ttu-id="6d2e1-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="6d2e1-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6d2e1-115">Return code</span></span>                                                                                   | <span data-ttu-id="6d2e1-116">Description</span><span class="sxs-lookup"><span data-stu-id="6d2e1-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6d2e1-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6d2e1-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6d2e1-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6d2e1-120">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="6d2e1-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6d2e1-122">*索引* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="6d2e1-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6d2e1-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="6d2e1-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="6d2e1-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6d2e1-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="6d2e1-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6d2e1-129">備註</span><span class="sxs-lookup"><span data-stu-id="6d2e1-129">Remarks</span></span>

<span data-ttu-id="6d2e1-130">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *pVal* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d2e1-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *pVal* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d2e1-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d2e1-131">Requirements</span></span>



| <span data-ttu-id="6d2e1-132">需求</span><span class="sxs-lookup"><span data-stu-id="6d2e1-132">Requirement</span></span> | <span data-ttu-id="6d2e1-133">值</span><span class="sxs-lookup"><span data-stu-id="6d2e1-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2e1-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="6d2e1-134">TAPI version</span></span><br/> | <span data-ttu-id="6d2e1-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6d2e1-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6d2e1-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6d2e1-136">Header</span></span><br/>       | <dl> <span data-ttu-id="6d2e1-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d2e1-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="6d2e1-138">Library</span></span><br/>      | <dl> <span data-ttu-id="6d2e1-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6d2e1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6d2e1-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="6d2e1-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e1-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d2e1-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d2e1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d2e1-143">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="6d2e1-143">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

