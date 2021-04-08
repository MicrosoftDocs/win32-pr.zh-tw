---
title: 'TB_GETEXTENDEDSTYLE 訊息 (Commctrl .h) '
description: 抓取工具列控制項的延伸樣式。
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- TB_GETEXTENDEDSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80bc4f4ad45e5c1c75366e0890f3fd76ec1fa74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685835"
---
# <a name="tb_getextendedstyle-message"></a><span data-ttu-id="17000-104">TB \_ GETEXTENDEDSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="17000-104">TB\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="17000-105">抓取工具列控制項的延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="17000-105">Retrieves the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="17000-106">參數</span><span class="sxs-lookup"><span data-stu-id="17000-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17000-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17000-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="17000-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="17000-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="17000-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17000-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="17000-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="17000-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17000-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="17000-111">Return value</span></span>

<span data-ttu-id="17000-112">傳回 **DWORD** ，表示目前在工具列控制項中使用的樣式。</span><span class="sxs-lookup"><span data-stu-id="17000-112">Returns a **DWORD** that represents the styles currently in use for the toolbar control.</span></span> <span data-ttu-id="17000-113">這個值可以是 [擴充樣式](toolbar-extended-styles.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="17000-113">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17000-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="17000-114">Requirements</span></span>



| <span data-ttu-id="17000-115">需求</span><span class="sxs-lookup"><span data-stu-id="17000-115">Requirement</span></span> | <span data-ttu-id="17000-116">值</span><span class="sxs-lookup"><span data-stu-id="17000-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17000-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17000-117">Minimum supported client</span></span><br/> | <span data-ttu-id="17000-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17000-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17000-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17000-119">Minimum supported server</span></span><br/> | <span data-ttu-id="17000-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17000-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17000-121">標頭</span><span class="sxs-lookup"><span data-stu-id="17000-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="17000-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="17000-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17000-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17000-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17000-124">**TB \_ SETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="17000-124">**TB\_SETEXTENDEDSTYLE**</span></span>](tb-setextendedstyle.md)
</dt> </dl>

 

 





