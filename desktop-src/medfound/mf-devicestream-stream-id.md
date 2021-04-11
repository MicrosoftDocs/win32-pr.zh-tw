---
description: 針對影片捕獲裝置上的資料流程，指定內核串流 (KS) 識別碼。
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: 'MF_DEVICESTREAM_STREAM_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026449"
---
# <a name="mf_devicestream_stream_id-attribute"></a><span data-ttu-id="943de-103">MF \_ DEVICESTREAM \_ 串流 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="943de-103">MF\_DEVICESTREAM\_STREAM\_ID attribute</span></span>

<span data-ttu-id="943de-104">針對影片捕獲裝置上的資料流程，指定內核串流 (KS) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="943de-104">Specifies the kernel streaming (KS) identifier for a stream on a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="943de-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="943de-105">Data type</span></span>

<span data-ttu-id="943de-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="943de-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="943de-107">備註</span><span class="sxs-lookup"><span data-stu-id="943de-107">Remarks</span></span>

<span data-ttu-id="943de-108">若要取得這個屬性，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="943de-108">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="943de-109">查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="943de-109">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="943de-110">呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得資料流程的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="943de-110">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="943de-111">呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 以取得屬性。</span><span class="sxs-lookup"><span data-stu-id="943de-111">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="943de-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="943de-112">Requirements</span></span>



| <span data-ttu-id="943de-113">需求</span><span class="sxs-lookup"><span data-stu-id="943de-113">Requirement</span></span> | <span data-ttu-id="943de-114">值</span><span class="sxs-lookup"><span data-stu-id="943de-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="943de-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="943de-115">Minimum supported client</span></span><br/> | <span data-ttu-id="943de-116">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="943de-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="943de-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="943de-117">Minimum supported server</span></span><br/> | <span data-ttu-id="943de-118">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="943de-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="943de-119">標頭</span><span class="sxs-lookup"><span data-stu-id="943de-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="943de-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="943de-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="943de-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="943de-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943de-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="943de-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




