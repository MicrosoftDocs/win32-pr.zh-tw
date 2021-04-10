---
title: 'LVM_GETOUTLINECOLOR 訊息 (Commctrl .h) '
description: 如果 \_ \_ 已設定 lvs) EX BORDERSELECT 擴充視窗樣式，則抓取清單視圖控制項框線的色彩。
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- LVM_GETOUTLINECOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844095"
---
# <a name="lvm_getoutlinecolor-message"></a><span data-ttu-id="592cb-104">LVM \_ GETOUTLINECOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="592cb-104">LVM\_GETOUTLINECOLOR message</span></span>

<span data-ttu-id="592cb-105">如果已設定 [**lvs) \_ EX \_ BORDERSELECT**](extended-list-view-styles.md) 擴充視窗樣式，則抓取清單視圖控制項框線的色彩。</span><span class="sxs-lookup"><span data-stu-id="592cb-105">Retrieves the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="592cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="592cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="592cb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="592cb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="592cb-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="592cb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="592cb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="592cb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="592cb-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="592cb-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="592cb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="592cb-111">Return value</span></span>

<span data-ttu-id="592cb-112">傳回 **COLORREF** 結構，其中包含清單視圖控制項框線的色彩。</span><span class="sxs-lookup"><span data-stu-id="592cb-112">Returns a **COLORREF** structure that contains the color of the border of a list-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="592cb-113">備註</span><span class="sxs-lookup"><span data-stu-id="592cb-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="592cb-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="592cb-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="592cb-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="592cb-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="592cb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="592cb-116">Requirements</span></span>



| <span data-ttu-id="592cb-117">需求</span><span class="sxs-lookup"><span data-stu-id="592cb-117">Requirement</span></span> | <span data-ttu-id="592cb-118">值</span><span class="sxs-lookup"><span data-stu-id="592cb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="592cb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="592cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="592cb-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="592cb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="592cb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="592cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="592cb-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="592cb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="592cb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="592cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="592cb-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="592cb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





