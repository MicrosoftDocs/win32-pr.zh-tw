---
title: 'MCM_GETCALENDARGRIDINFO 訊息 (Commctrl .h) '
description: 取得行事曆方格的相關資訊。
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686675"
---
# <a name="mcm_getcalendargridinfo-message"></a><span data-ttu-id="93365-104">MCM \_ GETCALENDARGRIDINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="93365-104">MCM\_GETCALENDARGRIDINFO message</span></span>

<span data-ttu-id="93365-105">取得行事曆方格的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="93365-105">Gets information about a calendar grid.</span></span>

## <a name="parameters"></a><span data-ttu-id="93365-106">參數</span><span class="sxs-lookup"><span data-stu-id="93365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93365-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93365-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93365-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="93365-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="93365-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93365-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93365-110">[**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo)結構的指標，其中包含行事曆方格的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="93365-110">Pointer to an [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) structure that contains information about the calendar grid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93365-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="93365-111">Return value</span></span>

<span data-ttu-id="93365-112">如果成功則 **為 TRUE** ，否則為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="93365-112">**TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="93365-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="93365-113">Requirements</span></span>



| <span data-ttu-id="93365-114">需求</span><span class="sxs-lookup"><span data-stu-id="93365-114">Requirement</span></span> | <span data-ttu-id="93365-115">值</span><span class="sxs-lookup"><span data-stu-id="93365-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93365-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93365-116">Minimum supported client</span></span><br/> | <span data-ttu-id="93365-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93365-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93365-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93365-118">Minimum supported server</span></span><br/> | <span data-ttu-id="93365-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93365-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93365-120">標頭</span><span class="sxs-lookup"><span data-stu-id="93365-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="93365-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="93365-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





