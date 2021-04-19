---
description: 分派傳入的已傳送訊息、檢查已張貼訊息的執行緒訊息佇列，以及抓取訊息 (如果有任何) 存在的話。
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000703"
---
# <a name="_peekmessage-function"></a><span data-ttu-id="fd98c-103">\_PeekMessage 函式</span><span class="sxs-lookup"><span data-stu-id="fd98c-103">\_PeekMessage function</span></span>

<span data-ttu-id="fd98c-104">\[此函式是 **PeekMessage** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="fd98c-104">\[This function is a wrapper over the **PeekMessage** function.</span></span> <span data-ttu-id="fd98c-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="fd98c-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="fd98c-106">應用程式應該直接呼叫 **PeekMessage** 。\]</span><span class="sxs-lookup"><span data-stu-id="fd98c-106">Applications should call **PeekMessage** directly.\]</span></span>

<span data-ttu-id="fd98c-107">分派傳入的已傳送訊息、檢查已張貼訊息的執行緒訊息佇列，以及抓取訊息 (如果有任何) 存在的話。</span><span class="sxs-lookup"><span data-stu-id="fd98c-107">Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).</span></span> <span data-ttu-id="fd98c-108">請參閱 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)。</span><span class="sxs-lookup"><span data-stu-id="fd98c-108">See [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd98c-109">語法</span><span class="sxs-lookup"><span data-stu-id="fd98c-109">Syntax</span></span>


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="fd98c-110">參數</span><span class="sxs-lookup"><span data-stu-id="fd98c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd98c-111">*...*</span><span class="sxs-lookup"><span data-stu-id="fd98c-111">*...*</span></span> 
<span data-ttu-id="fd98c-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fd98c-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fd98c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd98c-113">Requirements</span></span>



| <span data-ttu-id="fd98c-114">需求</span><span class="sxs-lookup"><span data-stu-id="fd98c-114">Requirement</span></span> | <span data-ttu-id="fd98c-115">值</span><span class="sxs-lookup"><span data-stu-id="fd98c-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd98c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="fd98c-116">DLL</span></span><br/> | <dl> <span data-ttu-id="fd98c-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd98c-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd98c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd98c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd98c-119">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="fd98c-119">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
