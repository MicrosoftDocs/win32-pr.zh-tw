---
title: 'TTM_GETTITLE 訊息 (Commctrl .h) '
description: 取得工具提示控制項標題的相關資訊。
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- TTM_GETTITLE message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0048925ed3dc267ac07b10b85e2ea1ca1449996c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934394"
---
# <a name="ttm_gettitle-message"></a><span data-ttu-id="fe8b4-104">TTM \_ GETTITLE 訊息</span><span class="sxs-lookup"><span data-stu-id="fe8b4-104">TTM\_GETTITLE message</span></span>

<span data-ttu-id="fe8b4-105">取得工具提示控制項標題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe8b4-105">Retrieve information concerning the title of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe8b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe8b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe8b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe8b4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe8b4-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="fe8b4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fe8b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe8b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe8b4-110">[**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle)結構的指標，其中包含工具提示標題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe8b4-110">Pointer to a [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) structure that contains information about a tooltip title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe8b4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe8b4-111">Return value</span></span>

<span data-ttu-id="fe8b4-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="fe8b4-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe8b4-113">備註</span><span class="sxs-lookup"><span data-stu-id="fe8b4-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fe8b4-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="fe8b4-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="fe8b4-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="fe8b4-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe8b4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe8b4-116">Requirements</span></span>



| <span data-ttu-id="fe8b4-117">需求</span><span class="sxs-lookup"><span data-stu-id="fe8b4-117">Requirement</span></span> | <span data-ttu-id="fe8b4-118">值</span><span class="sxs-lookup"><span data-stu-id="fe8b4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8b4-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe8b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8b4-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe8b4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe8b4-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe8b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8b4-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe8b4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe8b4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fe8b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe8b4-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe8b4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





