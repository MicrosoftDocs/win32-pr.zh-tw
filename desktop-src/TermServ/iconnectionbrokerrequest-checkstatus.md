---
title: 'IConnectionBrokerRequest CheckStatus 方法 (Cbclient .h) '
description: 呼叫以判斷非同步要求的狀態。
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- CheckStatus 方法遠端桌面服務
- CheckStatus 方法遠端桌面服務，IConnectionBrokerRequest 介面
- IConnectionBrokerRequest 介面遠端桌面服務，CheckStatus 方法
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385178"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a><span data-ttu-id="b3dda-106">IConnectionBrokerRequest：： CheckStatus 方法</span><span class="sxs-lookup"><span data-stu-id="b3dda-106">IConnectionBrokerRequest::CheckStatus method</span></span>

<span data-ttu-id="b3dda-107">呼叫以判斷非同步要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="b3dda-107">Called to determine the status of an asynchronous request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3dda-108">語法</span><span class="sxs-lookup"><span data-stu-id="b3dda-108">Syntax</span></span>


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a><span data-ttu-id="b3dda-109">參數</span><span class="sxs-lookup"><span data-stu-id="b3dda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3dda-110">*pReqStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b3dda-110">*pReqStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3dda-111">變數的位址，此變數會接收 [**CB \_ 要求 \_ 狀態**](cb-request-status.md) 列舉值，指出要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="b3dda-111">The address of a variable that receives a value of the [**CB\_REQUEST\_STATUS**](cb-request-status.md) enumeration that indicates the status of the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3dda-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3dda-112">Return value</span></span>

<span data-ttu-id="b3dda-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b3dda-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3dda-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b3dda-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3dda-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3dda-115">Requirements</span></span>



| <span data-ttu-id="b3dda-116">需求</span><span class="sxs-lookup"><span data-stu-id="b3dda-116">Requirement</span></span> | <span data-ttu-id="b3dda-117">值</span><span class="sxs-lookup"><span data-stu-id="b3dda-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3dda-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3dda-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b3dda-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b3dda-119">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="b3dda-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3dda-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b3dda-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b3dda-121">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="b3dda-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b3dda-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3dda-123"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3dda-123"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3dda-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3dda-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3dda-125"><dt>Cbclient .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3dda-125"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3dda-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b3dda-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3dda-127"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3dda-127"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3dda-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3dda-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3dda-129">**IConnectionBrokerRequest**</span><span class="sxs-lookup"><span data-stu-id="b3dda-129">**IConnectionBrokerRequest**</span></span>](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





