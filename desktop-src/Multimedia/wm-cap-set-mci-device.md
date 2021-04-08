---
title: 'WM_CAP_SET_MCI_DEVICE 訊息 (Vfw .h) '
description: '[WM \_ CAP \_ 設定 \_ MCI \_ 裝置訊息] 會指定要用來捕捉資料的 MCI video 裝置名稱。 您可以使用 capSetMCIDeviceName 宏明確地傳送此訊息。'
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685546"
---
# <a name="wm_cap_set_mci_device-message"></a><span data-ttu-id="ec2b0-105">WM \_ CAP \_ 設定 \_ MCI \_ 裝置訊息</span><span class="sxs-lookup"><span data-stu-id="ec2b0-105">WM\_CAP\_SET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="ec2b0-106">[ **WM \_ CAP \_ 設定 \_ MCI \_ 裝置** 訊息] 會指定要用來捕捉資料的 MCI video 裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="ec2b0-106">The **WM\_CAP\_SET\_MCI\_DEVICE** message specifies the name of the MCI video device to be used to capture data.</span></span> <span data-ttu-id="ec2b0-107">您可以使用 [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ec2b0-107">You can send this message explicitly or by using the [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) macro.</span></span>


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="ec2b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="ec2b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec2b0-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*>szname*</span><span class="sxs-lookup"><span data-stu-id="ec2b0-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="ec2b0-110">以 null 結束的字串指標，其中包含裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec2b0-110">Pointer to a null-terminated string containing the name of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec2b0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec2b0-111">Return Value</span></span>

<span data-ttu-id="ec2b0-112">如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ec2b0-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec2b0-113">備註</span><span class="sxs-lookup"><span data-stu-id="ec2b0-113">Remarks</span></span>

<span data-ttu-id="ec2b0-114">此訊息會將 MCI 裝置名稱儲存在內部結構中。</span><span class="sxs-lookup"><span data-stu-id="ec2b0-114">This message stores the MCI device name in an internal structure.</span></span> <span data-ttu-id="ec2b0-115">它不會開啟或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="ec2b0-115">It does not open or access the device.</span></span> <span data-ttu-id="ec2b0-116">預設裝置名稱為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ec2b0-116">The default device name is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2b0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec2b0-117">Requirements</span></span>



| <span data-ttu-id="ec2b0-118">需求</span><span class="sxs-lookup"><span data-stu-id="ec2b0-118">Requirement</span></span> | <span data-ttu-id="ec2b0-119">值</span><span class="sxs-lookup"><span data-stu-id="ec2b0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec2b0-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec2b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ec2b0-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec2b0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec2b0-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec2b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ec2b0-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec2b0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec2b0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ec2b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec2b0-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec2b0-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec2b0-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec2b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2b0-127">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="ec2b0-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ec2b0-128">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="ec2b0-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





