---
description: 包含已同步處理之可存取媒體交換的易記名稱， (薩米文檔案中定義的薩米) 樣式。
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: 'MF_PD_SAMI_STYLELIST 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852431"
---
# <a name="mf_pd_sami_stylelist-attribute"></a><span data-ttu-id="27881-103">MF \_ PD \_ 薩米 \_ STYLELIST 屬性</span><span class="sxs-lookup"><span data-stu-id="27881-103">MF\_PD\_SAMI\_STYLELIST attribute</span></span>

<span data-ttu-id="27881-104">包含已同步處理之可存取媒體交換的易記名稱， (薩米文檔案中定義的薩米) 樣式。</span><span class="sxs-lookup"><span data-stu-id="27881-104">Contains the friendly names of the Synchronized Accessible Media Interchange (SAMI) styles defined in the SAMI file.</span></span>

<span data-ttu-id="27881-105">[薩米媒體來源](sami-media-source.md)會在其所建立的表示描述項上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="27881-105">The [SAMI Media Source](sami-media-source.md) sets this attribute on the presentation descriptor that it creates.</span></span>

## <a name="data-type"></a><span data-ttu-id="27881-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="27881-106">Data type</span></span>

<span data-ttu-id="27881-107">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="27881-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="27881-108">備註</span><span class="sxs-lookup"><span data-stu-id="27881-108">Remarks</span></span>

<span data-ttu-id="27881-109">屬性 blob 具有下列結構：</span><span class="sxs-lookup"><span data-stu-id="27881-109">The attribute blob has the following structure:</span></span>



<span data-ttu-id="27881-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="27881-110">Data Type</span></span>

<span data-ttu-id="27881-111">描述</span><span class="sxs-lookup"><span data-stu-id="27881-111">Description</span></span>

<span data-ttu-id="27881-112">大小 (位元組)</span><span class="sxs-lookup"><span data-stu-id="27881-112">Size (bytes)</span></span>

<span data-ttu-id="27881-113">**Dword**</span><span class="sxs-lookup"><span data-stu-id="27881-113">**DWORD**</span></span>

<span data-ttu-id="27881-114">樣式字串的數目。</span><span class="sxs-lookup"><span data-stu-id="27881-114">Number of style strings.</span></span>

<span data-ttu-id="27881-115">4</span><span class="sxs-lookup"><span data-stu-id="27881-115">4</span></span>

<span data-ttu-id="27881-116">針對每個樣式字串：</span><span class="sxs-lookup"><span data-stu-id="27881-116">For each style string:</span></span>

<span data-ttu-id="27881-117">**Dword**</span><span class="sxs-lookup"><span data-stu-id="27881-117">**DWORD**</span></span>

<span data-ttu-id="27881-118">字串的大小（以位元組為單位），包括 **Null** 字元。</span><span class="sxs-lookup"><span data-stu-id="27881-118">Size of the string in bytes, including the **NULL** character.</span></span>

<span data-ttu-id="27881-119">4</span><span class="sxs-lookup"><span data-stu-id="27881-119">4</span></span>

<span data-ttu-id="27881-120">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="27881-120">**LPWSTR**</span></span>

<span data-ttu-id="27881-121">以 Null 結尾的寬字元字串，其中包含樣式的名稱。</span><span class="sxs-lookup"><span data-stu-id="27881-121">Null-terminated wide-character string containing the name of the style.</span></span>

<span data-ttu-id="27881-122">不定</span><span class="sxs-lookup"><span data-stu-id="27881-122">Varies</span></span>



 

<span data-ttu-id="27881-123">若要設定樣式或取得目前的樣式，請使用 [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) 介面。</span><span class="sxs-lookup"><span data-stu-id="27881-123">To set the style or retrieve the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span>

<span data-ttu-id="27881-124">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="27881-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="27881-125">範例</span><span class="sxs-lookup"><span data-stu-id="27881-125">Examples</span></span>


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="27881-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="27881-126">Requirements</span></span>



| <span data-ttu-id="27881-127">需求</span><span class="sxs-lookup"><span data-stu-id="27881-127">Requirement</span></span> | <span data-ttu-id="27881-128">值</span><span class="sxs-lookup"><span data-stu-id="27881-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27881-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27881-129">Minimum supported client</span></span><br/> | <span data-ttu-id="27881-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27881-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="27881-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27881-131">Minimum supported server</span></span><br/> | <span data-ttu-id="27881-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27881-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="27881-133">標頭</span><span class="sxs-lookup"><span data-stu-id="27881-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="27881-134"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="27881-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27881-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27881-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27881-136">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="27881-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="27881-137">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="27881-137">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="27881-138">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="27881-138">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="27881-139">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="27881-139">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="27881-140">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="27881-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="27881-141">薩米媒體來源</span><span class="sxs-lookup"><span data-stu-id="27881-141">SAMI Media Source</span></span>](sami-media-source.md)
</dt> </dl>

 

 




