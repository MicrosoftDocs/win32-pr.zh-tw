---
description: 指定音訊捕獲裝置的裝置角色。
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026448"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a><span data-ttu-id="a7120-103">MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 角色屬性</span><span class="sxs-lookup"><span data-stu-id="a7120-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ROLE attribute</span></span>

<span data-ttu-id="a7120-104">指定音訊捕獲裝置的裝置角色。</span><span class="sxs-lookup"><span data-stu-id="a7120-104">Specifies the device role for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="a7120-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a7120-105">Data type</span></span>

<span data-ttu-id="a7120-106">**ERole** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="a7120-106">**ERole** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a7120-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="a7120-107">Get/set</span></span>

<span data-ttu-id="a7120-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="a7120-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a7120-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="a7120-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7120-110">備註</span><span class="sxs-lookup"><span data-stu-id="a7120-110">Remarks</span></span>

<span data-ttu-id="a7120-111">**ERole** 列舉型別記載于核心音訊 API 檔中。</span><span class="sxs-lookup"><span data-stu-id="a7120-111">The **eRole** enumeration type is documented in the Core Audio API documentation.</span></span>

<span data-ttu-id="a7120-112">屬性的值會指定裝置角色。</span><span class="sxs-lookup"><span data-stu-id="a7120-112">The value of the attribute specifies a device role.</span></span> <span data-ttu-id="a7120-113">這個屬性與下列函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="a7120-113">This attribute is used with the following functions.</span></span>

<span data-ttu-id="a7120-114">這個屬性可用來作為 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) 和 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函數的輸入。</span><span class="sxs-lookup"><span data-stu-id="a7120-114">This attribute can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="a7120-115">如果指定了屬性，則函式會建立媒體來源，以針對指定的裝置角色使用預設音訊捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="a7120-115">If the attribute is specified, the function creates a media source that uses the default audio capture device for the specified device role.</span></span>

<span data-ttu-id="a7120-116">這個屬性也可以當做 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) 函數的輸入使用。</span><span class="sxs-lookup"><span data-stu-id="a7120-116">This attribute can also be used as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="a7120-117">如果指定了屬性，則列舉會限制為指定的裝置角色。</span><span class="sxs-lookup"><span data-stu-id="a7120-117">If the attribute is specified, the enumeration is restricted to the specified device role.</span></span> <span data-ttu-id="a7120-118">此外， **MFEnumDeviceSources** 函式所傳回的每個啟用物件都包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a7120-118">In addition, each activation object returned by the **MFEnumDeviceSources** function contains this attribute.</span></span> <span data-ttu-id="a7120-119">然後，在建立媒體來源時，啟始物件會在內部使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7120-119">The attribute is then used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="a7120-120">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a7120-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7120-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7120-121">Requirements</span></span>



| <span data-ttu-id="a7120-122">需求</span><span class="sxs-lookup"><span data-stu-id="a7120-122">Requirement</span></span> | <span data-ttu-id="a7120-123">值</span><span class="sxs-lookup"><span data-stu-id="a7120-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a7120-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7120-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a7120-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7120-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a7120-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7120-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a7120-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7120-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a7120-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a7120-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7120-129"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7120-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7120-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7120-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7120-131">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a7120-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a7120-132">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="a7120-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="a7120-133">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="a7120-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




