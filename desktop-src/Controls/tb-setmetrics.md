---
title: 'TB_SETMETRICS 訊息 (Commctrl .h) '
description: 設定工具列控制項的度量。
ms.assetid: 60e35d65-6291-4a55-a4cf-19b5b1db8a65
keywords:
- TB_SETMETRICS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5320ecc85f0a44c4c80868ae5699b051e1ac1781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934092"
---
# <a name="tb_setmetrics-message"></a><span data-ttu-id="0f94e-104">TB \_ SETMETRICS 訊息</span><span class="sxs-lookup"><span data-stu-id="0f94e-104">TB\_SETMETRICS message</span></span>

<span data-ttu-id="0f94e-105">設定工具列控制項的度量。</span><span class="sxs-lookup"><span data-stu-id="0f94e-105">Sets the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f94e-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f94e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f94e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f94e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f94e-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0f94e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f94e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f94e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f94e-110">[**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) 結構，其中包含要設定的工具列度量。</span><span class="sxs-lookup"><span data-stu-id="0f94e-110">[**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that contains the toolbar metrics to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f94e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f94e-111">Return value</span></span>

<span data-ttu-id="0f94e-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="0f94e-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f94e-113">備註</span><span class="sxs-lookup"><span data-stu-id="0f94e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f94e-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="0f94e-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="0f94e-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="0f94e-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f94e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f94e-116">Requirements</span></span>



| <span data-ttu-id="0f94e-117">需求</span><span class="sxs-lookup"><span data-stu-id="0f94e-117">Requirement</span></span> | <span data-ttu-id="0f94e-118">值</span><span class="sxs-lookup"><span data-stu-id="0f94e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f94e-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f94e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f94e-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f94e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f94e-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f94e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f94e-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f94e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f94e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0f94e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f94e-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f94e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





