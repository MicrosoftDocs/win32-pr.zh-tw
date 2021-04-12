---
title: 'CCM_GETUNICODEFORMAT 訊息 (Commctrl .h) '
description: 取得控制項的 Unicode 字元格式旗標。
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- CCM_GETUNICODEFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d49ccc57faa05e86d12df130b12ce3d542bf6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104514"
---
# <a name="ccm_getunicodeformat-message"></a><span data-ttu-id="26504-104">CCM \_ GETUNICODEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="26504-104">CCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="26504-105">取得控制項的 Unicode 字元格式旗標。</span><span class="sxs-lookup"><span data-stu-id="26504-105">Gets the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="26504-106">參數</span><span class="sxs-lookup"><span data-stu-id="26504-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26504-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26504-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="26504-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="26504-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="26504-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26504-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="26504-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="26504-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26504-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="26504-111">Return value</span></span>

<span data-ttu-id="26504-112">傳回控制項的 Unicode 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="26504-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="26504-113">如果這個值為非零值，則控制項會使用 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="26504-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="26504-114">如果這個值為零，則控制項會使用 ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="26504-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="26504-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="26504-115">Requirements</span></span>



| <span data-ttu-id="26504-116">需求</span><span class="sxs-lookup"><span data-stu-id="26504-116">Requirement</span></span> | <span data-ttu-id="26504-117">值</span><span class="sxs-lookup"><span data-stu-id="26504-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26504-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26504-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26504-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26504-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26504-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26504-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26504-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26504-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26504-122">標頭</span><span class="sxs-lookup"><span data-stu-id="26504-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="26504-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="26504-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26504-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26504-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26504-125">**CCM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="26504-125">**CCM\_SETUNICODEFORMAT**</span></span>](ccm-setunicodeformat.md)
</dt> </dl>

 

 





