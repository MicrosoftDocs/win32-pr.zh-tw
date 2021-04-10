---
title: 'EM_GETSELTEXT 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項中目前選取的文字。
ms.assetid: 56af77c3-f2d7-4b5d-895f-a67c141459e3
keywords:
- EM_GETSELTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETSELTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde2c0677fa04ff6d7991bca56bad0c08a6f5ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843487"
---
# <a name="em_getseltext-message"></a><span data-ttu-id="66d05-104">EM \_ GETSELTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="66d05-104">EM\_GETSELTEXT message</span></span>

<span data-ttu-id="66d05-105">抓取 rich edit 控制項中目前選取的文字。</span><span class="sxs-lookup"><span data-stu-id="66d05-105">Retrieves the currently selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="66d05-106">參數</span><span class="sxs-lookup"><span data-stu-id="66d05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d05-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66d05-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66d05-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="66d05-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="66d05-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66d05-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66d05-110">接收選取文字之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="66d05-110">Pointer to a buffer that receives the selected text.</span></span> <span data-ttu-id="66d05-111">呼叫應用程式必須確定緩衝區夠大，足以容納選取的文字。</span><span class="sxs-lookup"><span data-stu-id="66d05-111">The calling application must ensure that the buffer is large enough to hold the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d05-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="66d05-112">Return value</span></span>

<span data-ttu-id="66d05-113">此訊息會傳回復制的字元數，而不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="66d05-113">This message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d05-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="66d05-114">Requirements</span></span>



| <span data-ttu-id="66d05-115">需求</span><span class="sxs-lookup"><span data-stu-id="66d05-115">Requirement</span></span> | <span data-ttu-id="66d05-116">值</span><span class="sxs-lookup"><span data-stu-id="66d05-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66d05-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66d05-117">Minimum supported client</span></span><br/> | <span data-ttu-id="66d05-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66d05-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66d05-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66d05-119">Minimum supported server</span></span><br/> | <span data-ttu-id="66d05-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66d05-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66d05-121">標頭</span><span class="sxs-lookup"><span data-stu-id="66d05-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d05-122"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="66d05-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





