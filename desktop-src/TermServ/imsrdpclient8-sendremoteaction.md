---
title: IMsRdpClient8 SendRemoteAction 方法
description: 使動作在遠端會話中執行。
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- SendRemoteAction 方法遠端桌面服務
- SendRemoteAction 方法遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，SendRemoteAction 方法
- SendRemoteAction 方法遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，SendRemoteAction 方法
- SendRemoteAction 方法遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，SendRemoteAction 方法
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28fc9695686402e0a8e98ed17fc1bc6a47939d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467032"
---
# <a name="imsrdpclient8sendremoteaction-method"></a><span data-ttu-id="0f35d-110">IMsRdpClient8：： SendRemoteAction 方法</span><span class="sxs-lookup"><span data-stu-id="0f35d-110">IMsRdpClient8::SendRemoteAction method</span></span>

<span data-ttu-id="0f35d-111">使動作在遠端會話中執行。</span><span class="sxs-lookup"><span data-stu-id="0f35d-111">Causes an action to be performed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f35d-112">語法</span><span class="sxs-lookup"><span data-stu-id="0f35d-112">Syntax</span></span>


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a><span data-ttu-id="0f35d-113">參數</span><span class="sxs-lookup"><span data-stu-id="0f35d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f35d-114">*actionType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f35d-114">*actionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f35d-115">[**RemoteSessionActionType**](remotesessionactiontype.md)列舉的值，指定要傳送至遠端會話的動作。</span><span class="sxs-lookup"><span data-stu-id="0f35d-115">A value of the [**RemoteSessionActionType**](remotesessionactiontype.md) enumeration that specifies the action to send to the remote session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f35d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f35d-116">Return value</span></span>

<span data-ttu-id="0f35d-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0f35d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f35d-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0f35d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f35d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f35d-119">Requirements</span></span>



| <span data-ttu-id="0f35d-120">需求</span><span class="sxs-lookup"><span data-stu-id="0f35d-120">Requirement</span></span> | <span data-ttu-id="0f35d-121">值</span><span class="sxs-lookup"><span data-stu-id="0f35d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f35d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f35d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0f35d-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f35d-123">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="0f35d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f35d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0f35d-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f35d-125">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="0f35d-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0f35d-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f35d-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f35d-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f35d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0f35d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f35d-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f35d-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f35d-130">IID</span><span class="sxs-lookup"><span data-stu-id="0f35d-130">IID</span></span><br/>                      | <span data-ttu-id="0f35d-131">IID \_ IMsRdpClient8 定義為4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="0f35d-131">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0f35d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f35d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f35d-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0f35d-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0f35d-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0f35d-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0f35d-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="0f35d-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





