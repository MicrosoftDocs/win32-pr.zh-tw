---
title: 'TF_LBI_STATUS_ 常數 (Ctfutb) '
description: TF \_ LBI \_ status \_ \ 常數表示 language bar 專案的狀態。 這些值會與 ITfLangBarItem GetStatus 方法搭配使用。
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686263"
---
# <a name="tf_lbi_status_-constants"></a><span data-ttu-id="200ab-104">TF \_ LBI \_ 狀態 \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="200ab-104">TF\_LBI\_STATUS\_\* Constants</span></span>

<span data-ttu-id="200ab-105">\**TF \_ LBI \_ STATUS \_ \** _ 常數表示語言列專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="200ab-105">The \**TF\_LBI\_STATUS\_\** _ constants indicate the status of a language bar item.</span></span> <span data-ttu-id="200ab-106">這些值會搭配 [ITfLangBarItem：： GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="200ab-106">These values are used with the [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) method.</span></span>



| <span data-ttu-id="200ab-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="200ab-107">Constant/value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="200ab-108">Description</span><span class="sxs-lookup"><span data-stu-id="200ab-108">Description</span></span>                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <span data-ttu-id="200ab-109"><dt>_ \* TF \_隱藏的 LBI \_ 狀態 \_ \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="200ab-109"><dt>_\*TF\_LBI\_STATUS\_HIDDEN\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="200ab-110">專案是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="200ab-110">The item is hidden.</span></span> <span data-ttu-id="200ab-111">如果專案不包含 TF \_ LBI \_ style HIDDENSTATUSCONTROL 樣式，則會忽略這個樣式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="200ab-111">This style is ignored if the item does not include the TF\_LBI\_STYLE\_HIDDENSTATUSCONTROL style.</span></span><br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <span data-ttu-id="200ab-112"><dt>**TF \_LBI \_ 狀態 \_ 停用**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="200ab-112"><dt>**TF\_LBI\_STATUS\_DISABLED**</dt> <dt>0x00000002</dt></span></span> </dl>           | <span data-ttu-id="200ab-113">項目已停用。</span><span class="sxs-lookup"><span data-stu-id="200ab-113">The item is disabled.</span></span><br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <span data-ttu-id="200ab-114"><dt>**TF \_LBI \_ 狀態 \_ BTN \_ 切換**</dt>的 <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="200ab-114"><dt>**TF\_LBI\_STATUS\_BTN\_TOGGLED**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="200ab-115">專案處於已切換或已按下的狀態。</span><span class="sxs-lookup"><span data-stu-id="200ab-115">The item is in the toggled or pressed state.</span></span> <span data-ttu-id="200ab-116">如果專案不包含 TF \_ LBI \_ style \_ BTN \_ 轉場樣式，則會忽略這個樣式。</span><span class="sxs-lookup"><span data-stu-id="200ab-116">This style is ignored if the item does not include the TF\_LBI\_STYLE\_BTN\_TOGGLE style.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="200ab-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="200ab-117">Requirements</span></span>



| <span data-ttu-id="200ab-118">需求</span><span class="sxs-lookup"><span data-stu-id="200ab-118">Requirement</span></span> | <span data-ttu-id="200ab-119">值</span><span class="sxs-lookup"><span data-stu-id="200ab-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="200ab-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="200ab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="200ab-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="200ab-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="200ab-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="200ab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="200ab-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="200ab-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="200ab-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="200ab-124">Redistributable</span></span><br/>          | <span data-ttu-id="200ab-125">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="200ab-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="200ab-126">標頭</span><span class="sxs-lookup"><span data-stu-id="200ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="200ab-127"><dt>Ctfutb。h</dt></span><span class="sxs-lookup"><span data-stu-id="200ab-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="200ab-128">Idl</span><span class="sxs-lookup"><span data-stu-id="200ab-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="200ab-129"><dt>Ctfutb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="200ab-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="200ab-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="200ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200ab-131">ITfLangBarItem：： GetStatus</span><span class="sxs-lookup"><span data-stu-id="200ab-131">ITfLangBarItem::GetStatus</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





