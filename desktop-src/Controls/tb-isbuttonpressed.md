---
title: 'TB_ISBUTTONPRESSED 訊息 (Commctrl .h) '
description: 決定是否按下工具列中指定的按鈕。
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- TB_ISBUTTONPRESSED message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc2e6ec7b56ce205f3d89bc22a7c9dbbee90b1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094175"
---
# <a name="tb_isbuttonpressed-message"></a><span data-ttu-id="03065-104">TB \_ ISBUTTONPRESSED 訊息</span><span class="sxs-lookup"><span data-stu-id="03065-104">TB\_ISBUTTONPRESSED message</span></span>

<span data-ttu-id="03065-105">決定是否按下工具列中指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="03065-105">Determines whether the specified button in a toolbar is pressed.</span></span>

## <a name="parameters"></a><span data-ttu-id="03065-106">參數</span><span class="sxs-lookup"><span data-stu-id="03065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03065-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03065-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03065-108">按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="03065-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="03065-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03065-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="03065-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="03065-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03065-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="03065-111">Return value</span></span>

<span data-ttu-id="03065-112">如果已按下按鈕，則傳回非零，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="03065-112">Returns nonzero if the button is pressed, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="03065-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="03065-113">Requirements</span></span>



| <span data-ttu-id="03065-114">需求</span><span class="sxs-lookup"><span data-stu-id="03065-114">Requirement</span></span> | <span data-ttu-id="03065-115">值</span><span class="sxs-lookup"><span data-stu-id="03065-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03065-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03065-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03065-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03065-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03065-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03065-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03065-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03065-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03065-120">標頭</span><span class="sxs-lookup"><span data-stu-id="03065-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="03065-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="03065-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





