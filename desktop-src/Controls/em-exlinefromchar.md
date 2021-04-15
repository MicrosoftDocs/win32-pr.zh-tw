---
title: 'EM_EXLINEFROMCHAR 訊息 (Richedit .h) '
description: 判斷哪一行在 rich edit 控制項中包含指定的字元。
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- EM_EXLINEFROMCHAR message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467127"
---
# <a name="em_exlinefromchar-message"></a><span data-ttu-id="51fda-104">EM \_ EXLINEFROMCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="51fda-104">EM\_EXLINEFROMCHAR message</span></span>

<span data-ttu-id="51fda-105">判斷哪一行在 rich edit 控制項中包含指定的字元。</span><span class="sxs-lookup"><span data-stu-id="51fda-105">Determines which line contains the specified character in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="51fda-106">參數</span><span class="sxs-lookup"><span data-stu-id="51fda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51fda-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51fda-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51fda-108">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="51fda-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="51fda-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51fda-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51fda-110">以零為基底的字元索引。</span><span class="sxs-lookup"><span data-stu-id="51fda-110">Zero-based index of the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51fda-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="51fda-111">Return value</span></span>

<span data-ttu-id="51fda-112">這則訊息會傳回以零為基底的索引行。</span><span class="sxs-lookup"><span data-stu-id="51fda-112">This message returns the zero-based index of the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fda-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="51fda-113">Requirements</span></span>



| <span data-ttu-id="51fda-114">需求</span><span class="sxs-lookup"><span data-stu-id="51fda-114">Requirement</span></span> | <span data-ttu-id="51fda-115">值</span><span class="sxs-lookup"><span data-stu-id="51fda-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51fda-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51fda-116">Minimum supported client</span></span><br/> | <span data-ttu-id="51fda-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51fda-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51fda-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51fda-118">Minimum supported server</span></span><br/> | <span data-ttu-id="51fda-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51fda-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51fda-120">標頭</span><span class="sxs-lookup"><span data-stu-id="51fda-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="51fda-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="51fda-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





