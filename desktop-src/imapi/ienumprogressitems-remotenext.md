---
title: IEnumProgressItems RemoteNext 方法
description: 支援遠端用戶端，該用戶端想要取得列舉順序中指定的專案數。 |IEnumProgressItems RemoteNext 方法
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- RemoteNext 方法 IMAPI.EXE
- RemoteNext 方法 IMAPI.EXE、IEnumProgressItems 介面
- IEnumProgressItems 介面 IMAPI.EXE，RemoteNext 方法
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a088a1be640c6653a8a8ccd8b00cf21bd027ecd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988139"
---
# <a name="ienumprogressitemsremotenext-method"></a><span data-ttu-id="05a5f-107">IEnumProgressItems：： RemoteNext 方法</span><span class="sxs-lookup"><span data-stu-id="05a5f-107">IEnumProgressItems::RemoteNext method</span></span>

<span data-ttu-id="05a5f-108">支援遠端用戶端，該用戶端想要取得列舉順序中指定的專案數</span><span class="sxs-lookup"><span data-stu-id="05a5f-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence</span></span>

## <a name="syntax"></a><span data-ttu-id="05a5f-109">語法</span><span class="sxs-lookup"><span data-stu-id="05a5f-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="05a5f-110">參數</span><span class="sxs-lookup"><span data-stu-id="05a5f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a5f-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05a5f-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05a5f-112">要取出的專案數目。</span><span class="sxs-lookup"><span data-stu-id="05a5f-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="05a5f-113">*rgelt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="05a5f-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05a5f-114">[**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem)介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="05a5f-114">Array of [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) interfaces.</span></span> <span data-ttu-id="05a5f-115">完成時，您必須在 rgelt 中釋放每個介面。</span><span class="sxs-lookup"><span data-stu-id="05a5f-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="05a5f-116">*pceltFetched* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="05a5f-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05a5f-117">在 rgelt 中傳回的元素數目。</span><span class="sxs-lookup"><span data-stu-id="05a5f-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="05a5f-118">如果 *celt* 是一個，您可以將 *PceltFetched* 設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="05a5f-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="05a5f-119">否則，在呼叫這個方法之前，請先將 *pceltFetched* 的值初始化為0。</span><span class="sxs-lookup"><span data-stu-id="05a5f-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a5f-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="05a5f-120">Return value</span></span>

<span data-ttu-id="05a5f-121">\_當 (*celt*) 的要求元素數目成功傳回，或 (*pceltFetched*) 的傳回專案數目小於要求的元素數目時，就會傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="05a5f-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="05a5f-122">可能會因為執行結果而傳回其他成功碼。</span><span class="sxs-lookup"><span data-stu-id="05a5f-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="05a5f-123">下列錯誤碼通常會在作業失敗時傳回，但不代表唯一可能的錯誤值：</span><span class="sxs-lookup"><span data-stu-id="05a5f-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="05a5f-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="05a5f-124">Return code</span></span>                                                                                   | <span data-ttu-id="05a5f-125">Description</span><span class="sxs-lookup"><span data-stu-id="05a5f-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05a5f-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="05a5f-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="05a5f-127">指標無效。</span><span class="sxs-lookup"><span data-stu-id="05a5f-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="05a5f-128">值：且顯示0x80004003</span><span class="sxs-lookup"><span data-stu-id="05a5f-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="05a5f-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="05a5f-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="05a5f-130">無法配置所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="05a5f-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="05a5f-131">值：0x8007000E</span><span class="sxs-lookup"><span data-stu-id="05a5f-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="05a5f-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="05a5f-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="05a5f-133">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="05a5f-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="05a5f-134">值：0x80070057</span><span class="sxs-lookup"><span data-stu-id="05a5f-134">Value: 0x80070057</span></span><br/>    |
| <dl> <span data-ttu-id="05a5f-135"><dt>**E \_未預期**</dt></span><span class="sxs-lookup"><span data-stu-id="05a5f-135"><dt> **E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="05a5f-136">發生未預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="05a5f-136">An unexpected failure occurred.</span></span><br/> <span data-ttu-id="05a5f-137">值：0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="05a5f-137">Value: 0x8000FFFF</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="05a5f-138">備註</span><span class="sxs-lookup"><span data-stu-id="05a5f-138">Remarks</span></span>

<span data-ttu-id="05a5f-139">如果序列中剩餘的元素數目少於所要求的數目，則會抓取剩餘的元素。</span><span class="sxs-lookup"><span data-stu-id="05a5f-139">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="05a5f-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="05a5f-140">Requirements</span></span>



| <span data-ttu-id="05a5f-141">需求</span><span class="sxs-lookup"><span data-stu-id="05a5f-141">Requirement</span></span> | <span data-ttu-id="05a5f-142">值</span><span class="sxs-lookup"><span data-stu-id="05a5f-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05a5f-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05a5f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="05a5f-144">Windows Vista、Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05a5f-144">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="05a5f-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05a5f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="05a5f-146">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05a5f-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05a5f-147">Idl</span><span class="sxs-lookup"><span data-stu-id="05a5f-147">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05a5f-148"><dt>Imapi2fs .idl</dt></span><span class="sxs-lookup"><span data-stu-id="05a5f-148"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a5f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05a5f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a5f-150">**IEnumProgressItems**</span><span class="sxs-lookup"><span data-stu-id="05a5f-150">**IEnumProgressItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[<span data-ttu-id="05a5f-151">IEnumProgressItems：： Next</span><span class="sxs-lookup"><span data-stu-id="05a5f-151">IEnumProgressItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





