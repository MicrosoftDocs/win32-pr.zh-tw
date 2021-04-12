---
description: 抓取目前視窗的功能表控制碼。
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: 'MN_GETHMENU 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192823"
---
# <a name="mn_gethmenu-message"></a><span data-ttu-id="58e7d-103">MN \_ GETHMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="58e7d-103">MN\_GETHMENU message</span></span>

<span data-ttu-id="58e7d-104">抓取目前視窗的功能表控制碼。</span><span class="sxs-lookup"><span data-stu-id="58e7d-104">Retrieves the menu handle for the current window.</span></span>


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a><span data-ttu-id="58e7d-105">參數</span><span class="sxs-lookup"><span data-stu-id="58e7d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e7d-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58e7d-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58e7d-107">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="58e7d-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58e7d-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58e7d-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58e7d-109">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="58e7d-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e7d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="58e7d-110">Return value</span></span>

<span data-ttu-id="58e7d-111">類型： **HMENU**</span><span class="sxs-lookup"><span data-stu-id="58e7d-111">Type: **HMENU**</span></span>

<span data-ttu-id="58e7d-112">如果成功，則傳回值是目前視窗的 **HMENU** 。</span><span class="sxs-lookup"><span data-stu-id="58e7d-112">If successful, the return value is the **HMENU** for the current window.</span></span> <span data-ttu-id="58e7d-113">如果失敗，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="58e7d-113">If it fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e7d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="58e7d-114">Requirements</span></span>



| <span data-ttu-id="58e7d-115">需求</span><span class="sxs-lookup"><span data-stu-id="58e7d-115">Requirement</span></span> | <span data-ttu-id="58e7d-116">值</span><span class="sxs-lookup"><span data-stu-id="58e7d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e7d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58e7d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58e7d-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58e7d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="58e7d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58e7d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58e7d-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58e7d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58e7d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="58e7d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e7d-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="58e7d-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 




