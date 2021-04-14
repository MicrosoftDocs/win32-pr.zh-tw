---
title: 'PSM_GETTABCONTROL 訊息 (Prsht.idl .h) '
description: 抓取屬性工作表之索引標籤控制項的控制碼。 您可以使用 PropSheet GetTabControl 宏明確地傳送此訊息 \_ 。
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- PSM_GETTABCONTROL message Windows 控制項
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509075"
---
# <a name="psm_gettabcontrol-message"></a><span data-ttu-id="fd372-105">PSM \_ GETTABCONTROL 訊息</span><span class="sxs-lookup"><span data-stu-id="fd372-105">PSM\_GETTABCONTROL message</span></span>

<span data-ttu-id="fd372-106">抓取屬性工作表之索引標籤控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fd372-106">Retrieves the handle to the tab control of a property sheet.</span></span> <span data-ttu-id="fd372-107">您可以使用 [**PropSheet \_ GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="fd372-107">You can send this message explicitly or by using the [**PropSheet\_GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd372-108">參數</span><span class="sxs-lookup"><span data-stu-id="fd372-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd372-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd372-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd372-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fd372-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fd372-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd372-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd372-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fd372-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd372-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd372-113">Return value</span></span>

<span data-ttu-id="fd372-114">將控制碼傳回至索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="fd372-114">Returns the handle to the tab control.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd372-115">備註</span><span class="sxs-lookup"><span data-stu-id="fd372-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fd372-116">使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="fd372-116">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fd372-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd372-117">Requirements</span></span>



| <span data-ttu-id="fd372-118">需求</span><span class="sxs-lookup"><span data-stu-id="fd372-118">Requirement</span></span> | <span data-ttu-id="fd372-119">值</span><span class="sxs-lookup"><span data-stu-id="fd372-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd372-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd372-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd372-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd372-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fd372-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd372-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd372-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd372-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fd372-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fd372-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd372-125"><dt>Prsht.idl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd372-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





