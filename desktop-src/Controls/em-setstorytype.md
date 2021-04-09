---
title: 'EM_SETSTORYTYPE 訊息 (Richedit .h) '
description: 設定案例類型。
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- EM_SETSTORYTYPE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843363"
---
# <a name="em_setstorytype-message"></a><span data-ttu-id="596f1-104">EM \_ SETSTORYTYPE 訊息</span><span class="sxs-lookup"><span data-stu-id="596f1-104">EM\_SETSTORYTYPE message</span></span>

<span data-ttu-id="596f1-105">設定案例類型。</span><span class="sxs-lookup"><span data-stu-id="596f1-105">Sets the story type.</span></span>


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a><span data-ttu-id="596f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="596f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="596f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="596f1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="596f1-108">故事索引。</span><span class="sxs-lookup"><span data-stu-id="596f1-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="596f1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="596f1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="596f1-110">新的案例類型。</span><span class="sxs-lookup"><span data-stu-id="596f1-110">The new story type.</span></span> <span data-ttu-id="596f1-111">如需故事類型的清單，請參閱 [**EM \_ GETSTORYTYPE**](em-getstorytype.md)。</span><span class="sxs-lookup"><span data-stu-id="596f1-111">For a list of story types, see [**EM\_GETSTORYTYPE**](em-getstorytype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="596f1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="596f1-112">Return value</span></span>

<span data-ttu-id="596f1-113">已設定的案例類型。</span><span class="sxs-lookup"><span data-stu-id="596f1-113">The story type that was set.</span></span>

## <a name="requirements"></a><span data-ttu-id="596f1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="596f1-114">Requirements</span></span>



| <span data-ttu-id="596f1-115">需求</span><span class="sxs-lookup"><span data-stu-id="596f1-115">Requirement</span></span> | <span data-ttu-id="596f1-116">值</span><span class="sxs-lookup"><span data-stu-id="596f1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="596f1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="596f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="596f1-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="596f1-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="596f1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="596f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="596f1-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="596f1-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="596f1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="596f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="596f1-122"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="596f1-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





