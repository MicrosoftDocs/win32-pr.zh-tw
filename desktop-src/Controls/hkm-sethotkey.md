---
title: 'HKM_SETHOTKEY 訊息 (Commctrl .h) '
description: 設定快速鍵控制項的快速鍵組合。
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY message Windows 控制項
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508491"
---
# <a name="hkm_sethotkey-message"></a><span data-ttu-id="2c39d-104">HKM \_ SETHOTKEY 訊息</span><span class="sxs-lookup"><span data-stu-id="2c39d-104">HKM\_SETHOTKEY message</span></span>

<span data-ttu-id="2c39d-105">設定快速鍵控制項的快速鍵組合。</span><span class="sxs-lookup"><span data-stu-id="2c39d-105">Sets the hot key combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c39d-106">參數</span><span class="sxs-lookup"><span data-stu-id="2c39d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c39d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c39d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c39d-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))的 [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))是快速鍵的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="2c39d-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="2c39d-109">**LOWORD** 的 [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85))是索引鍵修飾詞，表示定義快速鍵組合的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2c39d-109">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that indicates the keys that define a hot key combination.</span></span> <span data-ttu-id="2c39d-110">如需修飾詞旗標值的清單，請參閱 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息的說明。</span><span class="sxs-lookup"><span data-stu-id="2c39d-110">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="2c39d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c39d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c39d-112">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="2c39d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c39d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c39d-113">Return value</span></span>

<span data-ttu-id="2c39d-114">永遠傳回零。</span><span class="sxs-lookup"><span data-stu-id="2c39d-114">Always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c39d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c39d-115">Requirements</span></span>



| <span data-ttu-id="2c39d-116">需求</span><span class="sxs-lookup"><span data-stu-id="2c39d-116">Requirement</span></span> | <span data-ttu-id="2c39d-117">值</span><span class="sxs-lookup"><span data-stu-id="2c39d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c39d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c39d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c39d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c39d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c39d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c39d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c39d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c39d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c39d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2c39d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c39d-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c39d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

