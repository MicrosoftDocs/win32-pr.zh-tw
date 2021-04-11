---
title: 'TB_SETHOTITEM 訊息 (Commctrl .h) '
description: 設定工具列中的熱專案。
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
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843980"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="f7d92-104">TB \_ SETHOTITEM 訊息</span><span class="sxs-lookup"><span data-stu-id="f7d92-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="f7d92-105">設定工具列中的熱專案。</span><span class="sxs-lookup"><span data-stu-id="f7d92-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7d92-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7d92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d92-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7d92-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d92-108">將設為經常性存取之專案的索引。</span><span class="sxs-lookup"><span data-stu-id="f7d92-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="f7d92-109">如果這個值是-1，則沒有任何專案會是經常性的。</span><span class="sxs-lookup"><span data-stu-id="f7d92-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="f7d92-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7d92-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f7d92-111">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f7d92-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d92-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7d92-112">Return value</span></span>

<span data-ttu-id="f7d92-113">傳回先前熱專案的索引，如果沒有熱專案，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="f7d92-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d92-114">備註</span><span class="sxs-lookup"><span data-stu-id="f7d92-114">Remarks</span></span>

<span data-ttu-id="f7d92-115">未針對沒有 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式的工具列定義此訊息的行為。</span><span class="sxs-lookup"><span data-stu-id="f7d92-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d92-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7d92-116">Requirements</span></span>



| <span data-ttu-id="f7d92-117">需求</span><span class="sxs-lookup"><span data-stu-id="f7d92-117">Requirement</span></span> | <span data-ttu-id="f7d92-118">值</span><span class="sxs-lookup"><span data-stu-id="f7d92-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d92-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7d92-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d92-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7d92-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7d92-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7d92-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d92-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7d92-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7d92-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f7d92-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d92-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d92-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





