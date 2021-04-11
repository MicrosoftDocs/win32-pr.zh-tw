---
title: 'LVM_GETSELECTEDCOLUMN 訊息 (Commctrl .h) '
description: 抓取指定所選資料行的整數。
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- LVM_GETSELECTEDCOLUMN message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ffae9a9c7812f025241f5b46f3b1ea61bb88bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317376"
---
# <a name="lvm_getselectedcolumn-message"></a><span data-ttu-id="6c51b-104">LVM \_ GETSELECTEDCOLUMN 訊息</span><span class="sxs-lookup"><span data-stu-id="6c51b-104">LVM\_GETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="6c51b-105">抓取指定所選資料行的整數。</span><span class="sxs-lookup"><span data-stu-id="6c51b-105">Retrieves an integer that specifies the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c51b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c51b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c51b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c51b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6c51b-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6c51b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6c51b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c51b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6c51b-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6c51b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c51b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c51b-111">Return value</span></span>

<span data-ttu-id="6c51b-112">傳回指定所選資料行的 **UINT** 。</span><span class="sxs-lookup"><span data-stu-id="6c51b-112">Returns an **UINT** that specifies the selected column.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c51b-113">備註</span><span class="sxs-lookup"><span data-stu-id="6c51b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6c51b-114">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="6c51b-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6c51b-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="6c51b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c51b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c51b-116">Requirements</span></span>



| <span data-ttu-id="6c51b-117">需求</span><span class="sxs-lookup"><span data-stu-id="6c51b-117">Requirement</span></span> | <span data-ttu-id="6c51b-118">值</span><span class="sxs-lookup"><span data-stu-id="6c51b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c51b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c51b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6c51b-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c51b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c51b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c51b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6c51b-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c51b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c51b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6c51b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c51b-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c51b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





