---
description: 表示非同步動作完成時所呼叫的方法。
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: AsyncActionCompletedHandler 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973466"
---
# <a name="asyncactioncompletedhandler-interface"></a><span data-ttu-id="0e433-103">AsyncActionCompletedHandler 介面</span><span class="sxs-lookup"><span data-stu-id="0e433-103">AsyncActionCompletedHandler interface</span></span>

<span data-ttu-id="0e433-104">表示非同步動作完成時所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="0e433-104">Represents the method that is called when an asynchronous action completes.</span></span>

## <a name="members"></a><span data-ttu-id="0e433-105">成員</span><span class="sxs-lookup"><span data-stu-id="0e433-105">Members</span></span>

<span data-ttu-id="0e433-106">**AsyncActionCompletedHandler** 介面繼承自 [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)。</span><span class="sxs-lookup"><span data-stu-id="0e433-106">The **AsyncActionCompletedHandler** interface inherits from [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span></span> <span data-ttu-id="0e433-107">**AsyncActionCompletedHandler** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0e433-107">**AsyncActionCompletedHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="0e433-108">方法</span><span class="sxs-lookup"><span data-stu-id="0e433-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0e433-109">方法</span><span class="sxs-lookup"><span data-stu-id="0e433-109">Methods</span></span>

<span data-ttu-id="0e433-110">**AsyncActionCompletedHandler** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0e433-110">The **AsyncActionCompletedHandler** interface has these methods.</span></span>



| <span data-ttu-id="0e433-111">方法</span><span class="sxs-lookup"><span data-stu-id="0e433-111">Method</span></span>                                               | <span data-ttu-id="0e433-112">描述</span><span class="sxs-lookup"><span data-stu-id="0e433-112">Description</span></span>                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e433-113">**調用**</span><span class="sxs-lookup"><span data-stu-id="0e433-113">**Invoke**</span></span>](asyncactioncompletedhandler-invoke.md) | <span data-ttu-id="0e433-114">叫用指定的非同步動作完成時所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="0e433-114">Invokes the method that is called when the specified asynchronous action completes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e433-115">備註</span><span class="sxs-lookup"><span data-stu-id="0e433-115">Remarks</span></span>

<span data-ttu-id="0e433-116">將 **AsyncActionCompletedHandler** 指派給 [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) ，以在非同步動作完成時收到通知。</span><span class="sxs-lookup"><span data-stu-id="0e433-116">Assign an **AsyncActionCompletedHandler** to an [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) to receive a notification when the asynchronous action completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e433-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e433-117">Requirements</span></span>



| <span data-ttu-id="0e433-118">需求</span><span class="sxs-lookup"><span data-stu-id="0e433-118">Requirement</span></span> | <span data-ttu-id="0e433-119">值</span><span class="sxs-lookup"><span data-stu-id="0e433-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e433-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e433-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e433-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0e433-121">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="0e433-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e433-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e433-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e433-123">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="0e433-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0e433-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e433-125"><dt>Windows .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0e433-125"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e433-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e433-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e433-127">**IAsyncInfo**</span><span class="sxs-lookup"><span data-stu-id="0e433-127">**IAsyncInfo**</span></span>](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

