---
description: Clone 方法會建立另一個列舉值，其中包含與目前相同的列舉狀態。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'IEnumParticipant：： Clone 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001208"
---
# <a name="ienumparticipantclone-method"></a><span data-ttu-id="bcd22-104">IEnumParticipant：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="bcd22-104">IEnumParticipant::Clone method</span></span>

<span data-ttu-id="bcd22-105">\[在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用 **複製**。</span><span class="sxs-lookup"><span data-stu-id="bcd22-105">\[**Clone** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bcd22-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="bcd22-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bcd22-107">**Clone** 方法會建立另一個列舉值，其中包含與目前相同的列舉狀態。</span><span class="sxs-lookup"><span data-stu-id="bcd22-107">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span> <span data-ttu-id="bcd22-108">這種方法在 Visual Basic 和指令碼語言中是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="bcd22-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd22-109">語法</span><span class="sxs-lookup"><span data-stu-id="bcd22-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="bcd22-110">參數</span><span class="sxs-lookup"><span data-stu-id="bcd22-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcd22-111">*ppEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bcd22-111">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcd22-112">新 [**IEnumParticipant**](ienumparticipant.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bcd22-112">Pointer to new [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcd22-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bcd22-113">Return value</span></span>

<span data-ttu-id="bcd22-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bcd22-114">This method can return one of these values.</span></span>



| <span data-ttu-id="bcd22-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bcd22-115">Return code</span></span>                                                                                   | <span data-ttu-id="bcd22-116">Description</span><span class="sxs-lookup"><span data-stu-id="bcd22-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bcd22-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd22-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bcd22-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="bcd22-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bcd22-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd22-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bcd22-120">*PpEnum* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="bcd22-120">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="bcd22-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd22-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bcd22-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="bcd22-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bcd22-123"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd22-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="bcd22-124">因不明原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="bcd22-124">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="bcd22-125">備註</span><span class="sxs-lookup"><span data-stu-id="bcd22-125">Remarks</span></span>

<span data-ttu-id="bcd22-126">TAPI 會在 **IEnumParticipant：： Clone** 所傳回的 [**IEnumParticipant**](ienumparticipant.md)介面上呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)方法。</span><span class="sxs-lookup"><span data-stu-id="bcd22-126">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **IEnumParticipant::Clone**.</span></span> <span data-ttu-id="bcd22-127">應用程式必須在 **IEnumParticipant** 介面上呼叫 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="bcd22-127">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd22-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcd22-128">Requirements</span></span>



| <span data-ttu-id="bcd22-129">需求</span><span class="sxs-lookup"><span data-stu-id="bcd22-129">Requirement</span></span> | <span data-ttu-id="bcd22-130">值</span><span class="sxs-lookup"><span data-stu-id="bcd22-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd22-131">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="bcd22-131">TAPI version</span></span><br/> | <span data-ttu-id="bcd22-132">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="bcd22-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bcd22-133">標頭</span><span class="sxs-lookup"><span data-stu-id="bcd22-133">Header</span></span><br/>       | <dl> <span data-ttu-id="bcd22-134"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="bcd22-134"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="bcd22-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="bcd22-135">Library</span></span><br/>      | <dl> <span data-ttu-id="bcd22-136"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="bcd22-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bcd22-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd22-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="bcd22-138"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcd22-138"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bcd22-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcd22-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd22-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="bcd22-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="bcd22-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="bcd22-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

