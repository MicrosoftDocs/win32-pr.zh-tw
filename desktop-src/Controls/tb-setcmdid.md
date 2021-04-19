---
title: 'TB_SETCMDID 訊息 (Commctrl .h) '
description: 設定工具列按鈕的命令識別碼。
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- TB_SETCMDID message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969171"
---
# <a name="tb_setcmdid-message"></a><span data-ttu-id="c1a07-104">TB \_ SETCMDID 訊息</span><span class="sxs-lookup"><span data-stu-id="c1a07-104">TB\_SETCMDID message</span></span>

<span data-ttu-id="c1a07-105">設定工具列按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1a07-105">Sets the command identifier of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1a07-106">參數</span><span class="sxs-lookup"><span data-stu-id="c1a07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1a07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1a07-108">要設定其命令識別碼之按鈕的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="c1a07-108">Zero-based index of the button whose command identifier is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="c1a07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1a07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1a07-110">命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1a07-110">Command identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a07-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1a07-111">Return value</span></span>

<span data-ttu-id="c1a07-112">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c1a07-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a07-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1a07-113">Requirements</span></span>



| <span data-ttu-id="c1a07-114">需求</span><span class="sxs-lookup"><span data-stu-id="c1a07-114">Requirement</span></span> | <span data-ttu-id="c1a07-115">值</span><span class="sxs-lookup"><span data-stu-id="c1a07-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a07-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1a07-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c1a07-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1a07-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1a07-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1a07-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c1a07-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1a07-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1a07-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c1a07-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1a07-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a07-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





