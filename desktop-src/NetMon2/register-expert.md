---
description: 專家必須實行註冊專家功能。 網路監視器會呼叫註冊專家功能來取得專家的相關資訊。
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: '將專家回呼函式註冊 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848763"
---
# <a name="register-expert-callback-function"></a><span data-ttu-id="1eae2-104">註冊專家回呼函數</span><span class="sxs-lookup"><span data-stu-id="1eae2-104">Register Expert callback function</span></span>

<span data-ttu-id="1eae2-105">專家必須實行 **註冊** 專家功能。</span><span class="sxs-lookup"><span data-stu-id="1eae2-105">The expert must implement the **Register** expert function.</span></span> <span data-ttu-id="1eae2-106">網路監視器會呼叫 **註冊** 專家功能來取得專家的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1eae2-106">Network Monitor calls the **Register** expert function to obtain information about the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eae2-107">語法</span><span class="sxs-lookup"><span data-stu-id="1eae2-107">Syntax</span></span>


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1eae2-108">參數</span><span class="sxs-lookup"><span data-stu-id="1eae2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eae2-109">*pExpertInfo* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1eae2-109">*pExpertInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eae2-110">網路監視器配置之 [**EXPERTENUMINFO**](expertenuminfo.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1eae2-110">Pointer to an [**EXPERTENUMINFO**](expertenuminfo.md) structure that Network Monitor allocates.</span></span> <span data-ttu-id="1eae2-111">專家會以所有要求的資訊填入結構。</span><span class="sxs-lookup"><span data-stu-id="1eae2-111">The expert fills in the structure with all requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eae2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1eae2-112">Return value</span></span>

<span data-ttu-id="1eae2-113">如果函式成功，則傳回值為 **TRUE**，而且函數會傳回要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="1eae2-113">If the function is successful, the return value is **TRUE**, and the function returns the requested information.</span></span>

<span data-ttu-id="1eae2-114">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1eae2-114">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eae2-115">備註</span><span class="sxs-lookup"><span data-stu-id="1eae2-115">Remarks</span></span>

<span data-ttu-id="1eae2-116">[**EXPERTENUMINFO**](expertenuminfo.md)結構的 **版本** 成員必須為零。</span><span class="sxs-lookup"><span data-stu-id="1eae2-116">The **Version** member of the [**EXPERTENUMINFO**](expertenuminfo.md) structure must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eae2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1eae2-117">Requirements</span></span>



| <span data-ttu-id="1eae2-118">需求</span><span class="sxs-lookup"><span data-stu-id="1eae2-118">Requirement</span></span> | <span data-ttu-id="1eae2-119">值</span><span class="sxs-lookup"><span data-stu-id="1eae2-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1eae2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1eae2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1eae2-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1eae2-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1eae2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1eae2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1eae2-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1eae2-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1eae2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1eae2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1eae2-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="1eae2-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




