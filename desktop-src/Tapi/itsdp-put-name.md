---
description: Put \_ name 方法會設定會話名稱。
ms.assetid: aba05cdb-a870-490e-8bb0-98b11780b112
title: 'ITSdp：:p ut_Name 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7383183b6b367d71d18070eedd5857740665fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992924"
---
# <a name="itsdpput_name-method"></a><span data-ttu-id="8d6cf-103">ITSdp：:p 的內容 \_ 名稱方法</span><span class="sxs-lookup"><span data-stu-id="8d6cf-103">ITSdp::put\_Name method</span></span>

<span data-ttu-id="8d6cf-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8d6cf-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="8d6cf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8d6cf-106">**Put \_ name** 方法會設定會話名稱。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-106">The **put\_Name** method sets the session name.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d6cf-107">語法</span><span class="sxs-lookup"><span data-stu-id="8d6cf-107">Syntax</span></span>


```C++
HRESULT put_Name(
  [in] BSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="8d6cf-108">參數</span><span class="sxs-lookup"><span data-stu-id="8d6cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d6cf-109">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d6cf-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d6cf-110">包含會話名稱之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-110">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d6cf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d6cf-111">Return value</span></span>

<span data-ttu-id="8d6cf-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8d6cf-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8d6cf-113">Return code</span></span>                                                                                   | <span data-ttu-id="8d6cf-114">Description</span><span class="sxs-lookup"><span data-stu-id="8d6cf-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8d6cf-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cf-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8d6cf-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8d6cf-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cf-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8d6cf-118">*PName* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-118">The *pName* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="8d6cf-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cf-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8d6cf-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8d6cf-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cf-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8d6cf-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8d6cf-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cf-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8d6cf-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8d6cf-125">備註</span><span class="sxs-lookup"><span data-stu-id="8d6cf-125">Remarks</span></span>

<span data-ttu-id="8d6cf-126">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pName* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="8d6cf-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d6cf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d6cf-127">Requirements</span></span>



| <span data-ttu-id="8d6cf-128">需求</span><span class="sxs-lookup"><span data-stu-id="8d6cf-128">Requirement</span></span> | <span data-ttu-id="8d6cf-129">值</span><span class="sxs-lookup"><span data-stu-id="8d6cf-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d6cf-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="8d6cf-130">TAPI version</span></span><br/> | <span data-ttu-id="8d6cf-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8d6cf-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8d6cf-132">標頭</span><span class="sxs-lookup"><span data-stu-id="8d6cf-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8d6cf-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cf-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d6cf-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d6cf-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8d6cf-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cf-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8d6cf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8d6cf-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8d6cf-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d6cf-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d6cf-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d6cf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d6cf-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="8d6cf-139">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="8d6cf-140">**ITSdp：： get \_ Name**</span><span class="sxs-lookup"><span data-stu-id="8d6cf-140">**ITSdp::get\_Name**</span></span>](itsdp-get-name.md)
</dt> </dl>

 

