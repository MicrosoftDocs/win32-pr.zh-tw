---
description: 指定影片捕獲裝置的後置處理外掛程式 CLSID。
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: 'MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970217"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a><span data-ttu-id="cf681-103">MF \_ DEVICESTREAM \_ 延伸模組 \_ 外掛程式 \_ CLSID 屬性</span><span class="sxs-lookup"><span data-stu-id="cf681-103">MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute</span></span>

<span data-ttu-id="cf681-104">指定影片捕獲裝置的後置處理外掛程式 CLSID。</span><span class="sxs-lookup"><span data-stu-id="cf681-104">Specifies the CLSID of a post-processing plug-in for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf681-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="cf681-105">Data type</span></span>

<span data-ttu-id="cf681-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="cf681-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="cf681-107">備註</span><span class="sxs-lookup"><span data-stu-id="cf681-107">Remarks</span></span>

<span data-ttu-id="cf681-108">後置處理外掛程式是一種在捕獲影片映射後進行處理的 MFT。</span><span class="sxs-lookup"><span data-stu-id="cf681-108">A post-processing plug-in is an MFT that processes the video image after it is captured.</span></span> <span data-ttu-id="cf681-109">硬體廠商可在安裝套件中包含後置處理外掛程式。</span><span class="sxs-lookup"><span data-stu-id="cf681-109">The hardware vendor can include a post-processing plug-in as part of the installation package.</span></span> <span data-ttu-id="cf681-110">如果是，影片捕獲來源會將 MF \_ DEVICESTREAM \_ 延伸模組 \_ 外掛程式 \_ clsid 屬性設定為外掛程式的 clsid。</span><span class="sxs-lookup"><span data-stu-id="cf681-110">If so, the video capture source sets the MF\_DEVICESTREAM\_EXTENSION\_PLUGIN\_CLSID attribute to the CLSID of the plug-in.</span></span>

<span data-ttu-id="cf681-111">若要取得這個屬性，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="cf681-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="cf681-112">查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="cf681-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="cf681-113">呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得資料流程的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。</span><span class="sxs-lookup"><span data-stu-id="cf681-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="cf681-114">呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) 以取得屬性。</span><span class="sxs-lookup"><span data-stu-id="cf681-114">Call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) to get the attribute.</span></span>

<span data-ttu-id="cf681-115">若要建立外掛程式，請呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="cf681-115">To create the plug-in, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf681-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf681-116">Requirements</span></span>



| <span data-ttu-id="cf681-117">需求</span><span class="sxs-lookup"><span data-stu-id="cf681-117">Requirement</span></span> | <span data-ttu-id="cf681-118">值</span><span class="sxs-lookup"><span data-stu-id="cf681-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf681-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf681-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf681-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf681-120">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cf681-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf681-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf681-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf681-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cf681-123">標頭</span><span class="sxs-lookup"><span data-stu-id="cf681-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf681-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf681-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf681-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf681-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf681-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="cf681-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
