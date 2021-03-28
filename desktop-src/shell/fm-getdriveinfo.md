---
description: 由檔案管理員延伸模組所傳送，可從 [active File Manager] 視窗取出磁片磁碟機資訊。
title: 'FM_GETDRIVEINFO 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991075"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="04f6e-103">FM \_ GETDRIVEINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="04f6e-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="04f6e-104">由檔案管理員延伸模組所傳送，可從 [active File Manager] 視窗取出磁片磁碟機資訊。</span><span class="sxs-lookup"><span data-stu-id="04f6e-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="04f6e-105">參數</span><span class="sxs-lookup"><span data-stu-id="04f6e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f6e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04f6e-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="04f6e-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="04f6e-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="04f6e-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="04f6e-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="04f6e-109">接收磁片磁碟機資訊之 [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="04f6e-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f6e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="04f6e-110">Return value</span></span>

<span data-ttu-id="04f6e-111">傳回非零。</span><span class="sxs-lookup"><span data-stu-id="04f6e-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="04f6e-112">備註</span><span class="sxs-lookup"><span data-stu-id="04f6e-112">Remarks</span></span>

<span data-ttu-id="04f6e-113">如果在 [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md)結構的 **dwTotalSpace** 或 **dwFreeSpace** 成員中傳回0xffffffff，則延伸模組程式庫必須計算值或值。</span><span class="sxs-lookup"><span data-stu-id="04f6e-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f6e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="04f6e-114">Requirements</span></span>



| <span data-ttu-id="04f6e-115">需求</span><span class="sxs-lookup"><span data-stu-id="04f6e-115">Requirement</span></span> | <span data-ttu-id="04f6e-116">值</span><span class="sxs-lookup"><span data-stu-id="04f6e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04f6e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04f6e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="04f6e-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="04f6e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04f6e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="04f6e-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04f6e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="04f6e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="04f6e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="04f6e-122"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="04f6e-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f6e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04f6e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f6e-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="04f6e-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




