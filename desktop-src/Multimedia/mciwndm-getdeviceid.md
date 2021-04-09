---
title: 'MCIWNDM_GETDEVICEID 訊息 (Vfw .h) '
description: MCIWNDM \_ GETDEVICEID 訊息會抓取目前開啟之 MCI 裝置的識別碼，以搭配 mciSendCommand 函式使用。 您可以使用 MCIWndGetDeviceID 宏明確地傳送此訊息。
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- MCIWNDM_GETDEVICEID message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024705"
---
# <a name="mciwndm_getdeviceid-message"></a><span data-ttu-id="1bd27-105">MCIWNDM \_ GETDEVICEID 訊息</span><span class="sxs-lookup"><span data-stu-id="1bd27-105">MCIWNDM\_GETDEVICEID message</span></span>

<span data-ttu-id="1bd27-106">**MCIWNDM \_ GETDEVICEID** 訊息會抓取目前開啟之 MCI 裝置的識別碼，以搭配 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函式使用。</span><span class="sxs-lookup"><span data-stu-id="1bd27-106">The **MCIWNDM\_GETDEVICEID** message retrieves the identifier of the currently open MCI device to use with the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="1bd27-107">您可以使用 [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1bd27-107">You can send this message explicitly or by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span>


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="1bd27-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bd27-108">Return Value</span></span>

<span data-ttu-id="1bd27-109">傳回裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bd27-109">Returns the device identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bd27-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bd27-110">Requirements</span></span>



| <span data-ttu-id="1bd27-111">需求</span><span class="sxs-lookup"><span data-stu-id="1bd27-111">Requirement</span></span> | <span data-ttu-id="1bd27-112">值</span><span class="sxs-lookup"><span data-stu-id="1bd27-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1bd27-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bd27-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1bd27-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bd27-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1bd27-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bd27-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1bd27-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bd27-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1bd27-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1bd27-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bd27-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bd27-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bd27-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bd27-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="1bd27-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bd27-120">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1bd27-121">**MCIWndGetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1bd27-121">**MCIWndGetDeviceID**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

