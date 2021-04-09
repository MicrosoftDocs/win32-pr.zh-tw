---
title: 'UDM_SETBASE 訊息 (Commctrl .h) '
description: 設定上下按鈕控制項的基本基底。 基底值會決定合作者視窗是否以十進位或十六進位數字顯示數位。 十六進位數位一律不帶正負號，而且會簽署十進位數。
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934700"
---
# <a name="udm_setbase-message"></a><span data-ttu-id="de540-106">UDM \_ SETBASE 訊息</span><span class="sxs-lookup"><span data-stu-id="de540-106">UDM\_SETBASE message</span></span>

<span data-ttu-id="de540-107">設定上下按鈕控制項的基本基底。</span><span class="sxs-lookup"><span data-stu-id="de540-107">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="de540-108">基底值會決定合作者視窗是否以十進位或十六進位數字顯示數位。</span><span class="sxs-lookup"><span data-stu-id="de540-108">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="de540-109">十六進位數位一律不帶正負號，而且會簽署十進位數。</span><span class="sxs-lookup"><span data-stu-id="de540-109">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span>

## <a name="parameters"></a><span data-ttu-id="de540-110">參數</span><span class="sxs-lookup"><span data-stu-id="de540-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de540-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de540-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de540-112">控制項的新基底值。</span><span class="sxs-lookup"><span data-stu-id="de540-112">New base value for the control.</span></span> <span data-ttu-id="de540-113">針對十六進位，此參數可以是十進位或16的10。</span><span class="sxs-lookup"><span data-stu-id="de540-113">This parameter can be 10 for decimal or 16 for hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="de540-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de540-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="de540-115">必須為零。</span><span class="sxs-lookup"><span data-stu-id="de540-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de540-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="de540-116">Return value</span></span>

<span data-ttu-id="de540-117">傳回值是先前的基底值。</span><span class="sxs-lookup"><span data-stu-id="de540-117">The return value is the previous base value.</span></span> <span data-ttu-id="de540-118">如果指定了不正確基底，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="de540-118">If an invalid base is given, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="de540-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="de540-119">Requirements</span></span>



| <span data-ttu-id="de540-120">需求</span><span class="sxs-lookup"><span data-stu-id="de540-120">Requirement</span></span> | <span data-ttu-id="de540-121">值</span><span class="sxs-lookup"><span data-stu-id="de540-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de540-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de540-122">Minimum supported client</span></span><br/> | <span data-ttu-id="de540-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de540-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de540-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de540-124">Minimum supported server</span></span><br/> | <span data-ttu-id="de540-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de540-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de540-126">標頭</span><span class="sxs-lookup"><span data-stu-id="de540-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="de540-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="de540-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





