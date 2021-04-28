---
title: 'TB_SETHOTITEM 訊息 (Commctrl .h) '
description: TB_SETHOTITEM 訊息：設定工具列中的熱專案。
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104176"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="3db96-104">TB \_ SETHOTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="3db96-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="3db96-105">設定工具列中的熱專案。</span><span class="sxs-lookup"><span data-stu-id="3db96-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3db96-106">參數</span><span class="sxs-lookup"><span data-stu-id="3db96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3db96-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3db96-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3db96-108">將設為經常性存取之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="3db96-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="3db96-109">如果這個值是-1，則沒有任何專案會是經常性的。</span><span class="sxs-lookup"><span data-stu-id="3db96-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="3db96-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3db96-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3db96-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3db96-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3db96-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3db96-112">Return value</span></span>

<span data-ttu-id="3db96-113">傳回先前熱專案的索引，如果沒有熱專案，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="3db96-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="3db96-114">備註</span><span class="sxs-lookup"><span data-stu-id="3db96-114">Remarks</span></span>

<span data-ttu-id="3db96-115">未針對沒有 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式的工具列定義此訊息的行為。</span><span class="sxs-lookup"><span data-stu-id="3db96-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db96-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3db96-116">Requirements</span></span>



| <span data-ttu-id="3db96-117">需求</span><span class="sxs-lookup"><span data-stu-id="3db96-117">Requirement</span></span> | <span data-ttu-id="3db96-118">值</span><span class="sxs-lookup"><span data-stu-id="3db96-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3db96-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3db96-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3db96-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3db96-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3db96-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3db96-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3db96-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3db96-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3db96-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3db96-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3db96-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3db96-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





