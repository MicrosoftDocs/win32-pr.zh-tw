---
title: 'TB_AUTOSIZE 訊息 (Commctrl .h) '
description: 使工具列調整大小。
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- TB_AUTOSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509490"
---
# <a name="tb_autosize-message"></a><span data-ttu-id="67426-104">TB 自動 \_ 調整訊息</span><span class="sxs-lookup"><span data-stu-id="67426-104">TB\_AUTOSIZE message</span></span>

<span data-ttu-id="67426-105">使工具列調整大小。</span><span class="sxs-lookup"><span data-stu-id="67426-105">Causes a toolbar to be resized.</span></span>

## <a name="parameters"></a><span data-ttu-id="67426-106">參數</span><span class="sxs-lookup"><span data-stu-id="67426-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67426-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67426-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="67426-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67426-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="67426-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67426-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="67426-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="67426-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67426-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="67426-111">Return value</span></span>

<span data-ttu-id="67426-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="67426-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67426-113">備註</span><span class="sxs-lookup"><span data-stu-id="67426-113">Remarks</span></span>

<span data-ttu-id="67426-114">應用程式會在透過設定按鈕或點陣圖大小或第一次加入字串，而導致工具列的大小變更時，傳送 TB 的自動 **\_ 調整** 訊息。</span><span class="sxs-lookup"><span data-stu-id="67426-114">An application sends the **TB\_AUTOSIZE** message after causing the size of a toolbar to change either by setting the button or bitmap size or by adding strings for the first time.</span></span>

## <a name="requirements"></a><span data-ttu-id="67426-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="67426-115">Requirements</span></span>



| <span data-ttu-id="67426-116">需求</span><span class="sxs-lookup"><span data-stu-id="67426-116">Requirement</span></span> | <span data-ttu-id="67426-117">值</span><span class="sxs-lookup"><span data-stu-id="67426-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67426-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67426-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67426-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67426-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67426-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67426-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67426-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67426-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67426-122">標頭</span><span class="sxs-lookup"><span data-stu-id="67426-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67426-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="67426-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





