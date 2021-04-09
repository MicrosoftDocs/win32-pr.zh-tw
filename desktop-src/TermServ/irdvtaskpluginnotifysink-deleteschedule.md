---
title: IRDVTaskPluginNotifySink DeleteSchedule 方法
description: 由工作代理程式呼叫以刪除已排程的工作。
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- DeleteSchedule 方法遠端桌面服務
- DeleteSchedule 方法遠端桌面服務，IRDVTaskPluginNotifySink 介面
- IRDVTaskPluginNotifySink 介面遠端桌面服務，DeleteSchedule 方法
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106169"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a><span data-ttu-id="53605-106">IRDVTaskPluginNotifySink：:D eleteSchedule 方法</span><span class="sxs-lookup"><span data-stu-id="53605-106">IRDVTaskPluginNotifySink::DeleteSchedule method</span></span>

<span data-ttu-id="53605-107">由工作代理程式呼叫以刪除已排程的工作。</span><span class="sxs-lookup"><span data-stu-id="53605-107">Called by the task agent to delete a scheduled task.</span></span>

## <a name="syntax"></a><span data-ttu-id="53605-108">語法</span><span class="sxs-lookup"><span data-stu-id="53605-108">Syntax</span></span>


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a><span data-ttu-id="53605-109">參數</span><span class="sxs-lookup"><span data-stu-id="53605-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53605-110">*bstrIdentifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53605-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53605-111">排程工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="53605-111">The identifier of the scheduled task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53605-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="53605-112">Return value</span></span>

<span data-ttu-id="53605-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="53605-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53605-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53605-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53605-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="53605-115">Requirements</span></span>



| <span data-ttu-id="53605-116">需求</span><span class="sxs-lookup"><span data-stu-id="53605-116">Requirement</span></span> | <span data-ttu-id="53605-117">值</span><span class="sxs-lookup"><span data-stu-id="53605-117">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="53605-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53605-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53605-119">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="53605-119">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="53605-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53605-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53605-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53605-121">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53605-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53605-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53605-123">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="53605-123">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





