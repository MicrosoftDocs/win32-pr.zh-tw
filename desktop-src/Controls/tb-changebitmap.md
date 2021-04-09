---
title: 'TB_CHANGEBITMAP 訊息 (Commctrl .h) '
description: 變更工具列中按鈕的點陣圖。
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP message Windows 控制項
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844455"
---
# <a name="tb_changebitmap-message"></a><span data-ttu-id="9f481-104">TB \_ CHANGEBITMAP 訊息</span><span class="sxs-lookup"><span data-stu-id="9f481-104">TB\_CHANGEBITMAP message</span></span>

<span data-ttu-id="9f481-105">變更工具列中按鈕的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="9f481-105">Changes the bitmap for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f481-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f481-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f481-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f481-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f481-108">要接收新點陣圖之按鈕的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f481-108">Command identifier of the button that is to receive a new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="9f481-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f481-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f481-110">工具列影像清單中影像以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="9f481-110">Zero-based index of an image in the toolbar's image list.</span></span> <span data-ttu-id="9f481-111">系統會在按鈕中顯示指定的影像。</span><span class="sxs-lookup"><span data-stu-id="9f481-111">The system displays the specified image in the button.</span></span> <span data-ttu-id="9f481-112">將此參數設定為 I \_ IMAGECALLBACK，工具列會傳送 [**TBN \_ GETDISPINFO**](tbn-getdispinfo.md) 通知，以在需要時取出影像索引。</span><span class="sxs-lookup"><span data-stu-id="9f481-112">Set this parameter to I\_IMAGECALLBACK, and the toolbar will send the [**TBN\_GETDISPINFO**](tbn-getdispinfo.md) notification to retrieve the image index when it is needed.</span></span>

<span data-ttu-id="9f481-113">[版本 5.81](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="9f481-113">[Version 5.81](common-control-versions.md).</span></span> <span data-ttu-id="9f481-114">將此參數設定為 I \_ IMAGENONE，表示按鈕沒有影像。</span><span class="sxs-lookup"><span data-stu-id="9f481-114">Set this parameter to I\_IMAGENONE to indicate that the button does not have an image.</span></span> <span data-ttu-id="9f481-115">按鈕配置不會包含任何點陣圖的空間，只會包含文字。</span><span class="sxs-lookup"><span data-stu-id="9f481-115">The button layout will not include any space for a bitmap, only text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f481-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f481-116">Return value</span></span>

<span data-ttu-id="9f481-117">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9f481-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f481-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f481-118">Requirements</span></span>



| <span data-ttu-id="9f481-119">需求</span><span class="sxs-lookup"><span data-stu-id="9f481-119">Requirement</span></span> | <span data-ttu-id="9f481-120">值</span><span class="sxs-lookup"><span data-stu-id="9f481-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f481-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f481-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9f481-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f481-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f481-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f481-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9f481-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f481-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f481-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9f481-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f481-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f481-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





