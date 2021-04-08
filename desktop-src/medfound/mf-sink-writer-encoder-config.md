---
description: 包含具有編碼屬性之屬性存放區的指標。
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: 'MF_SINK_WRITER_ENCODER_CONFIG 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693575"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a><span data-ttu-id="cedd5-103">MF \_ 接收 \_ 寫入器 \_ 編碼器 \_ CONFIG 屬性</span><span class="sxs-lookup"><span data-stu-id="cedd5-103">MF\_SINK\_WRITER\_ENCODER\_CONFIG attribute</span></span>

<span data-ttu-id="cedd5-104">包含具有編碼屬性之屬性存放區的指標。</span><span class="sxs-lookup"><span data-stu-id="cedd5-104">Contains a pointer to a property store with encoding properties.</span></span>

## <a name="data-type"></a><span data-ttu-id="cedd5-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="cedd5-105">Data type</span></span>

<span data-ttu-id="cedd5-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="cedd5-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="cedd5-107">備註</span><span class="sxs-lookup"><span data-stu-id="cedd5-107">Remarks</span></span>

<span data-ttu-id="cedd5-108">這個屬性的值是 [_ *IPropertyStore* \*](/windows/win32/api/propsys/nn-propsys-ipropertystore)指標。</span><span class="sxs-lookup"><span data-stu-id="cedd5-108">The value of this attribute is an [_ *IPropertyStore*\*](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer.</span></span>

<span data-ttu-id="cedd5-109">這個屬性可讓應用程式在使用 [接收寫入器](sink-writer.md)時設定編碼屬性。</span><span class="sxs-lookup"><span data-stu-id="cedd5-109">This attribute enables an application to set encoding properties when using the [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="cedd5-110">若要設定此屬性，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="cedd5-110">To set this attribute, perform the following steps:</span></span>

1.  <span data-ttu-id="cedd5-111">呼叫 [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) 來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cedd5-111">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a new property store.</span></span>
2.  <span data-ttu-id="cedd5-112">在屬性存放區上設定編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="cedd5-112">Set encoder properties on the property store.</span></span> <span data-ttu-id="cedd5-113">可用的屬性視編碼器而定。</span><span class="sxs-lookup"><span data-stu-id="cedd5-113">The available properties depends on the encoder.</span></span> <span data-ttu-id="cedd5-114">如需詳細資訊，請參閱 [編解碼器物件](codecobjects.md)。</span><span class="sxs-lookup"><span data-stu-id="cedd5-114">For more information, see [Codec Objects](codecobjects.md).</span></span>
3.  <span data-ttu-id="cedd5-115">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立新的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="cedd5-115">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
4.  <span data-ttu-id="cedd5-116">呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) ，以在屬性存放區上設定 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標。</span><span class="sxs-lookup"><span data-stu-id="cedd5-116">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer on the attribute store.</span></span>
5.  <span data-ttu-id="cedd5-117">建立接收寫入器的新實例。</span><span class="sxs-lookup"><span data-stu-id="cedd5-117">Create a new instance of the Sink Writer.</span></span> <span data-ttu-id="cedd5-118">將 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標傳遞至建立函數。</span><span class="sxs-lookup"><span data-stu-id="cedd5-118">Pass the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer to the creation function.</span></span> <span data-ttu-id="cedd5-119">如需詳細資訊，請參閱 [接收寫入器屬性](sink-writer-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="cedd5-119">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

<span data-ttu-id="cedd5-120">接收寫入器會先設定編碼器上的屬性，然後再設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cedd5-120">The Sink Writer sets the properties on the encoder before setting the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="cedd5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cedd5-121">Requirements</span></span>



| <span data-ttu-id="cedd5-122">需求</span><span class="sxs-lookup"><span data-stu-id="cedd5-122">Requirement</span></span> | <span data-ttu-id="cedd5-123">值</span><span class="sxs-lookup"><span data-stu-id="cedd5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cedd5-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cedd5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cedd5-125">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cedd5-125">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="cedd5-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cedd5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cedd5-127">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cedd5-127">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="cedd5-128">標頭</span><span class="sxs-lookup"><span data-stu-id="cedd5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cedd5-129"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="cedd5-129"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cedd5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cedd5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cedd5-131">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="cedd5-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cedd5-132">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="cedd5-132">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="cedd5-133">接收寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="cedd5-133">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 
