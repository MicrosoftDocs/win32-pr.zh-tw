---
description: 從來源讀取器取得媒體來源的特性。
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: 'MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321660"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a><span data-ttu-id="7d52b-103">MF \_ 來源 \_ 讀取器 \_ MEDIASOURCE \_ 特性屬性</span><span class="sxs-lookup"><span data-stu-id="7d52b-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="7d52b-104">從 [來源讀取器](source-reader.md)取得媒體來源的特性。</span><span class="sxs-lookup"><span data-stu-id="7d52b-104">Gets the characteristics of the media source from the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="7d52b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7d52b-105">Data type</span></span>

<span data-ttu-id="7d52b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7d52b-106">**UINT32**</span></span>

<span data-ttu-id="7d52b-107">值是 [**MFMEDIASOURCE \_ 特性**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)列舉中的位 **or** 旗標。</span><span class="sxs-lookup"><span data-stu-id="7d52b-107">The value is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d52b-108">備註</span><span class="sxs-lookup"><span data-stu-id="7d52b-108">Remarks</span></span>

<span data-ttu-id="7d52b-109">若要取得這個屬性，請在來源讀取器上呼叫 [**IMFSourceReader：： GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) 方法。</span><span class="sxs-lookup"><span data-stu-id="7d52b-109">To get this attribute, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method on the source reader.</span></span> <span data-ttu-id="7d52b-110">將 *dwStreamIndex* 參數設定為 [ **mf \_ 來源 \_ 讀取器 \_ MEDIASOURCE** ]，並將 *guidAttribute* 參數設定為 [mf \_ 來源 \_ 讀取器 \_ MEDIASOURCE] \_ 特性。</span><span class="sxs-lookup"><span data-stu-id="7d52b-110">Set the *dwStreamIndex* parameter to **MF\_SOURCE\_READER\_MEDIASOURCE** and the *guidAttribute* parameter to MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS.</span></span>

<span data-ttu-id="7d52b-111">這個屬性的 **PROPVARIANT** 類型是 **VT \_ UI4**。</span><span class="sxs-lookup"><span data-stu-id="7d52b-111">The **PROPVARIANT** type for this attribute is **VT\_UI4**.</span></span>

## <a name="examples"></a><span data-ttu-id="7d52b-112">範例</span><span class="sxs-lookup"><span data-stu-id="7d52b-112">Examples</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="7d52b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d52b-113">Requirements</span></span>



| <span data-ttu-id="7d52b-114">需求</span><span class="sxs-lookup"><span data-stu-id="7d52b-114">Requirement</span></span> | <span data-ttu-id="7d52b-115">值</span><span class="sxs-lookup"><span data-stu-id="7d52b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d52b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d52b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7d52b-117">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d52b-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7d52b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d52b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7d52b-119">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d52b-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7d52b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7d52b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d52b-121"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d52b-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d52b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d52b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d52b-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7d52b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d52b-124">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="7d52b-124">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




