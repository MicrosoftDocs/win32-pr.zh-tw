---
title: 'EM_GETSCROLLPOS 訊息 (Richedit .h) '
description: 取得編輯控制項的目前滾動位置。
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465153"
---
# <a name="em_getscrollpos-message"></a><span data-ttu-id="87f96-104">EM \_ GETSCROLLPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="87f96-104">EM\_GETSCROLLPOS message</span></span>

<span data-ttu-id="87f96-105">取得編輯控制項的目前滾動位置。</span><span class="sxs-lookup"><span data-stu-id="87f96-105">Obtains the current scroll position of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="87f96-106">參數</span><span class="sxs-lookup"><span data-stu-id="87f96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f96-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87f96-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87f96-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="87f96-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="87f96-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87f96-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87f96-110">[**點**](/previous-versions//dd162805(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="87f96-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <span data-ttu-id="87f96-111">在呼叫 **EM \_ GETSCROLLPOS** 之後，此參數會在檔的虛擬文字空間中包含點（以圖元表示）。</span><span class="sxs-lookup"><span data-stu-id="87f96-111">After calling **EM\_GETSCROLLPOS**, this parameters contains a point in the virtual text space of the document, expressed in pixels.</span></span> <span data-ttu-id="87f96-112">這一點將會是目前位於 [編輯] 控制項視窗左上角的點。</span><span class="sxs-lookup"><span data-stu-id="87f96-112">This point will be the point that is currently located in the upper-left corner of the edit control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f96-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="87f96-113">Return value</span></span>

<span data-ttu-id="87f96-114">此訊息一律會傳回1。</span><span class="sxs-lookup"><span data-stu-id="87f96-114">This message always returns 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="87f96-115">備註</span><span class="sxs-lookup"><span data-stu-id="87f96-115">Remarks</span></span>

<span data-ttu-id="87f96-116">[**點**](/previous-versions//dd162805(v=vs.85))結構中所傳回的值為16位值， (偶數) 的32位寬欄位中。</span><span class="sxs-lookup"><span data-stu-id="87f96-116">The values returned in the [**POINT**](/previous-versions//dd162805(v=vs.85)) structure are 16-bit values (even in the 32-bit wide fields).</span></span>

## <a name="requirements"></a><span data-ttu-id="87f96-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="87f96-117">Requirements</span></span>



| <span data-ttu-id="87f96-118">需求</span><span class="sxs-lookup"><span data-stu-id="87f96-118">Requirement</span></span> | <span data-ttu-id="87f96-119">值</span><span class="sxs-lookup"><span data-stu-id="87f96-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87f96-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87f96-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87f96-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87f96-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87f96-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87f96-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87f96-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87f96-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87f96-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="87f96-124">Redistributable</span></span><br/>          | <span data-ttu-id="87f96-125">Rich Edit 3。0</span><span class="sxs-lookup"><span data-stu-id="87f96-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="87f96-126">標頭</span><span class="sxs-lookup"><span data-stu-id="87f96-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f96-127"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="87f96-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f96-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87f96-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f96-129">**EM \_ SETSCROLLPOS**</span><span class="sxs-lookup"><span data-stu-id="87f96-129">**EM\_SETSCROLLPOS**</span></span>](em-setscrollpos.md)
</dt> </dl>

 

