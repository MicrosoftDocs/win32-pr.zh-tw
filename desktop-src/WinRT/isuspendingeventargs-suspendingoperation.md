---
description: 取得應用程式暫停作業。
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'ISuspendingEventArgs：： SuspendingOperation 屬性 (Windows. ApplicationModel .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848038"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a><span data-ttu-id="80f0f-103">ISuspendingEventArgs：： SuspendingOperation 屬性</span><span class="sxs-lookup"><span data-stu-id="80f0f-103">ISuspendingEventArgs::SuspendingOperation property</span></span>

<span data-ttu-id="80f0f-104">取得應用程式暫停作業。</span><span class="sxs-lookup"><span data-stu-id="80f0f-104">Gets the app suspending operation.</span></span>

<span data-ttu-id="80f0f-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="80f0f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="80f0f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="80f0f-106">Syntax</span></span>


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a><span data-ttu-id="80f0f-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="80f0f-107">Property value</span></span>

<span data-ttu-id="80f0f-108">暫止作業。</span><span class="sxs-lookup"><span data-stu-id="80f0f-108">The suspending operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="80f0f-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="80f0f-109">Requirements</span></span>



| <span data-ttu-id="80f0f-110">需求</span><span class="sxs-lookup"><span data-stu-id="80f0f-110">Requirement</span></span> | <span data-ttu-id="80f0f-111">值</span><span class="sxs-lookup"><span data-stu-id="80f0f-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80f0f-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80f0f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="80f0f-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="80f0f-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="80f0f-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80f0f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="80f0f-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80f0f-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="80f0f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="80f0f-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="80f0f-117"><dt>ApplicationModel。h</dt></span><span class="sxs-lookup"><span data-stu-id="80f0f-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="80f0f-118">Idl</span><span class="sxs-lookup"><span data-stu-id="80f0f-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80f0f-119"><dt>ApplicationModel .idl</dt></span><span class="sxs-lookup"><span data-stu-id="80f0f-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80f0f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80f0f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80f0f-121">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="80f0f-121">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 




