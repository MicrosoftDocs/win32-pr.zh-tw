---
title: 'HKM_GETHOTKEY 訊息 (Commctrl .h) '
description: 從熱鍵控制項取得快速鍵的虛擬按鍵碼和修飾詞旗標。
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY message Windows 控制項
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465044"
---
# <a name="hkm_gethotkey-message"></a><span data-ttu-id="1b5f5-104">HKM \_ GETHOTKEY 訊息</span><span class="sxs-lookup"><span data-stu-id="1b5f5-104">HKM\_GETHOTKEY message</span></span>

<span data-ttu-id="1b5f5-105">從熱鍵控制項取得快速鍵的虛擬按鍵碼和修飾詞旗標。</span><span class="sxs-lookup"><span data-stu-id="1b5f5-105">Gets the virtual key code and modifier flags of a hot key from a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b5f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="1b5f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b5f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b5f5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b5f5-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1b5f5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1b5f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b5f5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1b5f5-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1b5f5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b5f5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1b5f5-111">Return value</span></span>

<span data-ttu-id="1b5f5-112">傳回虛擬按鍵碼和修飾詞旗標。</span><span class="sxs-lookup"><span data-stu-id="1b5f5-112">Returns the virtual key code and modifier flags.</span></span> <span data-ttu-id="1b5f5-113">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))的 [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))是快速鍵的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="1b5f5-113">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="1b5f5-114">**LOWORD** 的 [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85))是索引鍵修飾詞，可指定定義快速鍵組合的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1b5f5-114">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that specifies the keys that define a hot key combination.</span></span> <span data-ttu-id="1b5f5-115">修飾詞旗標可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="1b5f5-115">The modifier flags can be a combination of the following values.</span></span>



| <span data-ttu-id="1b5f5-116">值</span><span class="sxs-lookup"><span data-stu-id="1b5f5-116">Value</span></span>            | <span data-ttu-id="1b5f5-117">意義</span><span class="sxs-lookup"><span data-stu-id="1b5f5-117">Meaning</span></span>      |
|------------------|--------------|
| <span data-ttu-id="1b5f5-118">HOTKEYF \_ ALT</span><span class="sxs-lookup"><span data-stu-id="1b5f5-118">HOTKEYF\_ALT</span></span>     | <span data-ttu-id="1b5f5-119">ALT 鍵</span><span class="sxs-lookup"><span data-stu-id="1b5f5-119">ALT key</span></span>      |
| <span data-ttu-id="1b5f5-120">HOTKEYF \_ 控制項</span><span class="sxs-lookup"><span data-stu-id="1b5f5-120">HOTKEYF\_CONTROL</span></span> | <span data-ttu-id="1b5f5-121">控制索引鍵</span><span class="sxs-lookup"><span data-stu-id="1b5f5-121">CONTROL key</span></span>  |
| <span data-ttu-id="1b5f5-122">HOTKEYF \_ EXT</span><span class="sxs-lookup"><span data-stu-id="1b5f5-122">HOTKEYF\_EXT</span></span>     | <span data-ttu-id="1b5f5-123">擴充金鑰</span><span class="sxs-lookup"><span data-stu-id="1b5f5-123">Extended key</span></span> |
| <span data-ttu-id="1b5f5-124">HOTKEYF \_ SHIFT</span><span class="sxs-lookup"><span data-stu-id="1b5f5-124">HOTKEYF\_SHIFT</span></span>   | <span data-ttu-id="1b5f5-125">SHIFT 鍵</span><span class="sxs-lookup"><span data-stu-id="1b5f5-125">SHIFT key</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="1b5f5-126">備註</span><span class="sxs-lookup"><span data-stu-id="1b5f5-126">Remarks</span></span>

<span data-ttu-id="1b5f5-127">此訊息所傳回的16位值可用來作為 [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey)訊息中的 *wParam* 參數。</span><span class="sxs-lookup"><span data-stu-id="1b5f5-127">The 16-bit value returned by this message can be used as the *wParam* parameter in the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b5f5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b5f5-128">Requirements</span></span>



| <span data-ttu-id="1b5f5-129">需求</span><span class="sxs-lookup"><span data-stu-id="1b5f5-129">Requirement</span></span> | <span data-ttu-id="1b5f5-130">值</span><span class="sxs-lookup"><span data-stu-id="1b5f5-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b5f5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b5f5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1b5f5-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b5f5-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b5f5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b5f5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1b5f5-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b5f5-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b5f5-135">標頭</span><span class="sxs-lookup"><span data-stu-id="1b5f5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b5f5-136"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1b5f5-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

