---
title: 'RB_GETBANDMARGINS 訊息 (Commctrl .h) '
description: 抓取寬線的邊界。
ms.assetid: 262f4180-53f9-428f-9360-75b762470270
keywords:
- RB_GETBANDMARGINS message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETBANDMARGINS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ab77c057073d9816d1310b1e8cb39fd374956b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934707"
---
# <a name="rb_getbandmargins-message"></a><span data-ttu-id="eebcb-104">RB \_ GETBANDMARGINS 訊息</span><span class="sxs-lookup"><span data-stu-id="eebcb-104">RB\_GETBANDMARGINS message</span></span>

<span data-ttu-id="eebcb-105">抓取寬線的邊界。</span><span class="sxs-lookup"><span data-stu-id="eebcb-105">Retrieves the margins of a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="eebcb-106">參數</span><span class="sxs-lookup"><span data-stu-id="eebcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eebcb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eebcb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eebcb-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="eebcb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eebcb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eebcb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eebcb-110">接收已抓取邊界的 [**邊界**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="eebcb-110">Pointer to a [**MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) structure that receives the retrieved margins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eebcb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="eebcb-111">Return value</span></span>

<span data-ttu-id="eebcb-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="eebcb-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="eebcb-113">備註</span><span class="sxs-lookup"><span data-stu-id="eebcb-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eebcb-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="eebcb-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="eebcb-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="eebcb-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eebcb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="eebcb-116">Requirements</span></span>



| <span data-ttu-id="eebcb-117">需求</span><span class="sxs-lookup"><span data-stu-id="eebcb-117">Requirement</span></span> | <span data-ttu-id="eebcb-118">值</span><span class="sxs-lookup"><span data-stu-id="eebcb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eebcb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eebcb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eebcb-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eebcb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eebcb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eebcb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eebcb-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eebcb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eebcb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="eebcb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eebcb-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="eebcb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





