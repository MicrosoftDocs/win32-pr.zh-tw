---
description: 啟用工作完成。
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: TaskCompletionClient 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194428"
---
# <a name="taskcompletionclient-interface"></a><span data-ttu-id="67975-103">TaskCompletionClient 介面</span><span class="sxs-lookup"><span data-stu-id="67975-103">TaskCompletionClient interface</span></span>

<span data-ttu-id="67975-104">啟用工作完成。</span><span class="sxs-lookup"><span data-stu-id="67975-104">Enables task completion.</span></span>

## <a name="members"></a><span data-ttu-id="67975-105">成員</span><span class="sxs-lookup"><span data-stu-id="67975-105">Members</span></span>

<span data-ttu-id="67975-106">**TaskCompletionClient** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="67975-106">The **TaskCompletionClient** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="67975-107">**TaskCompletionClient** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="67975-107">**TaskCompletionClient** also has these types of members:</span></span>

-   [<span data-ttu-id="67975-108">方法</span><span class="sxs-lookup"><span data-stu-id="67975-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="67975-109">方法</span><span class="sxs-lookup"><span data-stu-id="67975-109">Methods</span></span>

<span data-ttu-id="67975-110">**TaskCompletionClient** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="67975-110">The **TaskCompletionClient** interface has these methods.</span></span>



| <span data-ttu-id="67975-111">方法</span><span class="sxs-lookup"><span data-stu-id="67975-111">Method</span></span>                                                                    | <span data-ttu-id="67975-112">描述</span><span class="sxs-lookup"><span data-stu-id="67975-112">Description</span></span>                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [<span data-ttu-id="67975-113">**ApplyTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="67975-113">**ApplyTaskCompletion**</span></span>](taskcompletionclient-applytaskcompletion.md)   | <span data-ttu-id="67975-114">開始工作完成。</span><span class="sxs-lookup"><span data-stu-id="67975-114">Begins the task completion.</span></span><br/> |
| [<span data-ttu-id="67975-115">**RevokeTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="67975-115">**RevokeTaskCompletion**</span></span>](taskcompletionclient-revoketaskcompletion.md) | <span data-ttu-id="67975-116">結束工作完成。</span><span class="sxs-lookup"><span data-stu-id="67975-116">Ends the task completion.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="67975-117">備註</span><span class="sxs-lookup"><span data-stu-id="67975-117">Remarks</span></span>

<span data-ttu-id="67975-118">此介面的 GUID 為 "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96"。</span><span class="sxs-lookup"><span data-stu-id="67975-118">The GUID for this interface is "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span></span>

<span data-ttu-id="67975-119">此 API 已被取代，在未來的 Windows 版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="67975-119">This API is deprecated and may not be available in future versions of Windows.</span></span> <span data-ttu-id="67975-120">應用程式應該改為使用 [**ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) 命名空間中的 api。</span><span class="sxs-lookup"><span data-stu-id="67975-120">Apps should use the APIs in the [**Windows.ApplicationModel.ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) namespace instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="67975-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="67975-121">Requirements</span></span>



| <span data-ttu-id="67975-122">需求</span><span class="sxs-lookup"><span data-stu-id="67975-122">Requirement</span></span> | <span data-ttu-id="67975-123">值</span><span class="sxs-lookup"><span data-stu-id="67975-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67975-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67975-124">Minimum supported client</span></span><br/> | <span data-ttu-id="67975-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67975-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67975-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67975-126">Minimum supported server</span></span><br/> | <span data-ttu-id="67975-127">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67975-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="67975-128">DLL</span><span class="sxs-lookup"><span data-stu-id="67975-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67975-129"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67975-129"><dt>ExecModelClient.dll</dt></span></span> </dl> |



 

 
