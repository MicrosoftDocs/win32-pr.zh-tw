---
title: 'ICM_CONFIGURE 訊息 (Vfw .h) '
description: ICM \_ 設定訊息會通知視訊壓縮驅動程式顯示其設定對話方塊，或查詢視訊壓縮驅動程式來判斷它是否有設定對話方塊。
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967988"
---
# <a name="icm_configure-message"></a><span data-ttu-id="96b9a-104">ICM \_ 設定訊息</span><span class="sxs-lookup"><span data-stu-id="96b9a-104">ICM\_CONFIGURE message</span></span>

<span data-ttu-id="96b9a-105">**ICM \_ 設定** 訊息會通知視訊壓縮驅動程式顯示其設定對話方塊，或查詢視訊壓縮驅動程式來判斷它是否有設定對話方塊。</span><span class="sxs-lookup"><span data-stu-id="96b9a-105">The **ICM\_CONFIGURE** message notifies a video compression driver to display its configuration dialog box or queries a video compression driver to determine if it has a configuration dialog box.</span></span> <span data-ttu-id="96b9a-106">您可以使用 [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="96b9a-106">You can send this message explicitly or by using the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro.</span></span>


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="96b9a-107">參數</span><span class="sxs-lookup"><span data-stu-id="96b9a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b9a-108"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span><span class="sxs-lookup"><span data-stu-id="96b9a-108"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="96b9a-109">顯示之對話方塊的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="96b9a-109">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="96b9a-110">您可以在此參數中指定1，以判斷驅動程式是否有設定對話方塊，如同在 [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) 宏中一樣。</span><span class="sxs-lookup"><span data-stu-id="96b9a-110">You can determine if a driver has a configuration dialog box by specifying  1 in this parameter, as in the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b9a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="96b9a-111">Return Value</span></span>

<span data-ttu-id="96b9a-112">\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。</span><span class="sxs-lookup"><span data-stu-id="96b9a-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="96b9a-113">備註</span><span class="sxs-lookup"><span data-stu-id="96b9a-113">Remarks</span></span>

<span data-ttu-id="96b9a-114">此訊息不同于用於硬體設定的 [**Winspool.drv \_ 設定**](drv-configure.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="96b9a-114">This message is different from the [**DRV\_CONFIGURE**](drv-configure.md) message used for hardware configuration.</span></span> <span data-ttu-id="96b9a-115">此訊息的對話方塊應可讓使用者設定和編輯 [**icm \_ >getstate**](icm-getstate.md) 和 [**icm \_ SETSTATE**](icm-setstate.md) 訊息所參考的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="96b9a-115">The dialog box for this message should let the user set and edit the internal state referenced by the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages.</span></span> <span data-ttu-id="96b9a-116">例如，此對話方塊可讓使用者變更影響品質層級和其他類似壓縮選項的參數。</span><span class="sxs-lookup"><span data-stu-id="96b9a-116">For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.</span></span>

## <a name="requirements"></a><span data-ttu-id="96b9a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="96b9a-117">Requirements</span></span>



| <span data-ttu-id="96b9a-118">需求</span><span class="sxs-lookup"><span data-stu-id="96b9a-118">Requirement</span></span> | <span data-ttu-id="96b9a-119">值</span><span class="sxs-lookup"><span data-stu-id="96b9a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="96b9a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96b9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96b9a-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96b9a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="96b9a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96b9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96b9a-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96b9a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="96b9a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="96b9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96b9a-125"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="96b9a-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96b9a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96b9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b9a-127">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="96b9a-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="96b9a-128">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="96b9a-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





