---
title: 'EM_GETTEXTRANGE 訊息 (Richedit .h) '
description: 從 rich edit 控制項抓取指定的字元範圍。
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- EM_GETTEXTRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934809"
---
# <a name="em_gettextrange-message"></a><span data-ttu-id="fdfad-104">EM \_ GETTEXTRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="fdfad-104">EM\_GETTEXTRANGE message</span></span>

<span data-ttu-id="fdfad-105">從 rich edit 控制項抓取指定的字元範圍。</span><span class="sxs-lookup"><span data-stu-id="fdfad-105">Retrieves a specified range of characters from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdfad-106">參數</span><span class="sxs-lookup"><span data-stu-id="fdfad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdfad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdfad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdfad-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="fdfad-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fdfad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdfad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdfad-110">[**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea)結構的指標，指定要取出的字元範圍，以及要將字元複製到其中的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fdfad-110">Pointer to a [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure that specifies the range of characters to retrieve and a buffer to copy the characters to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdfad-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdfad-111">Return value</span></span>

<span data-ttu-id="fdfad-112">訊息會傳回復制的字元數，而不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="fdfad-112">The message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdfad-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdfad-113">Requirements</span></span>



| <span data-ttu-id="fdfad-114">需求</span><span class="sxs-lookup"><span data-stu-id="fdfad-114">Requirement</span></span> | <span data-ttu-id="fdfad-115">值</span><span class="sxs-lookup"><span data-stu-id="fdfad-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdfad-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdfad-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fdfad-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdfad-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdfad-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdfad-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fdfad-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdfad-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdfad-120">標頭</span><span class="sxs-lookup"><span data-stu-id="fdfad-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdfad-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fdfad-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdfad-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdfad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdfad-123">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="fdfad-123">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





