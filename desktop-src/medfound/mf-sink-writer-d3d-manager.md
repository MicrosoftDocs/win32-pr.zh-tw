---
description: 包含接收寫入器之 DXGI 裝置管理員的指標。
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: 'MF_SINK_WRITER_D3D_MANAGER 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975914"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a><span data-ttu-id="11403-103">MF \_ 接收 \_ 寫入器 \_ D3D \_ 管理員屬性</span><span class="sxs-lookup"><span data-stu-id="11403-103">MF\_SINK\_WRITER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="11403-104">包含 [接收寫入器](sink-writer.md)之 DXGI 裝置管理員的指標。</span><span class="sxs-lookup"><span data-stu-id="11403-104">Contains a pointer to the DXGI Device Manager for the [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="11403-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="11403-105">Data type</span></span>

<span data-ttu-id="11403-106">**IMFDXGIDeviceManager \** _ 儲存為 _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="11403-106">**IMFDXGIDeviceManager\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="remarks"></a><span data-ttu-id="11403-107">備註</span><span class="sxs-lookup"><span data-stu-id="11403-107">Remarks</span></span>

<span data-ttu-id="11403-108">這個屬性的值是 [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="11403-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="11403-109">使用此屬性可為接收寫入器載入的任何影片編碼器或媒體接收器提供 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="11403-109">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the Sink Writer.</span></span>

<span data-ttu-id="11403-110">使用這個屬性搭配下列函數：</span><span class="sxs-lookup"><span data-stu-id="11403-110">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="11403-111">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="11403-111">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="11403-112">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="11403-112">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="11403-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="11403-113">Requirements</span></span>



| <span data-ttu-id="11403-114">需求</span><span class="sxs-lookup"><span data-stu-id="11403-114">Requirement</span></span> | <span data-ttu-id="11403-115">值</span><span class="sxs-lookup"><span data-stu-id="11403-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11403-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11403-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11403-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11403-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="11403-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11403-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11403-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11403-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="11403-120">標頭</span><span class="sxs-lookup"><span data-stu-id="11403-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="11403-121"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="11403-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11403-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11403-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11403-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="11403-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="11403-124">接收寫入器</span><span class="sxs-lookup"><span data-stu-id="11403-124">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 




