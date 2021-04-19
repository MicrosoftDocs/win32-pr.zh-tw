---
description: Get \_ Count 方法會取得屬性的數目。
ms.assetid: dc607f09-4cca-4ef0-8b86-dbc5e6edcfdd
title: 'ITAttributeList：： get_Count 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634996e8d920005f5da4c40b6cfca3f5cb632363
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990815"
---
# <a name="itattributelistget_count-method"></a><span data-ttu-id="1a738-103">ITAttributeList：： get \_ Count 方法</span><span class="sxs-lookup"><span data-stu-id="1a738-103">ITAttributeList::get\_Count method</span></span>

<span data-ttu-id="1a738-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="1a738-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1a738-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="1a738-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1a738-106">**Get \_ Count** 方法會取得屬性的數目。</span><span class="sxs-lookup"><span data-stu-id="1a738-106">The **get\_Count** method gets the number of attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a738-107">語法</span><span class="sxs-lookup"><span data-stu-id="1a738-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1a738-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a738-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a738-109">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1a738-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a738-110">清單中屬性的計數。</span><span class="sxs-lookup"><span data-stu-id="1a738-110">Count of the attributes in the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a738-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a738-111">Return value</span></span>

<span data-ttu-id="1a738-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1a738-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1a738-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1a738-113">Return code</span></span>                                                                                   | <span data-ttu-id="1a738-114">Description</span><span class="sxs-lookup"><span data-stu-id="1a738-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1a738-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1a738-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="1a738-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1a738-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1a738-118">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="1a738-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="1a738-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1a738-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="1a738-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1a738-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1a738-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a738-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1a738-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1a738-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="1a738-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="1a738-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a738-125">Requirements</span></span>



| <span data-ttu-id="1a738-126">需求</span><span class="sxs-lookup"><span data-stu-id="1a738-126">Requirement</span></span> | <span data-ttu-id="1a738-127">值</span><span class="sxs-lookup"><span data-stu-id="1a738-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a738-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="1a738-128">TAPI version</span></span><br/> | <span data-ttu-id="1a738-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1a738-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1a738-130">標頭</span><span class="sxs-lookup"><span data-stu-id="1a738-130">Header</span></span><br/>       | <dl> <span data-ttu-id="1a738-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a738-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a738-132">Library</span></span><br/>      | <dl> <span data-ttu-id="1a738-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1a738-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1a738-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="1a738-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a738-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a738-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a738-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="1a738-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




