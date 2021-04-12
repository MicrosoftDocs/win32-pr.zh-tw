---
title: IRDVTaskPlugin Initialize 方法
description: 呼叫以初始化工作代理程式。
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Initialize 方法遠端桌面服務
- Initialize 方法遠端桌面服務，IRDVTaskPlugin 介面
- IRDVTaskPlugin 介面遠端桌面服務，Initialize 方法
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384157"
---
# <a name="irdvtaskplugininitialize-method"></a><span data-ttu-id="d6f51-106">IRDVTaskPlugin：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="d6f51-106">IRDVTaskPlugin::Initialize method</span></span>

<span data-ttu-id="d6f51-107">呼叫以初始化工作代理程式。</span><span class="sxs-lookup"><span data-stu-id="d6f51-107">Called to initialize the task agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f51-108">語法</span><span class="sxs-lookup"><span data-stu-id="d6f51-108">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a><span data-ttu-id="d6f51-109">參數</span><span class="sxs-lookup"><span data-stu-id="d6f51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f51-110">*pNotifySink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6f51-110">*pNotifySink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f51-111">類型： \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d6f51-111">Type: \**[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\** _</span></span>

<span data-ttu-id="d6f51-112">[_ *IRDVTaskPluginNotifySink* \*](irdvtaskpluginnotifysink.md)介面的指標，工作代理程式會使用此介面與觸發程式代理程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="d6f51-112">A pointer to an [_ *IRDVTaskPluginNotifySink*\*](irdvtaskpluginnotifysink.md) interface that the task agent uses to communicate with the trigger agent.</span></span> <span data-ttu-id="d6f51-113">如果不再需要此介面，您必須釋放這個介面。</span><span class="sxs-lookup"><span data-stu-id="d6f51-113">You must release this interface when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6f51-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6f51-114">Return value</span></span>

<span data-ttu-id="d6f51-115">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6f51-115">Type: **HRESULT**</span></span>

<span data-ttu-id="d6f51-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d6f51-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6f51-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6f51-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f51-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6f51-118">Requirements</span></span>



| <span data-ttu-id="d6f51-119">需求</span><span class="sxs-lookup"><span data-stu-id="d6f51-119">Requirement</span></span> | <span data-ttu-id="d6f51-120">值</span><span class="sxs-lookup"><span data-stu-id="d6f51-120">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="d6f51-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6f51-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f51-122">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="d6f51-122">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="d6f51-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6f51-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f51-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d6f51-124">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6f51-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6f51-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f51-126">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="d6f51-126">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





