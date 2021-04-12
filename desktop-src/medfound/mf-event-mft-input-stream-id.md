---
description: 指定媒體基礎轉換 (MFT) 的輸入資料流程。
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: 'MF_EVENT_MFT_INPUT_STREAM_ID 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d3966c33dc563fc9e38ad367cc675ba6616c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191516"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a><span data-ttu-id="5d2c6-103">MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="5d2c6-103">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID attribute</span></span>

<span data-ttu-id="5d2c6-104">指定媒體基礎轉換 (MFT) 的輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-104">Specifies an input stream on a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="5d2c6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5d2c6-105">Data type</span></span>

<span data-ttu-id="5d2c6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5d2c6-106">**UINT32**</span></span>

<span data-ttu-id="5d2c6-107">此值為輸入資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-107">The value is an input stream identifier.</span></span>

## <a name="getset"></a><span data-ttu-id="5d2c6-108">取得/設定</span><span class="sxs-lookup"><span data-stu-id="5d2c6-108">Get/set</span></span>

<span data-ttu-id="5d2c6-109">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5d2c6-110">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5d2c6-111">適用於</span><span class="sxs-lookup"><span data-stu-id="5d2c6-111">Applies to</span></span>

[<span data-ttu-id="5d2c6-112">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="5d2c6-112">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="5d2c6-113">備註</span><span class="sxs-lookup"><span data-stu-id="5d2c6-113">Remarks</span></span>

<span data-ttu-id="5d2c6-114">這個屬性會搭配下列事件使用：</span><span class="sxs-lookup"><span data-stu-id="5d2c6-114">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="5d2c6-115">METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="5d2c6-115">METransformDrainComplete</span></span>](metransformdraincomplete.md)
-   [<span data-ttu-id="5d2c6-116">METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="5d2c6-116">METransformNeedInput</span></span>](metransformneedinput.md)

<span data-ttu-id="5d2c6-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2c6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d2c6-118">Requirements</span></span>



| <span data-ttu-id="5d2c6-119">需求</span><span class="sxs-lookup"><span data-stu-id="5d2c6-119">Requirement</span></span> | <span data-ttu-id="5d2c6-120">值</span><span class="sxs-lookup"><span data-stu-id="5d2c6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2c6-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d2c6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2c6-122">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d2c6-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5d2c6-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d2c6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2c6-124">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d2c6-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5d2c6-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5d2c6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d2c6-126"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2c6-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2c6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d2c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2c6-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5d2c6-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d2c6-129">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="5d2c6-129">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="5d2c6-130">事件屬性</span><span class="sxs-lookup"><span data-stu-id="5d2c6-130">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




