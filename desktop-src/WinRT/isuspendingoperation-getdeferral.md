---
description: 要求應用程式暫停操作延遲。
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'ISuspendingOperation：： GetDeferral 方法 (Windows. ApplicationModel .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848037"
---
# <a name="isuspendingoperationgetdeferral-method"></a><span data-ttu-id="0564e-103">ISuspendingOperation：： GetDeferral 方法</span><span class="sxs-lookup"><span data-stu-id="0564e-103">ISuspendingOperation::GetDeferral method</span></span>

<span data-ttu-id="0564e-104">要求應用程式暫停操作延遲。</span><span class="sxs-lookup"><span data-stu-id="0564e-104">Requests that the app suspending operation be delayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0564e-105">語法</span><span class="sxs-lookup"><span data-stu-id="0564e-105">Syntax</span></span>


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a><span data-ttu-id="0564e-106">參數</span><span class="sxs-lookup"><span data-stu-id="0564e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0564e-107">*延遲* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="0564e-107">*deferral* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0564e-108">延遲暫停。</span><span class="sxs-lookup"><span data-stu-id="0564e-108">The deferral suspension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0564e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0564e-109">Return value</span></span>

<span data-ttu-id="0564e-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0564e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0564e-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0564e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0564e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0564e-112">Requirements</span></span>



| <span data-ttu-id="0564e-113">需求</span><span class="sxs-lookup"><span data-stu-id="0564e-113">Requirement</span></span> | <span data-ttu-id="0564e-114">值</span><span class="sxs-lookup"><span data-stu-id="0564e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0564e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0564e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0564e-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0564e-116">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0564e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0564e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0564e-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0564e-118">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0564e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0564e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0564e-120"><dt>ApplicationModel。h</dt></span><span class="sxs-lookup"><span data-stu-id="0564e-120"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="0564e-121">Idl</span><span class="sxs-lookup"><span data-stu-id="0564e-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0564e-122"><dt>ApplicationModel .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0564e-122"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0564e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0564e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0564e-124">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="0564e-124">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




