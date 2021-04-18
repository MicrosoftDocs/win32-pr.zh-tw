---
title: 'MCIWNDM_GETALIAS 訊息 (Vfw .h) '
description: MCIWNDM \_ GETALIAS 訊息會抓取用來開啟 MCI 裝置或具有 mciSendString 功能之檔案的別名。 您可以使用 MCIWndGetAlias 宏明確地傳送此訊息。
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e971c50b9abc450387ac29f9a7331bfdca5c38c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965064"
---
# <a name="mciwndm_getalias-message"></a><span data-ttu-id="b99e9-105">MCIWNDM \_ GETALIAS 訊息</span><span class="sxs-lookup"><span data-stu-id="b99e9-105">MCIWNDM\_GETALIAS message</span></span>

<span data-ttu-id="b99e9-106">**MCIWNDM \_ GETALIAS** 訊息會抓取用來開啟 MCI 裝置或具有 [**mciSendString**](/previous-versions//dd757161(v=vs.85))功能之檔案的別名。</span><span class="sxs-lookup"><span data-stu-id="b99e9-106">The **MCIWNDM\_GETALIAS** message retrieves the alias used to open an MCI device or file with the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="b99e9-107">您可以使用 [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="b99e9-107">You can send this message explicitly or by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span>


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="b99e9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b99e9-108">Return Value</span></span>

<span data-ttu-id="b99e9-109">傳回裝置別名。</span><span class="sxs-lookup"><span data-stu-id="b99e9-109">Returns the device alias.</span></span>

## <a name="requirements"></a><span data-ttu-id="b99e9-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="b99e9-110">Requirements</span></span>



| <span data-ttu-id="b99e9-111">需求</span><span class="sxs-lookup"><span data-stu-id="b99e9-111">Requirement</span></span> | <span data-ttu-id="b99e9-112">值</span><span class="sxs-lookup"><span data-stu-id="b99e9-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b99e9-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b99e9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b99e9-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b99e9-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b99e9-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b99e9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b99e9-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b99e9-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b99e9-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b99e9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b99e9-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="b99e9-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b99e9-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b99e9-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="b99e9-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b99e9-120">[**mciSendString**](/previous-versions//dd757161(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b99e9-121">**MCIWndGetAlias**</span><span class="sxs-lookup"><span data-stu-id="b99e9-121">**MCIWndGetAlias**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

