---
title: 'EM_SETPALETTE 訊息 (Richedit .h) '
description: 變更 rich edit 控制項用於顯示視窗的調色板。
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- EM_SETPALETTE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024996"
---
# <a name="em_setpalette-message"></a><span data-ttu-id="80573-104">EM \_ SETPALETTE 訊息</span><span class="sxs-lookup"><span data-stu-id="80573-104">EM\_SETPALETTE message</span></span>

<span data-ttu-id="80573-105">變更 rich edit 控制項用於顯示視窗的調色板。</span><span class="sxs-lookup"><span data-stu-id="80573-105">Changes the palette that a rich edit control uses for its display window.</span></span>

## <a name="parameters"></a><span data-ttu-id="80573-106">參數</span><span class="sxs-lookup"><span data-stu-id="80573-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80573-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80573-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80573-108">Rich edit 控制項所使用之新調色板的控制碼。</span><span class="sxs-lookup"><span data-stu-id="80573-108">Handle to the new palette used by the rich edit control.</span></span>

</dd> <dt>

<span data-ttu-id="80573-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80573-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80573-110">未使用此參數;它必須為零。</span><span class="sxs-lookup"><span data-stu-id="80573-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80573-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="80573-111">Return value</span></span>

<span data-ttu-id="80573-112">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="80573-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80573-113">備註</span><span class="sxs-lookup"><span data-stu-id="80573-113">Remarks</span></span>

<span data-ttu-id="80573-114">Rich edit 控制項不會檢查新的調色板是否有效。</span><span class="sxs-lookup"><span data-stu-id="80573-114">The rich edit control does not check whether the new palette is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="80573-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="80573-115">Requirements</span></span>



| <span data-ttu-id="80573-116">需求</span><span class="sxs-lookup"><span data-stu-id="80573-116">Requirement</span></span> | <span data-ttu-id="80573-117">值</span><span class="sxs-lookup"><span data-stu-id="80573-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80573-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80573-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80573-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80573-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80573-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80573-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80573-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80573-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80573-122">標頭</span><span class="sxs-lookup"><span data-stu-id="80573-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80573-123"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="80573-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





