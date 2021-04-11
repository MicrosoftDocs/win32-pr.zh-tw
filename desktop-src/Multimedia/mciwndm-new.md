---
title: 'MCIWNDM_NEW 訊息 (Vfw .h) '
description: MCIWNDM \_ NEW message 會為目前的 MCI 裝置建立新的檔案。 您可以使用 MCIWndNew 宏明確地傳送此訊息。
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685823"
---
# <a name="mciwndm_new-message"></a><span data-ttu-id="dbf7c-105">MCIWNDM \_ 新訊息</span><span class="sxs-lookup"><span data-stu-id="dbf7c-105">MCIWNDM\_NEW message</span></span>

<span data-ttu-id="dbf7c-106">**MCIWNDM \_ NEW** message 會為目前的 MCI 裝置建立新的檔案。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-106">The **MCIWNDM\_NEW** message creates a new file for the current MCI device.</span></span> <span data-ttu-id="dbf7c-107">您可以使用 [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-107">You can send this message explicitly or by using the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro.</span></span>


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="dbf7c-108">參數</span><span class="sxs-lookup"><span data-stu-id="dbf7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf7c-109"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="dbf7c-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="dbf7c-110">緩衝區的指標，其中包含將使用該檔案之 MCI 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-110">Pointer to a buffer containing the name of the MCI device that will use the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf7c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbf7c-111">Return Value</span></span>

<span data-ttu-id="dbf7c-112">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="dbf7c-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf7c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbf7c-113">Requirements</span></span>



| <span data-ttu-id="dbf7c-114">需求</span><span class="sxs-lookup"><span data-stu-id="dbf7c-114">Requirement</span></span> | <span data-ttu-id="dbf7c-115">值</span><span class="sxs-lookup"><span data-stu-id="dbf7c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dbf7c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbf7c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dbf7c-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbf7c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dbf7c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbf7c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dbf7c-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbf7c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dbf7c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="dbf7c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbf7c-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf7c-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf7c-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbf7c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf7c-123">**MCIWndNew**</span><span class="sxs-lookup"><span data-stu-id="dbf7c-123">**MCIWndNew**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





