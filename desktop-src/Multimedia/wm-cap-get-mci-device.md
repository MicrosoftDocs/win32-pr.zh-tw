---
title: 'WM_CAP_GET_MCI_DEVICE 訊息 (Vfw .h) '
description: '[WM \_ cap \_ 取得 \_ mci \_ 裝置] 訊息會取出先前以 WM \_ CAP \_ SET \_ MCI \_ 裝置訊息設定的 MCI 裝置名稱。 您可以使用 capGetMCIDeviceName 宏明確地傳送此訊息。'
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464212"
---
# <a name="wm_cap_get_mci_device-message"></a><span data-ttu-id="1a7eb-105">WM \_ CAP \_ 取得 \_ MCI \_ 裝置訊息</span><span class="sxs-lookup"><span data-stu-id="1a7eb-105">WM\_CAP\_GET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="1a7eb-106">[ **Wm \_ cap \_ 取得 \_ mci \_ 裝置** ] 訊息會取出先前以 [**WM \_ CAP \_ set \_ MCI \_ 裝置**](wm-cap-set-mci-device.md) 訊息設定的 MCI 裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="1a7eb-106">The **WM\_CAP\_GET\_MCI\_DEVICE** message retrieves the name of an MCI device previously set with the [**WM\_CAP\_SET\_MCI\_DEVICE**](wm-cap-set-mci-device.md) message.</span></span> <span data-ttu-id="1a7eb-107">您可以使用 [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1a7eb-107">You can send this message explicitly or by using the [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) macro.</span></span>


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="1a7eb-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a7eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a7eb-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="1a7eb-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="1a7eb-110">**>szname** 所參考的緩衝區長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1a7eb-110">Length, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="1a7eb-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="1a7eb-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="1a7eb-112">包含 MCI 裝置名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="1a7eb-112">Pointer to a null-terminated string that contains the MCI device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a7eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a7eb-113">Return Value</span></span>

<span data-ttu-id="1a7eb-114">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1a7eb-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a7eb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a7eb-115">Requirements</span></span>



| <span data-ttu-id="1a7eb-116">需求</span><span class="sxs-lookup"><span data-stu-id="1a7eb-116">Requirement</span></span> | <span data-ttu-id="1a7eb-117">值</span><span class="sxs-lookup"><span data-stu-id="1a7eb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1a7eb-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a7eb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1a7eb-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a7eb-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1a7eb-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a7eb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1a7eb-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a7eb-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1a7eb-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1a7eb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a7eb-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a7eb-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a7eb-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a7eb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a7eb-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="1a7eb-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1a7eb-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="1a7eb-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





