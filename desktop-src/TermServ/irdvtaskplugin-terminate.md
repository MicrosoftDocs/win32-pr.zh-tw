---
title: IRDVTaskPlugin Terminate 方法
description: 在工作代理程式關閉時呼叫。
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Terminate 方法遠端桌面服務
- Terminate 方法遠端桌面服務，IRDVTaskPlugin 介面
- IRDVTaskPlugin 介面遠端桌面服務，Terminate 方法
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384873"
---
# <a name="irdvtaskpluginterminate-method"></a><span data-ttu-id="35fca-106">IRDVTaskPlugin：： Terminate 方法</span><span class="sxs-lookup"><span data-stu-id="35fca-106">IRDVTaskPlugin::Terminate method</span></span>

<span data-ttu-id="35fca-107">在工作代理程式關閉時呼叫。</span><span class="sxs-lookup"><span data-stu-id="35fca-107">Called when the task agent is being shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fca-108">語法</span><span class="sxs-lookup"><span data-stu-id="35fca-108">Syntax</span></span>


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="35fca-109">參數</span><span class="sxs-lookup"><span data-stu-id="35fca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fca-110">*hr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35fca-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35fca-111">指出關機是否因為正常關機或失敗。</span><span class="sxs-lookup"><span data-stu-id="35fca-111">Indicates whether the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="35fca-112">如果關機正常，則會包含 **\_ [確定]**。</span><span class="sxs-lookup"><span data-stu-id="35fca-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="35fca-113">否則，它會包含 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="35fca-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fca-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="35fca-114">Return value</span></span>

<span data-ttu-id="35fca-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="35fca-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35fca-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="35fca-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fca-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="35fca-117">Requirements</span></span>



| <span data-ttu-id="35fca-118">需求</span><span class="sxs-lookup"><span data-stu-id="35fca-118">Requirement</span></span> | <span data-ttu-id="35fca-119">值</span><span class="sxs-lookup"><span data-stu-id="35fca-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="35fca-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35fca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35fca-121">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="35fca-121">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="35fca-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35fca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35fca-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35fca-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35fca-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35fca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fca-125">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="35fca-125">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





