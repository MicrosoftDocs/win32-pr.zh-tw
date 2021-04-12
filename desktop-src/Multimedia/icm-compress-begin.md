---
title: 'ICM_COMPRESS_BEGIN 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 開始訊息會通知影片壓縮驅動程式準備壓縮資料。 您可以使用 ICCompressBegin 宏明確地傳送此訊息。
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- ICM_COMPRESS_BEGIN message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025476"
---
# <a name="icm_compress_begin-message"></a><span data-ttu-id="02d11-105">ICM \_ 壓縮 \_ 開始訊息</span><span class="sxs-lookup"><span data-stu-id="02d11-105">ICM\_COMPRESS\_BEGIN message</span></span>

<span data-ttu-id="02d11-106">**ICM \_ 壓縮 \_ 開始** 訊息會通知影片壓縮驅動程式準備壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="02d11-106">The **ICM\_COMPRESS\_BEGIN** message notifies a video compression driver to prepare to compress data.</span></span> <span data-ttu-id="02d11-107">您可以使用 [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="02d11-107">You can send this message explicitly or by using the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro.</span></span>


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="02d11-108">參數</span><span class="sxs-lookup"><span data-stu-id="02d11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d11-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="02d11-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="02d11-110">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。</span><span class="sxs-lookup"><span data-stu-id="02d11-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="02d11-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="02d11-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="02d11-112">[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸出格式。</span><span class="sxs-lookup"><span data-stu-id="02d11-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02d11-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="02d11-113">Return Value</span></span>

<span data-ttu-id="02d11-114">如果如果 \_ \_ 不支援輸入或輸出格式，驅動程式支援指定的壓縮或 ICERR BADFORMAT，則會傳回 ICERR OK。</span><span class="sxs-lookup"><span data-stu-id="02d11-114">Returns ICERR\_OK if the driver supports the specified compression or ICERR\_BADFORMAT if the input or output format is not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="02d11-115">備註</span><span class="sxs-lookup"><span data-stu-id="02d11-115">Remarks</span></span>

<span data-ttu-id="02d11-116">驅動程式應該在收到 [**ICM \_ 壓縮**](icm-compress.md) 訊息時，配置並初始化其壓縮資料格式所需的任何資料表或記憶體。</span><span class="sxs-lookup"><span data-stu-id="02d11-116">The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the [**ICM\_COMPRESS**](icm-compress.md) message.</span></span>

<span data-ttu-id="02d11-117">BC-VCM-LVM-HYPERV 會儲存最近的 **ICM \_ 壓縮 \_ 開始** 訊息的設定。</span><span class="sxs-lookup"><span data-stu-id="02d11-117">VCM saves the settings of the most recent **ICM\_COMPRESS\_BEGIN** message.</span></span> <span data-ttu-id="02d11-118">**Icm \_ 壓縮 \_ 開始** 和 [**icm \_ 壓縮 \_ 結束**](icm-compress-end.md)訊息不會被嵌套。</span><span class="sxs-lookup"><span data-stu-id="02d11-118">The **ICM\_COMPRESS\_BEGIN** and [**ICM\_COMPRESS\_END**](icm-compress-end.md) messages do not nest.</span></span> <span data-ttu-id="02d11-119">如果您的驅動程式會在使用 **icm \_ 壓縮 \_ 結束** 的情況下，于壓縮停止之前收到 **icm \_ 壓縮 \_ 開始**，則應該以新的參數重新開機壓縮。</span><span class="sxs-lookup"><span data-stu-id="02d11-119">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="02d11-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="02d11-120">Requirements</span></span>



| <span data-ttu-id="02d11-121">需求</span><span class="sxs-lookup"><span data-stu-id="02d11-121">Requirement</span></span> | <span data-ttu-id="02d11-122">值</span><span class="sxs-lookup"><span data-stu-id="02d11-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="02d11-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02d11-123">Minimum supported client</span></span><br/> | <span data-ttu-id="02d11-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02d11-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="02d11-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02d11-125">Minimum supported server</span></span><br/> | <span data-ttu-id="02d11-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02d11-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="02d11-127">標頭</span><span class="sxs-lookup"><span data-stu-id="02d11-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="02d11-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="02d11-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d11-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02d11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d11-130">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="02d11-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="02d11-131">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="02d11-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

