---
title: 'CBEM_HASEDITCHANGED 訊息 (Commctrl .h) '
description: 判斷使用者是否已變更 ComboBoxEx 編輯控制項的文字。
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- CBEM_HASEDITCHANGED message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935100"
---
# <a name="cbem_haseditchanged-message"></a><span data-ttu-id="cc58b-104">CBEM \_ HASEDITCHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="cc58b-104">CBEM\_HASEDITCHANGED message</span></span>

<span data-ttu-id="cc58b-105">判斷使用者是否已變更 ComboBoxEx 編輯控制項的文字。</span><span class="sxs-lookup"><span data-stu-id="cc58b-105">Determines whether the user has changed the text of a ComboBoxEx edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc58b-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc58b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc58b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc58b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cc58b-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="cc58b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cc58b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc58b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cc58b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="cc58b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc58b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc58b-111">Return value</span></span>

<span data-ttu-id="cc58b-112">如果控制項編輯方塊中的文字已變更，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="cc58b-112">Returns **TRUE** if the text in the control's edit box has been changed, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc58b-113">備註</span><span class="sxs-lookup"><span data-stu-id="cc58b-113">Remarks</span></span>

<span data-ttu-id="cc58b-114">當 ComboBoxEx 控制項設定為 [**CBS \_ 下拉式**](combo-box-styles.md) 樣式時，會使用編輯方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="cc58b-114">A ComboBoxEx control uses an edit box control when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="cc58b-115">您可以藉由傳送 [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) 訊息來取得編輯方塊控制項的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="cc58b-115">You can retrieve the edit box control's window handle by sending a [**CBEM\_GETEDITCONTROL**](cbem-geteditcontrol.md) message.</span></span>

<span data-ttu-id="cc58b-116">當使用者開始編輯時，您將會收到 [CBEN \_ BEGINEDIT](cben-beginedit.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="cc58b-116">When the user begins editing, you will receive a [CBEN\_BEGINEDIT](cben-beginedit.md) notification.</span></span> <span data-ttu-id="cc58b-117">當編輯完成或焦點變更時，您將會收到 [CBEN \_ ENDEDIT](cben-endedit.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="cc58b-117">When editing is complete, or the focus changes, you will receive a [CBEN\_ENDEDIT](cben-endedit.md) notification.</span></span> <span data-ttu-id="cc58b-118">**CBEM \_ HASEDITCHANGED** 訊息只適用于在 CBEN ENDEDIT 通知之前，判斷文字是否已變更 \_ 。</span><span class="sxs-lookup"><span data-stu-id="cc58b-118">The **CBEM\_HASEDITCHANGED** message is only useful for determining whether the text has been changed if it is sent before the CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="cc58b-119">如果訊息在之後傳送，則會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cc58b-119">If the message is sent afterward, it will return **FALSE**.</span></span> <span data-ttu-id="cc58b-120">例如，假設使用者開始編輯編輯方塊中的文字，但變更焦點，產生 CBEN \_ ENDEDIT 通知。</span><span class="sxs-lookup"><span data-stu-id="cc58b-120">For example, suppose the user starts to edit the text in the edit box but changes focus, generating a CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="cc58b-121">如果您接著傳送 **CBEM \_ HASEDITCHANGED** 訊息，它會傳回 **FALSE**，即使文字已變更也是一樣。</span><span class="sxs-lookup"><span data-stu-id="cc58b-121">If you then send a **CBEM\_HASEDITCHANGED** message, it will return **FALSE**, even though the text has been changed.</span></span>

<span data-ttu-id="cc58b-122">[**CBS \_ 簡單**](combo-box-styles.md)樣式無法與 **CBEM \_ HASEDITCHANGED** 正常搭配運作。</span><span class="sxs-lookup"><span data-stu-id="cc58b-122">The [**CBS\_SIMPLE**](combo-box-styles.md) style does not work correctly with **CBEM\_HASEDITCHANGED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc58b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc58b-123">Requirements</span></span>



| <span data-ttu-id="cc58b-124">需求</span><span class="sxs-lookup"><span data-stu-id="cc58b-124">Requirement</span></span> | <span data-ttu-id="cc58b-125">值</span><span class="sxs-lookup"><span data-stu-id="cc58b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc58b-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc58b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cc58b-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc58b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc58b-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc58b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cc58b-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc58b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc58b-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cc58b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc58b-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cc58b-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





