---
title: 'LVM_GETGROUPINFO 訊息 (Commctrl .h) '
description: 取得群組資訊。
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024929"
---
# <a name="lvm_getgroupinfo-message"></a><span data-ttu-id="d6ce1-104">LVM \_ GETGROUPINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="d6ce1-104">LVM\_GETGROUPINFO message</span></span>

<span data-ttu-id="d6ce1-105">取得群組資訊。</span><span class="sxs-lookup"><span data-stu-id="d6ce1-105">Gets group information.</span></span>

## <a name="parameters"></a><span data-ttu-id="d6ce1-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6ce1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6ce1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6ce1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d6ce1-108">識別碼，指定要抓取其資訊的群組。</span><span class="sxs-lookup"><span data-stu-id="d6ce1-108">An ID that specifies the group whose information is retrieved.</span></span></dd> <dt>

<span data-ttu-id="d6ce1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6ce1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d6ce1-110"><a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a>結構的指標，此結構會接收抓取的資訊。</span><span class="sxs-lookup"><span data-stu-id="d6ce1-110">A pointer an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that receives the retrieved information.</span></span> <span data-ttu-id="d6ce1-111">將此結構的 **cbSize** 成員設定為 SIZEOF (LVGROUP) 。</span><span class="sxs-lookup"><span data-stu-id="d6ce1-111">Set the **cbSize** member of this structure to sizeof(LVGROUP).</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6ce1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6ce1-112">Return value</span></span>

<span data-ttu-id="d6ce1-113">如果成功，則傳回群組的識別碼，否則為-1。</span><span class="sxs-lookup"><span data-stu-id="d6ce1-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6ce1-114">備註</span><span class="sxs-lookup"><span data-stu-id="d6ce1-114">Remarks</span></span>

<span data-ttu-id="d6ce1-115">嘗試取得群組的標頭之前，請先確定群組沒有 LBGS \_ NOHEADER 樣式。</span><span class="sxs-lookup"><span data-stu-id="d6ce1-115">Before attempting to retrieve the header for a group, first ensure that the group does not have the LBGS\_NOHEADER style.</span></span>

> [!Note]  
> <span data-ttu-id="d6ce1-116">若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="d6ce1-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d6ce1-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d6ce1-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6ce1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6ce1-118">Requirements</span></span>



| <span data-ttu-id="d6ce1-119">需求</span><span class="sxs-lookup"><span data-stu-id="d6ce1-119">Requirement</span></span> | <span data-ttu-id="d6ce1-120">值</span><span class="sxs-lookup"><span data-stu-id="d6ce1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ce1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6ce1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ce1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6ce1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d6ce1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6ce1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ce1-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6ce1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6ce1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d6ce1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6ce1-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d6ce1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





