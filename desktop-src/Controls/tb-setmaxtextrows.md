---
title: 'TB_SETMAXTEXTROWS 訊息 (Commctrl .h) '
description: 設定工具列按鈕上顯示之文字資料列的最大數目。
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934094"
---
# <a name="tb_setmaxtextrows-message"></a><span data-ttu-id="c4a94-104">TB \_ SETMAXTEXTROWS 訊息</span><span class="sxs-lookup"><span data-stu-id="c4a94-104">TB\_SETMAXTEXTROWS message</span></span>

<span data-ttu-id="c4a94-105">設定工具列按鈕上顯示之文字資料列的最大數目。</span><span class="sxs-lookup"><span data-stu-id="c4a94-105">Sets the maximum number of text rows displayed on a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4a94-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4a94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a94-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4a94-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4a94-108">可顯示之文字的最大資料列數。</span><span class="sxs-lookup"><span data-stu-id="c4a94-108">Maximum number of rows of text that can be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="c4a94-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4a94-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c4a94-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="c4a94-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4a94-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4a94-111">Return value</span></span>

<span data-ttu-id="c4a94-112">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="c4a94-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4a94-113">備註</span><span class="sxs-lookup"><span data-stu-id="c4a94-113">Remarks</span></span>

<span data-ttu-id="c4a94-114">若要讓文字換行，您必須藉由傳送 [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) 訊息來設定最大按鈕寬度。</span><span class="sxs-lookup"><span data-stu-id="c4a94-114">To cause text to wrap, you must set the maximum button width by sending a [**TB\_SETBUTTONWIDTH**](tb-setbuttonwidth.md) message.</span></span> <span data-ttu-id="c4a94-115">文字會在字組分隔處換行;\\文字中的 "n" )  ( 的分行符號會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c4a94-115">The text wraps at a word break; line breaks ("\\n") in the text are ignored.</span></span> <span data-ttu-id="c4a94-116">TBSTYLE 清單工具列中的文字 \_ 一律會顯示在同一行上。</span><span class="sxs-lookup"><span data-stu-id="c4a94-116">Text in TBSTYLE\_LIST toolbars is always shown on a single line.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a94-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4a94-117">Requirements</span></span>



| <span data-ttu-id="c4a94-118">需求</span><span class="sxs-lookup"><span data-stu-id="c4a94-118">Requirement</span></span> | <span data-ttu-id="c4a94-119">值</span><span class="sxs-lookup"><span data-stu-id="c4a94-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a94-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4a94-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a94-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4a94-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4a94-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4a94-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a94-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4a94-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4a94-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c4a94-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4a94-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4a94-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





