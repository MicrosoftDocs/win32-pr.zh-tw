---
description: 指定資料流程是否與相同類型的其他資料流程相互排斥。
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: 'MF_SD_MUTUALLY_EXCLUSIVE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984605"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a><span data-ttu-id="19656-103">MF \_ SD \_ 互斥 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="19656-103">MF\_SD\_MUTUALLY\_EXCLUSIVE attribute</span></span>

<span data-ttu-id="19656-104">指定資料流程是否與相同類型的其他資料流程相互排斥。</span><span class="sxs-lookup"><span data-stu-id="19656-104">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span>

## <a name="data-type"></a><span data-ttu-id="19656-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="19656-105">Data type</span></span>

<span data-ttu-id="19656-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="19656-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="19656-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="19656-107">Get/set</span></span>

<span data-ttu-id="19656-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="19656-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="19656-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="19656-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="19656-110">適用於</span><span class="sxs-lookup"><span data-stu-id="19656-110">Applies to</span></span>

[<span data-ttu-id="19656-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="19656-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="19656-112">備註</span><span class="sxs-lookup"><span data-stu-id="19656-112">Remarks</span></span>

<span data-ttu-id="19656-113">如果此屬性為 **TRUE** (非零) ，則在相同的呈現中，資料流程與相同類型的其他資料流程（例如音訊或影片）互斥。</span><span class="sxs-lookup"><span data-stu-id="19656-113">If this attribute is **TRUE** (nonzero), the stream is mutually exclusive with other streams of the same type, such as audio or video, within the same presentation.</span></span> <span data-ttu-id="19656-114">例如，如果 AVI 檔案包含多個音訊串流，則會標示為互斥，因為一次只能播放一個音訊串流。</span><span class="sxs-lookup"><span data-stu-id="19656-114">For example, if an AVI file contains multiple audio streams, they are marked as mutually exclusive, because only one audio stream should be played at one time.</span></span>

<span data-ttu-id="19656-115">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="19656-115">The default value is **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="19656-116">這個屬性不會用於 Advanced 系統格式 (ASF) 檔，其具有更精密的方式來表示相互排除準則。</span><span class="sxs-lookup"><span data-stu-id="19656-116">This attribute is not used for Advanced Systems Format (ASF) files, which have a more sophisticated way to represent mutual exclusion criteria.</span></span> <span data-ttu-id="19656-117">如需詳細資訊，請參閱 [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion)。</span><span class="sxs-lookup"><span data-stu-id="19656-117">For more information, see [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span></span>

 

<span data-ttu-id="19656-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="19656-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="19656-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="19656-119">Requirements</span></span>



| <span data-ttu-id="19656-120">需求</span><span class="sxs-lookup"><span data-stu-id="19656-120">Requirement</span></span> | <span data-ttu-id="19656-121">值</span><span class="sxs-lookup"><span data-stu-id="19656-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19656-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19656-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19656-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19656-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="19656-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19656-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19656-125">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19656-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="19656-126">標頭</span><span class="sxs-lookup"><span data-stu-id="19656-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="19656-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="19656-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19656-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19656-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19656-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="19656-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="19656-130">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="19656-130">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




