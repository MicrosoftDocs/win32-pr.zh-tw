---
title: 'CB_GETCUEBANNER 訊息 (Winuser .h) '
description: 取得在下拉式方塊的編輯控制項中顯示的提示橫幅文字。 明確地傳送此訊息，或使用 ComboBox \_ GetCueBannerText 宏。
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843823"
---
# <a name="cb_getcuebanner-message"></a><span data-ttu-id="33bc0-105">CB \_ GETCUEBANNER 訊息</span><span class="sxs-lookup"><span data-stu-id="33bc0-105">CB\_GETCUEBANNER message</span></span>

<span data-ttu-id="33bc0-106">取得在下拉式方塊的編輯控制項中顯示的提示橫幅文字。</span><span class="sxs-lookup"><span data-stu-id="33bc0-106">Gets the cue banner text displayed in the edit control of a combo box.</span></span> <span data-ttu-id="33bc0-107">明確地傳送此訊息，或使用 [**ComboBox \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) 宏。</span><span class="sxs-lookup"><span data-stu-id="33bc0-107">Send this message explicitly or by using the [**ComboBox\_GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="33bc0-108">參數</span><span class="sxs-lookup"><span data-stu-id="33bc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33bc0-109">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33bc0-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33bc0-110">Unicode 字串緩衝區的指標，此緩衝區會接收提示橫幅文字。</span><span class="sxs-lookup"><span data-stu-id="33bc0-110">A pointer to a Unicode string buffer that receives the cue banner text.</span></span> <span data-ttu-id="33bc0-111">呼叫應用程式負責配置緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="33bc0-111">The calling application is responsible for allocating the memory for the buffer.</span></span> <span data-ttu-id="33bc0-112">緩衝區大小必須等於 **WCHARs** 中的提示橫幅字串長度，再加上1表示終止的 **Null** **WCHAR**。</span><span class="sxs-lookup"><span data-stu-id="33bc0-112">The buffer size must be equal to the length of the cue banner string in **WCHARs**, plus 1 for the terminating **NULL** **WCHAR**.</span></span>

</dd> <dt>

<span data-ttu-id="33bc0-113">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33bc0-113">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33bc0-114">*LpcwText* 在 **WCHARs** 中所指向的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="33bc0-114">The size of the buffer pointed to by *lpcwText* in **WCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33bc0-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="33bc0-115">Return value</span></span>

<span data-ttu-id="33bc0-116">如果成功，則傳回1，否則會傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="33bc0-116">Returns 1 if successful, or an error value otherwise.</span></span>

<span data-ttu-id="33bc0-117">如果沒有要取得的提示橫幅文字，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="33bc0-117">If there is no cue banner text to get, the return value is 0.</span></span> <span data-ttu-id="33bc0-118">如果呼叫的應用程式無法配置緩衝區，或在傳送此訊息之前設定 *lParam* ，則可能會產生未定義的行為，而且傳回值可能不可靠。</span><span class="sxs-lookup"><span data-stu-id="33bc0-118">If the calling application fails to allocate a buffer, or set *lParam* before sending this message, undefined behavior may result and the return value may not be reliable.</span></span>

## <a name="requirements"></a><span data-ttu-id="33bc0-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="33bc0-119">Requirements</span></span>



| <span data-ttu-id="33bc0-120">需求</span><span class="sxs-lookup"><span data-stu-id="33bc0-120">Requirement</span></span> | <span data-ttu-id="33bc0-121">值</span><span class="sxs-lookup"><span data-stu-id="33bc0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33bc0-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33bc0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33bc0-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33bc0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="33bc0-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33bc0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33bc0-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33bc0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33bc0-126">標頭</span><span class="sxs-lookup"><span data-stu-id="33bc0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="33bc0-127"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="33bc0-127"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33bc0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33bc0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33bc0-129">下拉式列示方塊功能</span><span class="sxs-lookup"><span data-stu-id="33bc0-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





