---
title: 'MCIWNDM_EJECT 訊息 (Vfw .h) '
description: MCIWNDM \_ 退出訊息會將命令傳送至 MCI 裝置，以將其媒體退出。 您可以使用 MCIWndEject 宏明確地傳送此訊息。
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41686ce41b82dc48ee6c22ac556606c79c5b24a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384122"
---
# <a name="mciwndm_eject-message"></a><span data-ttu-id="71502-105">MCIWNDM \_ 退出訊息</span><span class="sxs-lookup"><span data-stu-id="71502-105">MCIWNDM\_EJECT message</span></span>

<span data-ttu-id="71502-106">**MCIWNDM \_ 退出** 訊息會將命令傳送至 MCI 裝置，以將其媒體退出。</span><span class="sxs-lookup"><span data-stu-id="71502-106">The **MCIWNDM\_EJECT** message sends a command to an MCI device to eject its media.</span></span> <span data-ttu-id="71502-107">您可以使用 [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="71502-107">You can send this message explicitly or by using the [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject) macro.</span></span>


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="71502-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="71502-108">Return Value</span></span>

<span data-ttu-id="71502-109">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="71502-109">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="71502-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="71502-110">Requirements</span></span>



| <span data-ttu-id="71502-111">需求</span><span class="sxs-lookup"><span data-stu-id="71502-111">Requirement</span></span> | <span data-ttu-id="71502-112">值</span><span class="sxs-lookup"><span data-stu-id="71502-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="71502-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71502-113">Minimum supported client</span></span><br/> | <span data-ttu-id="71502-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71502-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="71502-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71502-115">Minimum supported server</span></span><br/> | <span data-ttu-id="71502-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71502-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71502-117">標頭</span><span class="sxs-lookup"><span data-stu-id="71502-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="71502-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="71502-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71502-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71502-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71502-120">**MCIWndEject**</span><span class="sxs-lookup"><span data-stu-id="71502-120">**MCIWndEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





