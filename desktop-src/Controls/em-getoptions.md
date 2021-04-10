---
title: 'EM_GETOPTIONS 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項選項。
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- EM_GETOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934729"
---
# <a name="em_getoptions-message"></a><span data-ttu-id="d10e4-104">EM \_ GETOPTIONS 訊息</span><span class="sxs-lookup"><span data-stu-id="d10e4-104">EM\_GETOPTIONS message</span></span>

<span data-ttu-id="d10e4-105">抓取 rich edit 控制項選項。</span><span class="sxs-lookup"><span data-stu-id="d10e4-105">Retrieves rich edit control options.</span></span>

## <a name="parameters"></a><span data-ttu-id="d10e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="d10e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d10e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d10e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d10e4-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="d10e4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d10e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d10e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d10e4-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="d10e4-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d10e4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d10e4-111">Return value</span></span>

<span data-ttu-id="d10e4-112">此訊息會傳回 [**EM \_ >setoptions**](em-setoptions.md) 訊息中所述之目前選項旗標值的組合。</span><span class="sxs-lookup"><span data-stu-id="d10e4-112">This message returns a combination of the current option flag values described in the [**EM\_SETOPTIONS**](em-setoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10e4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d10e4-113">Requirements</span></span>



| <span data-ttu-id="d10e4-114">需求</span><span class="sxs-lookup"><span data-stu-id="d10e4-114">Requirement</span></span> | <span data-ttu-id="d10e4-115">值</span><span class="sxs-lookup"><span data-stu-id="d10e4-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d10e4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d10e4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d10e4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d10e4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d10e4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d10e4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d10e4-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d10e4-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d10e4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d10e4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d10e4-121"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d10e4-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10e4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d10e4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10e4-123">**EM \_ >SETOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="d10e4-123">**EM\_SETOPTIONS**</span></span>](em-setoptions.md)
</dt> </dl>

 

 





