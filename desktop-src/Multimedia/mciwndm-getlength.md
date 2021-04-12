---
title: 'MCIWNDM_GETLENGTH 訊息 (Vfw .h) '
description: MCIWNDM \_ GETLENGTH 訊息會抓取 MCI 裝置目前所使用的內容或檔案的長度。 您可以使用 MCIWndGetLength 宏明確地傳送此訊息。
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464516"
---
# <a name="mciwndm_getlength-message"></a><span data-ttu-id="05d8c-105">MCIWNDM \_ GETLENGTH 訊息</span><span class="sxs-lookup"><span data-stu-id="05d8c-105">MCIWNDM\_GETLENGTH message</span></span>

<span data-ttu-id="05d8c-106">**MCIWNDM \_ GETLENGTH** 訊息會抓取 MCI 裝置目前所使用的內容或檔案的長度。</span><span class="sxs-lookup"><span data-stu-id="05d8c-106">The **MCIWNDM\_GETLENGTH** message retrieves the length of the content or file currently used by an MCI device.</span></span> <span data-ttu-id="05d8c-107">您可以使用 [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="05d8c-107">You can send this message explicitly or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span>


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="05d8c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="05d8c-108">Return Value</span></span>

<span data-ttu-id="05d8c-109">傳回長度。</span><span class="sxs-lookup"><span data-stu-id="05d8c-109">Returns the length.</span></span> <span data-ttu-id="05d8c-110">長度的單位取決於目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="05d8c-110">The units for the length depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="05d8c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="05d8c-111">Requirements</span></span>



| <span data-ttu-id="05d8c-112">需求</span><span class="sxs-lookup"><span data-stu-id="05d8c-112">Requirement</span></span> | <span data-ttu-id="05d8c-113">值</span><span class="sxs-lookup"><span data-stu-id="05d8c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="05d8c-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05d8c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="05d8c-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05d8c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="05d8c-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05d8c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="05d8c-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05d8c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="05d8c-118">標頭</span><span class="sxs-lookup"><span data-stu-id="05d8c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="05d8c-119"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="05d8c-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d8c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05d8c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d8c-121">**MCIWndGetLength**</span><span class="sxs-lookup"><span data-stu-id="05d8c-121">**MCIWndGetLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





