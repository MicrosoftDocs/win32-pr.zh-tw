---
description: 當檔案管理員卸載 DLL 時，傳送至擴充 DLL。
title: 'FMEVENT_UNLOAD 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 140fbdc79980a2ab6ba9f50b8815429436df0d3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111748"
---
# <a name="fmevent_unload-message"></a><span data-ttu-id="9f035-103">FMEVENT 卸載 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="9f035-103">FMEVENT\_UNLOAD message</span></span>

<span data-ttu-id="9f035-104">當檔案管理員卸載 DLL 時，傳送至擴充 DLL。</span><span class="sxs-lookup"><span data-stu-id="9f035-104">Sent to an extension DLL when File Manager is unloading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f035-105">參數</span><span class="sxs-lookup"><span data-stu-id="9f035-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f035-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f035-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9f035-107">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9f035-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9f035-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f035-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9f035-109">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9f035-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f035-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f035-110">Return value</span></span>

<span data-ttu-id="9f035-111">如果延伸模組 DLL 處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="9f035-111">An extension DLL should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f035-112">備註</span><span class="sxs-lookup"><span data-stu-id="9f035-112">Remarks</span></span>

<span data-ttu-id="9f035-113">在傳送此訊息時，與 [**FMEVENT \_ LOAD**](fmevent-load.md)和 [**FMEVENT \_ INITMENU**](fmevent-initmenu.md)訊息一起傳遞的 *hwnd* 和 **hMenu** 值可能無效。</span><span class="sxs-lookup"><span data-stu-id="9f035-113">The *hwnd* and **hMenu** values passed with the [**FMEVENT\_LOAD**](fmevent-load.md) and [**FMEVENT\_INITMENU**](fmevent-initmenu.md) messages may not be valid at the time this message is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f035-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f035-114">Requirements</span></span>



| <span data-ttu-id="9f035-115">需求</span><span class="sxs-lookup"><span data-stu-id="9f035-115">Requirement</span></span> | <span data-ttu-id="9f035-116">值</span><span class="sxs-lookup"><span data-stu-id="9f035-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f035-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f035-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f035-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f035-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9f035-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f035-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f035-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f035-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9f035-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9f035-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f035-122"><dt>Wfext。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f035-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f035-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f035-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f035-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="9f035-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




