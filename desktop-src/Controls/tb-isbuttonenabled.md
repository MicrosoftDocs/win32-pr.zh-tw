---
title: 'TB_ISBUTTONENABLED 訊息 (Commctrl .h) '
description: 判斷是否已啟用工具列中指定的按鈕。
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- TB_ISBUTTONENABLED message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647d158f0e19ce9dc110a475990cfcc9deff770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843348"
---
# <a name="tb_isbuttonenabled-message"></a><span data-ttu-id="0fa07-104">TB \_ ISBUTTONENABLED 訊息</span><span class="sxs-lookup"><span data-stu-id="0fa07-104">TB\_ISBUTTONENABLED message</span></span>

<span data-ttu-id="0fa07-105">判斷是否已啟用工具列中指定的按鈕。</span><span class="sxs-lookup"><span data-stu-id="0fa07-105">Determines whether the specified button in a toolbar is enabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fa07-106">參數</span><span class="sxs-lookup"><span data-stu-id="0fa07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fa07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fa07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fa07-108">按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="0fa07-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="0fa07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fa07-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0fa07-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0fa07-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fa07-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fa07-111">Return value</span></span>

<span data-ttu-id="0fa07-112">如果按鈕已啟用，則傳回非零，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0fa07-112">Returns nonzero if the button is enabled, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fa07-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fa07-113">Requirements</span></span>



| <span data-ttu-id="0fa07-114">需求</span><span class="sxs-lookup"><span data-stu-id="0fa07-114">Requirement</span></span> | <span data-ttu-id="0fa07-115">值</span><span class="sxs-lookup"><span data-stu-id="0fa07-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa07-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fa07-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0fa07-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fa07-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fa07-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0fa07-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fa07-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fa07-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0fa07-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fa07-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fa07-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





