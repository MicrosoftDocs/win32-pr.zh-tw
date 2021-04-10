---
title: 'EM_CANPASTE 訊息 (Richedit .h) '
description: 判斷 rich edit 控制項是否可以貼上指定的剪貼簿格式。
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- EM_CANPASTE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025257"
---
# <a name="em_canpaste-message"></a><span data-ttu-id="52bbf-104">EM \_ CANPASTE 訊息</span><span class="sxs-lookup"><span data-stu-id="52bbf-104">EM\_CANPASTE message</span></span>

<span data-ttu-id="52bbf-105">判斷 rich edit 控制項是否可以貼上指定的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="52bbf-105">Determines whether a rich edit control can paste a specified clipboard format.</span></span>

## <a name="parameters"></a><span data-ttu-id="52bbf-106">參數</span><span class="sxs-lookup"><span data-stu-id="52bbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52bbf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52bbf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52bbf-108">指定要嘗試的 [剪貼簿格式](/windows/desktop/dataxchg/clipboard-formats) 。</span><span class="sxs-lookup"><span data-stu-id="52bbf-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats) to try.</span></span> <span data-ttu-id="52bbf-109">若要嘗試目前剪貼簿上的任何格式，請將此參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="52bbf-109">To try any format currently on the clipboard, set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="52bbf-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52bbf-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52bbf-111">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="52bbf-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52bbf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="52bbf-112">Return value</span></span>

<span data-ttu-id="52bbf-113">如果可以貼上剪貼簿格式，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="52bbf-113">If the clipboard format can be pasted, the return value is a nonzero value.</span></span>

<span data-ttu-id="52bbf-114">如果無法貼上剪貼簿格式，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="52bbf-114">If the clipboard format cannot be pasted, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="52bbf-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="52bbf-115">Requirements</span></span>



| <span data-ttu-id="52bbf-116">需求</span><span class="sxs-lookup"><span data-stu-id="52bbf-116">Requirement</span></span> | <span data-ttu-id="52bbf-117">值</span><span class="sxs-lookup"><span data-stu-id="52bbf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52bbf-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52bbf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52bbf-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52bbf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52bbf-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52bbf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52bbf-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52bbf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52bbf-122">標頭</span><span class="sxs-lookup"><span data-stu-id="52bbf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="52bbf-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="52bbf-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52bbf-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52bbf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52bbf-125">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="52bbf-125">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

