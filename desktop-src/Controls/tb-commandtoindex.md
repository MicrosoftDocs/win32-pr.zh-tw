---
title: 'TB_COMMANDTOINDEX 訊息 (Commctrl .h) '
description: 針對與指定的命令識別碼相關聯的按鈕，取得以零為基底的索引。
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- TB_COMMANDTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106607"
---
# <a name="tb_commandtoindex-message"></a><span data-ttu-id="e96b6-104">TB \_ COMMANDTOINDEX 訊息</span><span class="sxs-lookup"><span data-stu-id="e96b6-104">TB\_COMMANDTOINDEX message</span></span>

<span data-ttu-id="e96b6-105">針對與指定的命令識別碼相關聯的按鈕，取得以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e96b6-105">Retrieves the zero-based index for the button associated with the specified command identifier.</span></span>

## <a name="parameters"></a><span data-ttu-id="e96b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="e96b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e96b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e96b6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e96b6-108">與按鈕相關聯的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="e96b6-108">Command identifier associated with the button.</span></span>

</dd> <dt>

<span data-ttu-id="e96b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e96b6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e96b6-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="e96b6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e96b6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e96b6-111">Return value</span></span>

<span data-ttu-id="e96b6-112">傳回按鈕的以零為基底的索引，如果指定的命令識別碼無效，則為-1。</span><span class="sxs-lookup"><span data-stu-id="e96b6-112">Returns the zero-based index for the button or -1 if the specified command identifier is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="e96b6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e96b6-113">Requirements</span></span>



| <span data-ttu-id="e96b6-114">需求</span><span class="sxs-lookup"><span data-stu-id="e96b6-114">Requirement</span></span> | <span data-ttu-id="e96b6-115">值</span><span class="sxs-lookup"><span data-stu-id="e96b6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e96b6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e96b6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e96b6-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e96b6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e96b6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e96b6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e96b6-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e96b6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e96b6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e96b6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e96b6-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e96b6-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





