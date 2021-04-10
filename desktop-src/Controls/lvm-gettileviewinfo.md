---
title: 'LVM_GETTILEVIEWINFO 訊息 (Commctrl .h) '
description: 抓取並排顯示中清單視圖控制項的相關資訊。
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- LVM_GETTILEVIEWINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe1f34da560d539a9ae12cc7a065b2bf37bc3c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686278"
---
# <a name="lvm_gettileviewinfo-message"></a><span data-ttu-id="eb652-104">LVM \_ GETTILEVIEWINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="eb652-104">LVM\_GETTILEVIEWINFO message</span></span>

<span data-ttu-id="eb652-105">抓取並排顯示中清單視圖控制項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb652-105">Retrieves information about a list-view control in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb652-106">參數</span><span class="sxs-lookup"><span data-stu-id="eb652-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb652-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb652-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eb652-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="eb652-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eb652-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb652-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eb652-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a>結構的指標，此結構會接收抓取的資訊。</span><span class="sxs-lookup"><span data-stu-id="eb652-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb652-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb652-111">Return value</span></span>

<span data-ttu-id="eb652-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="eb652-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb652-113">備註</span><span class="sxs-lookup"><span data-stu-id="eb652-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eb652-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="eb652-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="eb652-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="eb652-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb652-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb652-116">Requirements</span></span>



| <span data-ttu-id="eb652-117">需求</span><span class="sxs-lookup"><span data-stu-id="eb652-117">Requirement</span></span> | <span data-ttu-id="eb652-118">值</span><span class="sxs-lookup"><span data-stu-id="eb652-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb652-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb652-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb652-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb652-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb652-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb652-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb652-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb652-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb652-123">標頭</span><span class="sxs-lookup"><span data-stu-id="eb652-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb652-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb652-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





