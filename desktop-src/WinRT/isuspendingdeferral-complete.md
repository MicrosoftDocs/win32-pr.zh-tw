---
description: 通知系統應用程式已儲存其資料，並已準備好暫停。
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'ISuspendingDeferral：： Complete 方法 (ApplicationModel .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970608"
---
# <a name="isuspendingdeferralcomplete-method"></a><span data-ttu-id="21b3a-103">ISuspendingDeferral：： Complete 方法</span><span class="sxs-lookup"><span data-stu-id="21b3a-103">ISuspendingDeferral::Complete method</span></span>

<span data-ttu-id="21b3a-104">通知系統應用程式已儲存其資料，並已準備好暫停。</span><span class="sxs-lookup"><span data-stu-id="21b3a-104">Notifies the system that the app has saved its data and is ready to be suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="21b3a-105">語法</span><span class="sxs-lookup"><span data-stu-id="21b3a-105">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="21b3a-106">參數</span><span class="sxs-lookup"><span data-stu-id="21b3a-106">Parameters</span></span>

<span data-ttu-id="21b3a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="21b3a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21b3a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="21b3a-108">Return value</span></span>

<span data-ttu-id="21b3a-109">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="21b3a-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21b3a-110">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="21b3a-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="21b3a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="21b3a-111">Requirements</span></span>



| <span data-ttu-id="21b3a-112">需求</span><span class="sxs-lookup"><span data-stu-id="21b3a-112">Requirement</span></span> | <span data-ttu-id="21b3a-113">值</span><span class="sxs-lookup"><span data-stu-id="21b3a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b3a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21b3a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="21b3a-115">Windows 8</span><span class="sxs-lookup"><span data-stu-id="21b3a-115">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="21b3a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21b3a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="21b3a-117">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21b3a-117">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="21b3a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="21b3a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="21b3a-119"><dt>ApplicationModel。h</dt></span><span class="sxs-lookup"><span data-stu-id="21b3a-119"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="21b3a-120">Idl</span><span class="sxs-lookup"><span data-stu-id="21b3a-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21b3a-121"><dt>ApplicationModel .idl</dt></span><span class="sxs-lookup"><span data-stu-id="21b3a-121"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b3a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21b3a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b3a-123">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="21b3a-123">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 




