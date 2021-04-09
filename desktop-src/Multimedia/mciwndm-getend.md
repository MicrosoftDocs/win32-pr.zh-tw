---
title: 'MCIWNDM_GETEND 訊息 (Vfw .h) '
description: MCIWNDM \_ GETEND 訊息會抓取 MCI 裝置或檔案的內容結尾位置。 您可以使用 MCIWndGetEnd 宏明確地傳送此訊息。
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844224"
---
# <a name="mciwndm_getend-message"></a><span data-ttu-id="2c96e-105">MCIWNDM \_ GETEND 訊息</span><span class="sxs-lookup"><span data-stu-id="2c96e-105">MCIWNDM\_GETEND message</span></span>

<span data-ttu-id="2c96e-106">**MCIWNDM \_ GETEND** 訊息會抓取 MCI 裝置或檔案的內容結尾位置。</span><span class="sxs-lookup"><span data-stu-id="2c96e-106">The **MCIWNDM\_GETEND** message retrieves the location of the end of the content of an MCI device or file.</span></span> <span data-ttu-id="2c96e-107">您可以使用 [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2c96e-107">You can send this message explicitly or by using the [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macro.</span></span>


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="2c96e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c96e-108">Return Value</span></span>

<span data-ttu-id="2c96e-109">傳回目前時間格式的位置。</span><span class="sxs-lookup"><span data-stu-id="2c96e-109">Returns the location in the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c96e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c96e-110">Requirements</span></span>



| <span data-ttu-id="2c96e-111">需求</span><span class="sxs-lookup"><span data-stu-id="2c96e-111">Requirement</span></span> | <span data-ttu-id="2c96e-112">值</span><span class="sxs-lookup"><span data-stu-id="2c96e-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c96e-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c96e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2c96e-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c96e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2c96e-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c96e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2c96e-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c96e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2c96e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="2c96e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c96e-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c96e-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c96e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c96e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c96e-120">**MCIWndGetEnd**</span><span class="sxs-lookup"><span data-stu-id="2c96e-120">**MCIWndGetEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





