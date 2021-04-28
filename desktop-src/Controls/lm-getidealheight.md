---
title: 'LM_GETIDEALHEIGHT 訊息 (Commctrl .h) '
description: LM_GETIDEALHEIGHT 訊息-針對控制項目前寬度的連結，取得其慣用高度。
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- LM_GETIDEALHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6e82f259124e6da285ed2357d48ca07d5f8c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112396"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="590c7-104">LM \_ GETIDEALHEIGHT 訊息</span><span class="sxs-lookup"><span data-stu-id="590c7-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="590c7-105">抓取控制項目前寬度之連結的慣用高度。</span><span class="sxs-lookup"><span data-stu-id="590c7-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="590c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="590c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="590c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="590c7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="590c7-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="590c7-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="590c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="590c7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="590c7-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="590c7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="590c7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="590c7-111">Return value</span></span>

<span data-ttu-id="590c7-112">整數，表示連結文字的慣用高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="590c7-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="590c7-113">備註</span><span class="sxs-lookup"><span data-stu-id="590c7-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="590c7-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="590c7-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="590c7-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="590c7-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="590c7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="590c7-116">Requirements</span></span>



| <span data-ttu-id="590c7-117">需求</span><span class="sxs-lookup"><span data-stu-id="590c7-117">Requirement</span></span> | <span data-ttu-id="590c7-118">值</span><span class="sxs-lookup"><span data-stu-id="590c7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="590c7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="590c7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="590c7-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="590c7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="590c7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="590c7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="590c7-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="590c7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="590c7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="590c7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="590c7-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="590c7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





