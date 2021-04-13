---
title: 'IRDVTaskPluginNotifySink OnTerminated 方法 (Sbtsv .h) '
description: 由工作代理程式呼叫，以要求關閉工作代理程式。
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- OnTerminated 方法遠端桌面服務
- OnTerminated 方法遠端桌面服務，IRDVTaskPluginNotifySink 介面
- IRDVTaskPluginNotifySink 介面遠端桌面服務，OnTerminated 方法
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509347"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a><span data-ttu-id="dbab3-106">IRDVTaskPluginNotifySink：： OnTerminated 方法</span><span class="sxs-lookup"><span data-stu-id="dbab3-106">IRDVTaskPluginNotifySink::OnTerminated method</span></span>

<span data-ttu-id="dbab3-107">由工作代理程式呼叫，以要求關閉工作代理程式。</span><span class="sxs-lookup"><span data-stu-id="dbab3-107">Called by the task agent to request that the task agent be shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbab3-108">語法</span><span class="sxs-lookup"><span data-stu-id="dbab3-108">Syntax</span></span>


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="dbab3-109">參數</span><span class="sxs-lookup"><span data-stu-id="dbab3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbab3-110">*hr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dbab3-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbab3-111">指出關機是否因為正常關機或失敗。</span><span class="sxs-lookup"><span data-stu-id="dbab3-111">Indicates if the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="dbab3-112">如果關機正常，則會包含 **\_ [確定]**。</span><span class="sxs-lookup"><span data-stu-id="dbab3-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="dbab3-113">否則，它會包含 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dbab3-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbab3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbab3-114">Return value</span></span>

<span data-ttu-id="dbab3-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="dbab3-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbab3-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dbab3-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbab3-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbab3-117">Requirements</span></span>



| <span data-ttu-id="dbab3-118">需求</span><span class="sxs-lookup"><span data-stu-id="dbab3-118">Requirement</span></span> | <span data-ttu-id="dbab3-119">值</span><span class="sxs-lookup"><span data-stu-id="dbab3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbab3-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbab3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dbab3-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="dbab3-121">Windows 7 Enterprise</span></span><br/>                                                    |
| <span data-ttu-id="dbab3-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbab3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dbab3-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbab3-123">Windows Server 2008 R2</span></span><br/>                                                  |
| <span data-ttu-id="dbab3-124">標頭</span><span class="sxs-lookup"><span data-stu-id="dbab3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbab3-125"><dt>Sbtsv。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbab3-125"><dt>Sbtsv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbab3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbab3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbab3-127">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="dbab3-127">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





