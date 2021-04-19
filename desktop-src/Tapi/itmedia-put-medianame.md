---
description: Put \_ MediaName 方法會設定媒體名稱。 定義的媒體包括音訊、影片、白板、文字和資料。
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: 'ITMedia：:p ut_MediaName 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dcbd4e29f59694d610fb4e6af9fd49aa53323d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977475"
---
# <a name="itmediaput_medianame-method"></a><span data-ttu-id="3c003-104">ITMedia：:p 的 \_ MediaName 方法</span><span class="sxs-lookup"><span data-stu-id="3c003-104">ITMedia::put\_MediaName method</span></span>

<span data-ttu-id="3c003-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="3c003-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3c003-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="3c003-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3c003-107">**Put \_ MediaName** 方法會設定媒體名稱。</span><span class="sxs-lookup"><span data-stu-id="3c003-107">The **put\_MediaName** method sets the media name.</span></span> <span data-ttu-id="3c003-108">定義的媒體包括音訊、影片、白板、文字和資料。</span><span class="sxs-lookup"><span data-stu-id="3c003-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c003-109">語法</span><span class="sxs-lookup"><span data-stu-id="3c003-109">Syntax</span></span>


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="3c003-110">參數</span><span class="sxs-lookup"><span data-stu-id="3c003-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c003-111">*pMediaName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c003-111">*pMediaName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c003-112">包含要設定之媒體名稱的 **BSTR** 指標。</span><span class="sxs-lookup"><span data-stu-id="3c003-112">Pointer to a **BSTR** containing the media name to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c003-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c003-113">Return value</span></span>

<span data-ttu-id="3c003-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3c003-114">This method can return one of these values.</span></span>



| <span data-ttu-id="3c003-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3c003-115">Return code</span></span>                                                                                   | <span data-ttu-id="3c003-116">Description</span><span class="sxs-lookup"><span data-stu-id="3c003-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3c003-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3c003-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3c003-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="3c003-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3c003-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="3c003-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3c003-120">*PMediaName* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="3c003-120">The *pMediaName* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="3c003-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3c003-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3c003-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="3c003-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3c003-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="3c003-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3c003-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c003-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3c003-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3c003-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3c003-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="3c003-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3c003-127">備註</span><span class="sxs-lookup"><span data-stu-id="3c003-127">Remarks</span></span>

<span data-ttu-id="3c003-128">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pMediaName* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="3c003-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="3c003-129">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="3c003-129">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="3c003-130">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="3c003-130">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c003-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c003-131">Requirements</span></span>



| <span data-ttu-id="3c003-132">需求</span><span class="sxs-lookup"><span data-stu-id="3c003-132">Requirement</span></span> | <span data-ttu-id="3c003-133">值</span><span class="sxs-lookup"><span data-stu-id="3c003-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c003-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="3c003-134">TAPI version</span></span><br/> | <span data-ttu-id="3c003-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3c003-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3c003-136">標頭</span><span class="sxs-lookup"><span data-stu-id="3c003-136">Header</span></span><br/>       | <dl> <span data-ttu-id="3c003-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c003-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c003-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c003-138">Library</span></span><br/>      | <dl> <span data-ttu-id="3c003-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="3c003-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3c003-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3c003-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="3c003-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c003-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c003-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c003-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c003-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="3c003-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="3c003-144">**ITMedia：： get \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="3c003-144">**ITMedia::get\_MediaName**</span></span>](itmedia-get-medianame.md)
</dt> </dl>

 

