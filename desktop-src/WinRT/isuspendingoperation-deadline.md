---
description: 取得延遲的應用程式暫停作業繼續之前剩餘的時間。
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: 'ISuspendingOperation：:D eadline 屬性 (ApplicationModel .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943431"
---
# <a name="isuspendingoperationdeadline-property"></a><span data-ttu-id="1233d-103">ISuspendingOperation：:D eadline 屬性</span><span class="sxs-lookup"><span data-stu-id="1233d-103">ISuspendingOperation::Deadline property</span></span>

<span data-ttu-id="1233d-104">取得延遲的應用程式暫停作業繼續之前剩餘的時間。</span><span class="sxs-lookup"><span data-stu-id="1233d-104">Gets the time remaining before a delayed app suspending operation continues.</span></span>

<span data-ttu-id="1233d-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1233d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1233d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1233d-106">Syntax</span></span>


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a><span data-ttu-id="1233d-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="1233d-107">Property value</span></span>

<span data-ttu-id="1233d-108">延遲的應用程式暫停操作之前的剩餘時間。</span><span class="sxs-lookup"><span data-stu-id="1233d-108">The time remaining before a delayed app suspending operation continues.</span></span>

## <a name="requirements"></a><span data-ttu-id="1233d-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="1233d-109">Requirements</span></span>



| <span data-ttu-id="1233d-110">需求</span><span class="sxs-lookup"><span data-stu-id="1233d-110">Requirement</span></span> | <span data-ttu-id="1233d-111">值</span><span class="sxs-lookup"><span data-stu-id="1233d-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1233d-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1233d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1233d-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1233d-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1233d-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1233d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1233d-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1233d-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1233d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="1233d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1233d-117"><dt>ApplicationModel。h</dt></span><span class="sxs-lookup"><span data-stu-id="1233d-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="1233d-118">Idl</span><span class="sxs-lookup"><span data-stu-id="1233d-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1233d-119"><dt>ApplicationModel .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1233d-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1233d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1233d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1233d-121">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="1233d-121">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




