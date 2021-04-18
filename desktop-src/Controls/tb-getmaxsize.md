---
title: 'TB_GETMAXSIZE 訊息 (Commctrl .h) '
description: 抓取工具列中所有可見按鈕和分隔符號的總大小。
ms.assetid: 560e6ce2-00ef-46c3-b1d8-fbe0ac79c888
keywords:
- TB_GETMAXSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETMAXSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4829e65d90c04181369dd73b9c54634f1077144
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965103"
---
# <a name="tb_getmaxsize-message"></a><span data-ttu-id="3bf4f-104">TB \_ GETMAXSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="3bf4f-104">TB\_GETMAXSIZE message</span></span>

<span data-ttu-id="3bf4f-105">抓取工具列中所有可見按鈕和分隔符號的總大小。</span><span class="sxs-lookup"><span data-stu-id="3bf4f-105">Retrieves the total size of all of the visible buttons and separators in the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3bf4f-106">參數</span><span class="sxs-lookup"><span data-stu-id="3bf4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bf4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3bf4f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3bf4f-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="3bf4f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3bf4f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3bf4f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bf4f-110">接收專案大小的 [**大小**](/previous-versions//dd145106(v=vs.85)) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="3bf4f-110">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the size of the items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bf4f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bf4f-111">Return value</span></span>

<span data-ttu-id="3bf4f-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="3bf4f-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf4f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bf4f-113">Requirements</span></span>



| <span data-ttu-id="3bf4f-114">需求</span><span class="sxs-lookup"><span data-stu-id="3bf4f-114">Requirement</span></span> | <span data-ttu-id="3bf4f-115">值</span><span class="sxs-lookup"><span data-stu-id="3bf4f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf4f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bf4f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3bf4f-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bf4f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3bf4f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bf4f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3bf4f-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bf4f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3bf4f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3bf4f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bf4f-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bf4f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

