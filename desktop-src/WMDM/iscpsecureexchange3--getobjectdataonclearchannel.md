---
title: GetObjectDataOnClearChannel 方法
description: GetObjectDataOnClearChannel 方法會將清除通道上的物件資料區區塊轉送回 Windows Media 裝置管理員。
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- GetObjectDataOnClearChannel 方法 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000655"
---
# <a name="getobjectdataonclearchannel-method"></a><span data-ttu-id="7512a-104">GetObjectDataOnClearChannel 方法</span><span class="sxs-lookup"><span data-stu-id="7512a-104">GetObjectDataOnClearChannel method</span></span>

<span data-ttu-id="7512a-105">**GetObjectDataOnClearChannel** 方法會將清除通道上的物件資料區區塊轉送回 Windows Media 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="7512a-105">The **GetObjectDataOnClearChannel** method transfers a block of object data on a clear channel back to Windows Media Device Manager.</span></span>

<span data-ttu-id="7512a-106">此方法與 [**ISCPSecureExchange：： ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) 相同，不同之處在于這個方法所傳回的資料並未加密。</span><span class="sxs-lookup"><span data-stu-id="7512a-106">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="7512a-107">因此，這個方法更有效率。</span><span class="sxs-lookup"><span data-stu-id="7512a-107">Consequently this method is more efficient.</span></span>

## <a name="syntax"></a><span data-ttu-id="7512a-108">語法</span><span class="sxs-lookup"><span data-stu-id="7512a-108">Syntax</span></span>


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="7512a-109">參數</span><span class="sxs-lookup"><span data-stu-id="7512a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7512a-110">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="7512a-110">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7512a-111">裝置物件的指標。</span><span class="sxs-lookup"><span data-stu-id="7512a-111">Pointer to the device object.</span></span>

</dd> <dt>

<span data-ttu-id="7512a-112">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="7512a-112">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="7512a-113">用來接收資料的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="7512a-113">Pointer to a buffer to receive data.</span></span>

</dd> <dt>

<span data-ttu-id="7512a-114">*pdwSize*</span><span class="sxs-lookup"><span data-stu-id="7512a-114">*pdwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="7512a-115">包含傳輸大小的 **DWORD** 指標。</span><span class="sxs-lookup"><span data-stu-id="7512a-115">Pointer to a **DWORD** containing the transfer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7512a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="7512a-116">Return value</span></span>

<span data-ttu-id="7512a-117">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7512a-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="7512a-118">如果方法失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7512a-118">If the method fails, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="7512a-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7512a-119">Return code</span></span>                                                                                                | <span data-ttu-id="7512a-120">Description</span><span class="sxs-lookup"><span data-stu-id="7512a-120">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7512a-121"><dt>**WMDM \_ E \_ MAC \_ 檢查 \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="7512a-121"><dt>**WMDM\_E\_MAC\_CHECK\_FAILED**</dt></span></span> </dl> | <span data-ttu-id="7512a-122">訊息驗證碼無效。</span><span class="sxs-lookup"><span data-stu-id="7512a-122">The message authentication code is not valid.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7512a-123"><dt>**WMDM \_ E \_ NORIGHTS**</dt></span><span class="sxs-lookup"><span data-stu-id="7512a-123"><dt>**WMDM\_E\_NORIGHTS**</dt></span></span> </dl>           | <span data-ttu-id="7512a-124">呼叫端沒有執行要求的作業所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="7512a-124">The caller does not have the rights required to perform the requested operation.</span></span><br/> |
| <dl> <span data-ttu-id="7512a-125"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="7512a-125"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="7512a-126">方法失敗。</span><span class="sxs-lookup"><span data-stu-id="7512a-126">The method failed.</span></span> <span data-ttu-id="7512a-127">終止與內容提供者的互動。</span><span class="sxs-lookup"><span data-stu-id="7512a-127">Terminate interaction with the content provider.</span></span><br/>              |
| <dl> <span data-ttu-id="7512a-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7512a-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="7512a-129">參數是無效或 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="7512a-129">A parameter is an invalid or **NULL** pointer.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7512a-130"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="7512a-130"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="7512a-131">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7512a-131">An unspecified error occurred.</span></span><br/>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="7512a-132">備註</span><span class="sxs-lookup"><span data-stu-id="7512a-132">Remarks</span></span>

<span data-ttu-id="7512a-133">為了傳送資料，Windows Media 裝置管理員會呼叫 [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) 方法來取得容器資料。</span><span class="sxs-lookup"><span data-stu-id="7512a-133">To transfer data, Windows Media Device Manager calls the [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) method to obtain the container data.</span></span> <span data-ttu-id="7512a-134">接著會呼叫 **GetObjectDataOnClearChannel** ，將物件資料的區塊從內容提供者傳送至 Windows Media 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="7512a-134">**GetObjectDataOnClearChannel** is then called to transfer blocks of object data from the content provider to Windows Media Device Manager.</span></span> <span data-ttu-id="7512a-135">如果 \_ *pdwSize* 設定為零，則會傳回 S OK，Windows Media 裝置管理員將不會要求進一步的資料。</span><span class="sxs-lookup"><span data-stu-id="7512a-135">If S\_OK is returned with *pdwSize* set to zero, Windows Media Device Manager will request no further data.</span></span>

<span data-ttu-id="7512a-136">此方法與 [**ISCPSecureExchange：： ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) 相同，不同之處在于這個方法所傳回的資料並未加密。</span><span class="sxs-lookup"><span data-stu-id="7512a-136">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="7512a-137">因此，這個方法更有效率。</span><span class="sxs-lookup"><span data-stu-id="7512a-137">Consequently this method is more efficient.</span></span>

## <a name="requirements"></a><span data-ttu-id="7512a-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="7512a-138">Requirements</span></span>



| <span data-ttu-id="7512a-139">需求</span><span class="sxs-lookup"><span data-stu-id="7512a-139">Requirement</span></span> | <span data-ttu-id="7512a-140">值</span><span class="sxs-lookup"><span data-stu-id="7512a-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7512a-141">標頭</span><span class="sxs-lookup"><span data-stu-id="7512a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="7512a-142"><dt>WMSCP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7512a-142"><dt>WMSCP.idl</dt></span></span> </dl>    |
| <span data-ttu-id="7512a-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="7512a-143">Library</span></span><br/> | <dl> <span data-ttu-id="7512a-144"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7512a-144"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7512a-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7512a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7512a-146">**ISCPSecureExchange：： ObjectData**</span><span class="sxs-lookup"><span data-stu-id="7512a-146">**ISCPSecureExchange::ObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[<span data-ttu-id="7512a-147">**ISCPSecureExchange3 介面**</span><span class="sxs-lookup"><span data-stu-id="7512a-147">**ISCPSecureExchange3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





