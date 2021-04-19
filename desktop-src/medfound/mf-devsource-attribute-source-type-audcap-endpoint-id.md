---
description: 指定音訊捕獲裝置的端點識別碼。
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: 'MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989522"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a><span data-ttu-id="3d4fb-103">MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 端點 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="3d4fb-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="3d4fb-104">指定音訊捕獲裝置的端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-104">Specifies the endpoint ID for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="3d4fb-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="3d4fb-105">Data type</span></span>

<span data-ttu-id="3d4fb-106">**WCHAR\***</span><span class="sxs-lookup"><span data-stu-id="3d4fb-106">**WCHAR\***</span></span>

## <a name="getset"></a><span data-ttu-id="3d4fb-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="3d4fb-107">Get/set</span></span>

<span data-ttu-id="3d4fb-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="3d4fb-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d4fb-110">備註</span><span class="sxs-lookup"><span data-stu-id="3d4fb-110">Remarks</span></span>

<span data-ttu-id="3d4fb-111">屬性的值是端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-111">The value of the attribute is an endpoint ID.</span></span> <span data-ttu-id="3d4fb-112">這個屬性與下列函數搭配使用：</span><span class="sxs-lookup"><span data-stu-id="3d4fb-112">This attribute is used with the following functions:</span></span>

-   <span data-ttu-id="3d4fb-113">它可用來做為 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) 和 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函式的輸入。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-113">It can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="3d4fb-114">在此內容中，屬性會指定函式的音訊捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-114">In this context, the attribute specifies the audio capture device for the function.</span></span> <span data-ttu-id="3d4fb-115">您可以藉由呼叫 [**IMMDevice：： GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) 方法，取得指定裝置的端點識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-115">You can get the endpoint ID for a given device by calling the [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method.</span></span> <span data-ttu-id="3d4fb-116">如需詳細資訊，請參閱核心音訊 API 檔。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-116">See the Core Audio API documentation for more information.</span></span>
-   <span data-ttu-id="3d4fb-117">當 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) 函式列舉音訊裝置時，傳回的啟用物件會包含這個屬性。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-117">When the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function enumerates audio devices, the returned activation objects contain this attribute.</span></span> <span data-ttu-id="3d4fb-118">當啟用物件建立媒體來源時，會在內部使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-118">The attribute is used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="3d4fb-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="3d4fb-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d4fb-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d4fb-120">Requirements</span></span>



| <span data-ttu-id="3d4fb-121">需求</span><span class="sxs-lookup"><span data-stu-id="3d4fb-121">Requirement</span></span> | <span data-ttu-id="3d4fb-122">值</span><span class="sxs-lookup"><span data-stu-id="3d4fb-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4fb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3d4fb-123">Header</span></span><br/> | <dl> <span data-ttu-id="3d4fb-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d4fb-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4fb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d4fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4fb-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="3d4fb-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d4fb-127">音訊/視訊擷取</span><span class="sxs-lookup"><span data-stu-id="3d4fb-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="3d4fb-128">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="3d4fb-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
