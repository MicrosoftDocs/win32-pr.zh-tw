---
title: IMsTscAxEvents OnReceivedTSPublicKey 方法
description: 當用戶端從伺服器抓取公開金鑰時，在連接順序中呼叫。 只有當 NotifyTSPublicKey 屬性為 VARIANT TRUE 時，才會呼叫此事件 \_ 。
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- OnReceivedTSPublicKey 方法遠端桌面服務
- OnReceivedTSPublicKey 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnReceivedTSPublicKey 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465785"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a><span data-ttu-id="bfaa0-107">IMsTscAxEvents：： OnReceivedTSPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="bfaa0-107">IMsTscAxEvents::OnReceivedTSPublicKey method</span></span>

<span data-ttu-id="bfaa0-108">當用戶端從伺服器抓取公開金鑰時，在連接順序中呼叫。</span><span class="sxs-lookup"><span data-stu-id="bfaa0-108">Called during the connection sequence when the client retrieves the public key from the server.</span></span> <span data-ttu-id="bfaa0-109">只有當 **NotifyTSPublicKey** 屬性為 **VARIANT \_ TRUE** 時，才會呼叫此事件。</span><span class="sxs-lookup"><span data-stu-id="bfaa0-109">This event is only called if the **NotifyTSPublicKey** property is **VARIANT\_TRUE**.</span></span> <span data-ttu-id="bfaa0-110">這是在 [**OnConnecting**](imstscaxevents-onconnecting.md)之後，但在 [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) 和 [**OnConnected**](imstscaxevents-onconnected.md)之前。</span><span class="sxs-lookup"><span data-stu-id="bfaa0-110">This is after [**OnConnecting**](imstscaxevents-onconnecting.md), but before [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) and [**OnConnected**](imstscaxevents-onconnected.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfaa0-111">語法</span><span class="sxs-lookup"><span data-stu-id="bfaa0-111">Syntax</span></span>


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a><span data-ttu-id="bfaa0-112">參數</span><span class="sxs-lookup"><span data-stu-id="bfaa0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfaa0-113">*publicKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfaa0-113">*publicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfaa0-114">包含遠端電腦的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="bfaa0-114">Contains the public key of the remote machine.</span></span>

</dd> <dt>

<span data-ttu-id="bfaa0-115">*pfContinueLogon* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bfaa0-115">*pfContinueLogon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfaa0-116">**VARIANT \_ BOOL** 變數的指標，此變數會接收登入進程是否應繼續。</span><span class="sxs-lookup"><span data-stu-id="bfaa0-116">A pointer to a **VARIANT\_BOOL** variable that receives whether the logon process should continue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfaa0-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfaa0-117">Return value</span></span>

<span data-ttu-id="bfaa0-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bfaa0-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfaa0-119">備註</span><span class="sxs-lookup"><span data-stu-id="bfaa0-119">Remarks</span></span>

<span data-ttu-id="bfaa0-120">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="bfaa0-120">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfaa0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfaa0-121">Requirements</span></span>



| <span data-ttu-id="bfaa0-122">需求</span><span class="sxs-lookup"><span data-stu-id="bfaa0-122">Requirement</span></span> | <span data-ttu-id="bfaa0-123">值</span><span class="sxs-lookup"><span data-stu-id="bfaa0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfaa0-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfaa0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bfaa0-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfaa0-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bfaa0-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfaa0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bfaa0-127">Windows Server 2008、Windows Server 2008 SP1</span><span class="sxs-lookup"><span data-stu-id="bfaa0-127">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="bfaa0-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bfaa0-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfaa0-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfaa0-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfaa0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bfaa0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfaa0-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfaa0-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfaa0-132">IID</span><span class="sxs-lookup"><span data-stu-id="bfaa0-132">IID</span></span><br/>                      | <span data-ttu-id="bfaa0-133">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="bfaa0-133">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bfaa0-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfaa0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfaa0-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="bfaa0-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





