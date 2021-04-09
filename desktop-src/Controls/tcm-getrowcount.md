---
title: 'TCM_GETROWCOUNT 訊息 (Commctrl .h) '
description: 抓取索引標籤控制項中目前的索引標籤數目。 您可以使用 TabCtrl GetRowCount 宏明確地傳送此訊息 \_ 。
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- TCM_GETROWCOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844179"
---
# <a name="tcm_getrowcount-message"></a><span data-ttu-id="1e173-105">TCM \_ GETROWCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="1e173-105">TCM\_GETROWCOUNT message</span></span>

<span data-ttu-id="1e173-106">抓取索引標籤控制項中目前的索引標籤數目。</span><span class="sxs-lookup"><span data-stu-id="1e173-106">Retrieves the current number of rows of tabs in a tab control.</span></span> <span data-ttu-id="1e173-107">您可以使用 [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1e173-107">You can send this message explicitly or by using the [**TabCtrl\_GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e173-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e173-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e173-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e173-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1e173-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1e173-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1e173-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e173-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1e173-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="1e173-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e173-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e173-113">Return value</span></span>

<span data-ttu-id="1e173-114">傳回索引標籤的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="1e173-114">Returns the number of rows of tabs.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e173-115">備註</span><span class="sxs-lookup"><span data-stu-id="1e173-115">Remarks</span></span>

<span data-ttu-id="1e173-116">只有具有 [**TCS \_ 多行**](tab-control-styles.md) 樣式的索引標籤控制項可以有多個資料列的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="1e173-116">Only tab controls that have the [**TCS\_MULTILINE**](tab-control-styles.md) style can have multiple rows of tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e173-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e173-117">Requirements</span></span>



| <span data-ttu-id="1e173-118">需求</span><span class="sxs-lookup"><span data-stu-id="1e173-118">Requirement</span></span> | <span data-ttu-id="1e173-119">值</span><span class="sxs-lookup"><span data-stu-id="1e173-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e173-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e173-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1e173-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e173-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e173-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e173-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1e173-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e173-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e173-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1e173-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e173-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e173-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





