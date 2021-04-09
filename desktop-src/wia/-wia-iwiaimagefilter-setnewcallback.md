---
description: 針對要用於轉送呼叫的影像處理篩選設定新的應用程式回呼。
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'IWiaImageFilter：： SetNewCallback 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691092"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a><span data-ttu-id="6cc6a-103">IWiaImageFilter：： SetNewCallback 方法</span><span class="sxs-lookup"><span data-stu-id="6cc6a-103">IWiaImageFilter::SetNewCallback method</span></span>

<span data-ttu-id="6cc6a-104">針對要用於轉送呼叫的影像處理篩選設定新的應用程式回呼。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-104">Sets a new application callback for the image processing filter to use for forwarding calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc6a-105">語法</span><span class="sxs-lookup"><span data-stu-id="6cc6a-105">Syntax</span></span>


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="6cc6a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6cc6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc6a-107">*pWiaTransferCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6cc6a-107">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cc6a-108">類型： **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span><span class="sxs-lookup"><span data-stu-id="6cc6a-108">Type: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span></span>

<span data-ttu-id="6cc6a-109">指定應用程式 [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-109">Specifies a pointer to the application's [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc6a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cc6a-110">Return value</span></span>

<span data-ttu-id="6cc6a-111">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6cc6a-111">Type: **HRESULT**</span></span>

<span data-ttu-id="6cc6a-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6cc6a-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cc6a-114">備註</span><span class="sxs-lookup"><span data-stu-id="6cc6a-114">Remarks</span></span>

<span data-ttu-id="6cc6a-115">請勿直接從您的應用程式呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-115">Do not call this method directly from your application.</span></span>

<span data-ttu-id="6cc6a-116">需要有影像處理篩選，才能在設定新的回呼之前釋放先前儲存的應用程式回呼介面。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-116">The image processing filter is required to release the previously stored application callback interface before setting the new callback.</span></span>

<span data-ttu-id="6cc6a-117">如果 *pWiaTransferCallback* 為 **Null**，則影像處理篩選器應該只釋出舊的應用程式回呼，並傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-117">If *pWiaTransferCallback* is **NULL**, the image processing filter should simply release the old application callback and return S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc6a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cc6a-118">Requirements</span></span>



| <span data-ttu-id="6cc6a-119">需求</span><span class="sxs-lookup"><span data-stu-id="6cc6a-119">Requirement</span></span> | <span data-ttu-id="6cc6a-120">值</span><span class="sxs-lookup"><span data-stu-id="6cc6a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc6a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cc6a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc6a-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cc6a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6cc6a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cc6a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc6a-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cc6a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6cc6a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6cc6a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cc6a-126"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="6cc6a-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6cc6a-127">Idl</span><span class="sxs-lookup"><span data-stu-id="6cc6a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cc6a-128"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cc6a-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




