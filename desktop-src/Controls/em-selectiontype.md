---
title: 'EM_SELECTIONTYPE 訊息 (Richedit .h) '
description: 判斷 rich edit 控制項的選取專案類型。
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509179"
---
# <a name="em_selectiontype-message"></a><span data-ttu-id="21995-104">EM \_ SELECTIONTYPE 訊息</span><span class="sxs-lookup"><span data-stu-id="21995-104">EM\_SELECTIONTYPE message</span></span>

<span data-ttu-id="21995-105">判斷 rich edit 控制項的選取專案類型。</span><span class="sxs-lookup"><span data-stu-id="21995-105">Determines the selection type for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="21995-106">參數</span><span class="sxs-lookup"><span data-stu-id="21995-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21995-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21995-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21995-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="21995-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="21995-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21995-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21995-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="21995-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21995-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="21995-111">Return value</span></span>

<span data-ttu-id="21995-112">如果選取範圍是空的，則傳回值會是 \_ 空的。</span><span class="sxs-lookup"><span data-stu-id="21995-112">If the selection is empty, the return value is SEL\_EMPTY.</span></span>

<span data-ttu-id="21995-113">如果選取範圍不是空的，則傳回值是一組包含下列一或多個值的旗標。</span><span class="sxs-lookup"><span data-stu-id="21995-113">If the selection is not empty, the return value is a set of flags containing one or more of the following values.</span></span>



| <span data-ttu-id="21995-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="21995-114">Return code</span></span>                                                                                     | <span data-ttu-id="21995-115">Description</span><span class="sxs-lookup"><span data-stu-id="21995-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="21995-116"><dt>**選取 \_ 文字**</dt></span><span class="sxs-lookup"><span data-stu-id="21995-116"><dt>**SEL\_TEXT**</dt></span></span> </dl>        | <span data-ttu-id="21995-117">Text。</span><span class="sxs-lookup"><span data-stu-id="21995-117">Text.</span></span><br/>                            |
| <dl> <span data-ttu-id="21995-118"><dt>**SEL \_ 物件**</dt></span><span class="sxs-lookup"><span data-stu-id="21995-118"><dt>**SEL\_OBJECT**</dt></span></span> </dl>      | <span data-ttu-id="21995-119">至少一個 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="21995-119">At least one COM object.</span></span><br/>         |
| <dl> <span data-ttu-id="21995-120"><dt>**SEL \_ MULTICHAR**</dt></span><span class="sxs-lookup"><span data-stu-id="21995-120"><dt>**SEL\_MULTICHAR**</dt></span></span> </dl>   | <span data-ttu-id="21995-121">一個以上的文字字元。</span><span class="sxs-lookup"><span data-stu-id="21995-121">More than one character of text.</span></span><br/> |
| <dl> <span data-ttu-id="21995-122"><dt>**SEL \_ MULTIOBJECT**</dt></span><span class="sxs-lookup"><span data-stu-id="21995-122"><dt>**SEL\_MULTIOBJECT**</dt></span></span> </dl> | <span data-ttu-id="21995-123">一個以上的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="21995-123">More than one COM object.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="21995-124">備註</span><span class="sxs-lookup"><span data-stu-id="21995-124">Remarks</span></span>

<span data-ttu-id="21995-125">此訊息在無底邊 rich edit 控制項父系的 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 處理期間很有用。</span><span class="sxs-lookup"><span data-stu-id="21995-125">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="21995-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="21995-126">Requirements</span></span>



| <span data-ttu-id="21995-127">需求</span><span class="sxs-lookup"><span data-stu-id="21995-127">Requirement</span></span> | <span data-ttu-id="21995-128">值</span><span class="sxs-lookup"><span data-stu-id="21995-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21995-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21995-129">Minimum supported client</span></span><br/> | <span data-ttu-id="21995-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21995-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21995-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21995-131">Minimum supported server</span></span><br/> | <span data-ttu-id="21995-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21995-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21995-133">標頭</span><span class="sxs-lookup"><span data-stu-id="21995-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="21995-134"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="21995-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21995-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21995-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21995-136">**WM \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="21995-136">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

