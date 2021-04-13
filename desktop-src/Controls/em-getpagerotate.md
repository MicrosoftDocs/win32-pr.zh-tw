---
title: 'EM_GETPAGEROTATE 訊息 (Richedit .h) '
description: 取得 Microsoft Rich Edit 控制項的文字版面配置。
ms.assetid: 0efb112e-ad51-4ebb-9037-3aee3ab9ad1d
keywords:
- EM_GETPAGEROTATE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7bc7cd3c77ae88cd4c8710e14b4472e57407ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466560"
---
# <a name="em_getpagerotate-message"></a><span data-ttu-id="afc28-104">EM \_ GETPAGEROTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="afc28-104">EM\_GETPAGEROTATE message</span></span>

<span data-ttu-id="afc28-105">\[**EM \_GETPAGEROTATE** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="afc28-105">\[**EM\_GETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="afc28-106">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="afc28-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="afc28-107">取得 Microsoft Rich Edit 控制項的文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="afc28-107">Gets the text layout for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="afc28-108">參數</span><span class="sxs-lookup"><span data-stu-id="afc28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc28-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afc28-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afc28-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="afc28-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="afc28-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afc28-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afc28-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="afc28-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc28-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="afc28-113">Return value</span></span>

<span data-ttu-id="afc28-114">取得目前的文字版面配置。</span><span class="sxs-lookup"><span data-stu-id="afc28-114">Gets the current text layout.</span></span> <span data-ttu-id="afc28-115">如需可能的文字版面配置值清單，請參閱 [**EM \_ SETPAGEROTATE**](em-setpagerotate.md)。</span><span class="sxs-lookup"><span data-stu-id="afc28-115">For a list of possible text layout values, see [**EM\_SETPAGEROTATE**](em-setpagerotate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afc28-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="afc28-116">Requirements</span></span>



| <span data-ttu-id="afc28-117">需求</span><span class="sxs-lookup"><span data-stu-id="afc28-117">Requirement</span></span> | <span data-ttu-id="afc28-118">值</span><span class="sxs-lookup"><span data-stu-id="afc28-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afc28-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afc28-119">Minimum supported client</span></span><br/> | <span data-ttu-id="afc28-120">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afc28-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afc28-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afc28-121">Minimum supported server</span></span><br/> | <span data-ttu-id="afc28-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afc28-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afc28-123">標頭</span><span class="sxs-lookup"><span data-stu-id="afc28-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc28-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="afc28-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc28-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afc28-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc28-126">**EM \_ SETPAGEROTATE**</span><span class="sxs-lookup"><span data-stu-id="afc28-126">**EM\_SETPAGEROTATE**</span></span>](em-setpagerotate.md)
</dt> </dl>

 

 





