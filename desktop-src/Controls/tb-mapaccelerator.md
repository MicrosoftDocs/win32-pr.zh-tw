---
title: 'TB_MAPACCELERATOR 訊息 (Commctrl .h) '
description: 判斷對應至指定快速鍵的按鈕識別碼。
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR message Windows 控制項
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686197"
---
# <a name="tb_mapaccelerator-message"></a><span data-ttu-id="e9c0b-104">TB \_ MAPACCELERATOR 訊息</span><span class="sxs-lookup"><span data-stu-id="e9c0b-104">TB\_MAPACCELERATOR message</span></span>

<span data-ttu-id="e9c0b-105">判斷對應至指定快速鍵的按鈕識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9c0b-105">Determines the ID of the button that corresponds to the specified accelerator character.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9c0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9c0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c0b-107">*wParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9c0b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c0b-108">快速鍵字元。</span><span class="sxs-lookup"><span data-stu-id="e9c0b-108">The accelerator character.</span></span>

</dd> <dt>

<span data-ttu-id="e9c0b-109">*lParam* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9c0b-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c0b-110">**UINT** 的指標。</span><span class="sxs-lookup"><span data-stu-id="e9c0b-110">Pointer to a **UINT**.</span></span> <span data-ttu-id="e9c0b-111">傳回時，如果成功，此參數將會保留 *wParam* 為其快速鍵的按鈕的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9c0b-111">On return, if successful, this parameter will hold the id of the button that has *wParam* as its accelerator character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9c0b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9c0b-112">Return value</span></span>

<span data-ttu-id="e9c0b-113">如果其中一個按鈕的 *wParam* 為其快速鍵，則會傳回非零值，否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e9c0b-113">Returns a nonzero value if one of the buttons has *wParam* as its accelerator character, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c0b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9c0b-114">Requirements</span></span>



| <span data-ttu-id="e9c0b-115">需求</span><span class="sxs-lookup"><span data-stu-id="e9c0b-115">Requirement</span></span> | <span data-ttu-id="e9c0b-116">值</span><span class="sxs-lookup"><span data-stu-id="e9c0b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c0b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9c0b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c0b-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9c0b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9c0b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9c0b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c0b-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9c0b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9c0b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e9c0b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c0b-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c0b-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e9c0b-123">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="e9c0b-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9c0b-124">**TB \_MAPACCELERATORW** (Unicode) 和 **TB \_ MAPACCELERATORA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="e9c0b-124">**TB\_MAPACCELERATORW** (Unicode) and **TB\_MAPACCELERATORA** (ANSI)</span></span><br/>       |



 

 





