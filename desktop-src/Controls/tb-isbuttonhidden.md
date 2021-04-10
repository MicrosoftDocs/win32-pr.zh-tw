---
title: 'TB_ISBUTTONHIDDEN 訊息 (Commctrl .h) '
description: 決定是否隱藏工具列中指定的按鈕。
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- TB_ISBUTTONHIDDEN message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db36f289a05fecfb2a0795965820324a9ce68057
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935156"
---
# <a name="tb_isbuttonhidden-message"></a><span data-ttu-id="b6258-104">TB \_ ISBUTTONHIDDEN 訊息</span><span class="sxs-lookup"><span data-stu-id="b6258-104">TB\_ISBUTTONHIDDEN message</span></span>

<span data-ttu-id="b6258-105">決定是否隱藏工具列中指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="b6258-105">Determines whether the specified button in a toolbar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6258-106">參數</span><span class="sxs-lookup"><span data-stu-id="b6258-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6258-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6258-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6258-108">按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6258-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="b6258-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6258-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b6258-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b6258-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6258-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6258-111">Return value</span></span>

<span data-ttu-id="b6258-112">如果按鈕是隱藏的，則會傳回非零，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b6258-112">Returns nonzero if the button is hidden, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6258-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6258-113">Requirements</span></span>



| <span data-ttu-id="b6258-114">需求</span><span class="sxs-lookup"><span data-stu-id="b6258-114">Requirement</span></span> | <span data-ttu-id="b6258-115">值</span><span class="sxs-lookup"><span data-stu-id="b6258-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6258-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6258-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b6258-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6258-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6258-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6258-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b6258-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b6258-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6258-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b6258-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6258-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6258-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





