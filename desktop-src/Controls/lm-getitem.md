---
title: 'LM_GETITEM 訊息 (Commctrl .h) '
description: 抓取專案的狀態和屬性。
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- LM_GETITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093868"
---
# <a name="lm_getitem-message"></a><span data-ttu-id="f824d-104">LM \_ GETITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="f824d-104">LM\_GETITEM message</span></span>

<span data-ttu-id="f824d-105">抓取專案的狀態和屬性。</span><span class="sxs-lookup"><span data-stu-id="f824d-105">Retrieves the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="f824d-106">參數</span><span class="sxs-lookup"><span data-stu-id="f824d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f824d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f824d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f824d-108">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f824d-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="f824d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f824d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f824d-110">要填入專案相關資訊之 <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f824d-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure to be filled with information about the item.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f824d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f824d-111">Return value</span></span>

<span data-ttu-id="f824d-112">如果訊息成功取得指定的值和屬性，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f824d-112">Returns **TRUE** if the message succeeds in getting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="f824d-113">備註</span><span class="sxs-lookup"><span data-stu-id="f824d-113">Remarks</span></span>

<span data-ttu-id="f824d-114">使用 **LM \_ GETITEM** 訊息時，只能透過 [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem)的 **ashraf** 成員所傳回的數值索引來存取連結。</span><span class="sxs-lookup"><span data-stu-id="f824d-114">With the **LM\_GETITEM** message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="f824d-115">不支援透過 **szID** 中傳回的識別碼名稱來存取連結。</span><span class="sxs-lookup"><span data-stu-id="f824d-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="f824d-116">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="f824d-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f824d-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f824d-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f824d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f824d-118">Requirements</span></span>



| <span data-ttu-id="f824d-119">需求</span><span class="sxs-lookup"><span data-stu-id="f824d-119">Requirement</span></span> | <span data-ttu-id="f824d-120">值</span><span class="sxs-lookup"><span data-stu-id="f824d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f824d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f824d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f824d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f824d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f824d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f824d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f824d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f824d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f824d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f824d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f824d-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f824d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





