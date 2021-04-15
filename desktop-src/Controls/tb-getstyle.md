---
title: 'TB_GETSTYLE 訊息 (Commctrl .h) '
description: 抓取工具列控制項目前使用的樣式。
ms.assetid: 6fbe8733-79df-462e-acb6-6568105e5058
keywords:
- TB_GETSTYLE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8de0addae729a4a8c641d21fd1771137d8c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466321"
---
# <a name="tb_getstyle-message"></a><span data-ttu-id="0fb3b-104">TB \_ GETSTYLE 訊息</span><span class="sxs-lookup"><span data-stu-id="0fb3b-104">TB\_GETSTYLE message</span></span>

<span data-ttu-id="0fb3b-105">抓取工具列控制項目前使用的樣式。</span><span class="sxs-lookup"><span data-stu-id="0fb3b-105">Retrieves the styles currently in use for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fb3b-106">參數</span><span class="sxs-lookup"><span data-stu-id="0fb3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb3b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fb3b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0fb3b-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0fb3b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0fb3b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fb3b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0fb3b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0fb3b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb3b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fb3b-111">Return value</span></span>

<span data-ttu-id="0fb3b-112">傳回以 [工具列控制項樣式](toolbar-control-and-button-styles.md)組合的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="0fb3b-112">Returns a **DWORD** value that is a combination of [toolbar control styles](toolbar-control-and-button-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb3b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fb3b-113">Requirements</span></span>



| <span data-ttu-id="0fb3b-114">需求</span><span class="sxs-lookup"><span data-stu-id="0fb3b-114">Requirement</span></span> | <span data-ttu-id="0fb3b-115">值</span><span class="sxs-lookup"><span data-stu-id="0fb3b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb3b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fb3b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb3b-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fb3b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fb3b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fb3b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb3b-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fb3b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fb3b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0fb3b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fb3b-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb3b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





