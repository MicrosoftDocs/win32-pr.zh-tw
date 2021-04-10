---
title: 'MCIWNDM_SETVOLUME 訊息 (Vfw .h) '
description: MCIWNDM \_ SETVOLUME 訊息會設定 MCI 裝置的磁片區層級。 您可以使用 MCIWndSetVolume 宏明確地傳送此訊息。
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685590"
---
# <a name="mciwndm_setvolume-message"></a><span data-ttu-id="25c0c-105">MCIWNDM \_ SETVOLUME 訊息</span><span class="sxs-lookup"><span data-stu-id="25c0c-105">MCIWNDM\_SETVOLUME message</span></span>

<span data-ttu-id="25c0c-106">**MCIWNDM \_ SETVOLUME** 訊息會設定 MCI 裝置的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="25c0c-106">The **MCIWNDM\_SETVOLUME** message sets the volume level of an MCI device.</span></span> <span data-ttu-id="25c0c-107">您可以使用 [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="25c0c-107">You can send this message explicitly or by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span>


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a><span data-ttu-id="25c0c-108">參數</span><span class="sxs-lookup"><span data-stu-id="25c0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c0c-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span><span class="sxs-lookup"><span data-stu-id="25c0c-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span></span>
</dt> <dd>

<span data-ttu-id="25c0c-110">新的磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="25c0c-110">New volume level.</span></span> <span data-ttu-id="25c0c-111">針對一般磁片區層級指定1000。</span><span class="sxs-lookup"><span data-stu-id="25c0c-111">Specify 1000 for normal volume level.</span></span> <span data-ttu-id="25c0c-112">針對較大的磁片區指定較高的值，或針對較低的磁片區指定較低的值。</span><span class="sxs-lookup"><span data-stu-id="25c0c-112">Specify a higher value for a louder volume or a lower value for a quieter volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c0c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="25c0c-113">Return Value</span></span>

<span data-ttu-id="25c0c-114">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="25c0c-114">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c0c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="25c0c-115">Requirements</span></span>



| <span data-ttu-id="25c0c-116">需求</span><span class="sxs-lookup"><span data-stu-id="25c0c-116">Requirement</span></span> | <span data-ttu-id="25c0c-117">值</span><span class="sxs-lookup"><span data-stu-id="25c0c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="25c0c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="25c0c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25c0c-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25c0c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="25c0c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="25c0c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25c0c-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="25c0c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="25c0c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="25c0c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="25c0c-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="25c0c-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25c0c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25c0c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c0c-125">**MCIWndSetVolume**</span><span class="sxs-lookup"><span data-stu-id="25c0c-125">**MCIWndSetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 





