---
title: 'TB_GETMETRICS 訊息 (Commctrl .h) '
description: 抓取工具列控制項的度量。
ms.assetid: 19c735cf-09f8-443e-8a73-dd64af0193a1
keywords:
- TB_GETMETRICS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1ee299f56b367eef649a05657d713e22206a7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843988"
---
# <a name="tb_getmetrics-message"></a><span data-ttu-id="62437-104">TB \_ GETMETRICS 訊息</span><span class="sxs-lookup"><span data-stu-id="62437-104">TB\_GETMETRICS message</span></span>

<span data-ttu-id="62437-105">抓取工具列控制項的度量。</span><span class="sxs-lookup"><span data-stu-id="62437-105">Retrieves the metrics of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="62437-106">參數</span><span class="sxs-lookup"><span data-stu-id="62437-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62437-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62437-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62437-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="62437-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="62437-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62437-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62437-110">[**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics)結構的指標，此結構會接收工具列度量。</span><span class="sxs-lookup"><span data-stu-id="62437-110">Pointer to a [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics) structure that receives the toolbar metrics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62437-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="62437-111">Return value</span></span>

<span data-ttu-id="62437-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="62437-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="62437-113">備註</span><span class="sxs-lookup"><span data-stu-id="62437-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="62437-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="62437-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="62437-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="62437-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62437-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="62437-116">Requirements</span></span>



| <span data-ttu-id="62437-117">需求</span><span class="sxs-lookup"><span data-stu-id="62437-117">Requirement</span></span> | <span data-ttu-id="62437-118">值</span><span class="sxs-lookup"><span data-stu-id="62437-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62437-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62437-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62437-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62437-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62437-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62437-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62437-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62437-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62437-123">標頭</span><span class="sxs-lookup"><span data-stu-id="62437-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62437-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="62437-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





