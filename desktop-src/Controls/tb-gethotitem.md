---
title: 'TB_GETHOTITEM 訊息 (Commctrl .h) '
description: 抓取工具列中熱專案的索引。
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- TB_GETHOTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465032"
---
# <a name="tb_gethotitem-message"></a><span data-ttu-id="5980f-104">TB \_ GETHOTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="5980f-104">TB\_GETHOTITEM message</span></span>

<span data-ttu-id="5980f-105">抓取工具列中熱專案的索引。</span><span class="sxs-lookup"><span data-stu-id="5980f-105">Retrieves the index of the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5980f-106">參數</span><span class="sxs-lookup"><span data-stu-id="5980f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5980f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5980f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5980f-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5980f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5980f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5980f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5980f-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5980f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5980f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5980f-111">Return value</span></span>

<span data-ttu-id="5980f-112">傳回熱專案的索引，如果沒有設定熱專案，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="5980f-112">Returns the index of the hot item, or -1 if no hot item is set.</span></span> <span data-ttu-id="5980f-113">沒有 [ [**TBSTYLE] \_ 平面**](toolbar-control-and-button-styles.md) 樣式的工具列控制項沒有熱專案。</span><span class="sxs-lookup"><span data-stu-id="5980f-113">Toolbar controls that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style do not have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="5980f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5980f-114">Requirements</span></span>



| <span data-ttu-id="5980f-115">需求</span><span class="sxs-lookup"><span data-stu-id="5980f-115">Requirement</span></span> | <span data-ttu-id="5980f-116">值</span><span class="sxs-lookup"><span data-stu-id="5980f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5980f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5980f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5980f-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5980f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5980f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5980f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5980f-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5980f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5980f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5980f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5980f-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5980f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





