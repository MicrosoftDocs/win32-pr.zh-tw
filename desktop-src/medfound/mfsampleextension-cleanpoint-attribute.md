---
description: 指出範例是否為隨機存取點。
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: 'MFSampleExtension_CleanPoint 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54ea9bf4f1ca207a6ab12bac331c57db63136a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512625"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a><span data-ttu-id="48dd1-103">MFSampleExtension \_ CleanPoint 屬性</span><span class="sxs-lookup"><span data-stu-id="48dd1-103">MFSampleExtension\_CleanPoint attribute</span></span>

<span data-ttu-id="48dd1-104">指出範例是否為隨機存取點。</span><span class="sxs-lookup"><span data-stu-id="48dd1-104">Indicates whether a sample is a random access point.</span></span>

## <a name="data-type"></a><span data-ttu-id="48dd1-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="48dd1-105">Data type</span></span>

<span data-ttu-id="48dd1-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="48dd1-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="48dd1-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="48dd1-107">Get/set</span></span>

<span data-ttu-id="48dd1-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="48dd1-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="48dd1-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="48dd1-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="48dd1-110">適用於</span><span class="sxs-lookup"><span data-stu-id="48dd1-110">Applies to</span></span>

[<span data-ttu-id="48dd1-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="48dd1-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="48dd1-112">備註</span><span class="sxs-lookup"><span data-stu-id="48dd1-112">Remarks</span></span>

<span data-ttu-id="48dd1-113">這個屬性會套用至範例。</span><span class="sxs-lookup"><span data-stu-id="48dd1-113">This attribute applies to samples.</span></span> <span data-ttu-id="48dd1-114">如果屬性為 **TRUE**，則此範例為隨機存取點，而解碼可以從此範例開始。</span><span class="sxs-lookup"><span data-stu-id="48dd1-114">If the attribute is **TRUE**, the sample is a random access point and decoding can begin from this sample.</span></span> <span data-ttu-id="48dd1-115">否則，此範例不是隨機存取點。</span><span class="sxs-lookup"><span data-stu-id="48dd1-115">Otherwise, the sample is not a random access point.</span></span>

<span data-ttu-id="48dd1-116">如果未設定此屬性，則預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="48dd1-116">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="48dd1-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="48dd1-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="48dd1-118">範例</span><span class="sxs-lookup"><span data-stu-id="48dd1-118">Examples</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="48dd1-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="48dd1-119">Requirements</span></span>



| <span data-ttu-id="48dd1-120">需求</span><span class="sxs-lookup"><span data-stu-id="48dd1-120">Requirement</span></span> | <span data-ttu-id="48dd1-121">值</span><span class="sxs-lookup"><span data-stu-id="48dd1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48dd1-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48dd1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="48dd1-123">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48dd1-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="48dd1-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48dd1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="48dd1-125">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48dd1-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="48dd1-126">標頭</span><span class="sxs-lookup"><span data-stu-id="48dd1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="48dd1-127"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="48dd1-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48dd1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48dd1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48dd1-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="48dd1-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="48dd1-130">範例屬性</span><span class="sxs-lookup"><span data-stu-id="48dd1-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="48dd1-131">媒體範例</span><span class="sxs-lookup"><span data-stu-id="48dd1-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




