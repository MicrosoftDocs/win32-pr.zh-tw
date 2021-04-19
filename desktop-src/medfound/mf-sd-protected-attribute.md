---
description: 指出資料流程是否包含受保護的內容。
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: 'MF_SD_PROTECTED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989017"
---
# <a name="mf_sd_protected-attribute"></a><span data-ttu-id="73719-103">MF \_ SD \_ PROTECTED 屬性</span><span class="sxs-lookup"><span data-stu-id="73719-103">MF\_SD\_PROTECTED attribute</span></span>

<span data-ttu-id="73719-104">指出資料流程是否包含受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="73719-104">Indicates whether a stream contains protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="73719-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="73719-105">Data type</span></span>

<span data-ttu-id="73719-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="73719-106">**UINT32**</span></span>

<span data-ttu-id="73719-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="73719-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73719-108">備註</span><span class="sxs-lookup"><span data-stu-id="73719-108">Remarks</span></span>

<span data-ttu-id="73719-109">這個屬性會套用至資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="73719-109">This attribute applies to stream descriptors.</span></span> <span data-ttu-id="73719-110">如果屬性的值為 **TRUE**，則表示資料流程包含受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="73719-110">If the value of the attribute is **TRUE**, the stream contains protected content.</span></span> <span data-ttu-id="73719-111">如果值為 **FALSE**，或未設定屬性，則資料流程會包含明確的內容。</span><span class="sxs-lookup"><span data-stu-id="73719-111">If the value is **FALSE**, or the attribute is not set, the stream contains clear content.</span></span>

<span data-ttu-id="73719-112">您可以將簡報描述元傳遞給 [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) 函式，而不是檢查這個屬性的每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="73719-112">Instead of checking each stream for this attribute, you can pass a presentation descriptor to the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function.</span></span> <span data-ttu-id="73719-113">此函式會測試簡報描述元是否包含任何受保護的資料流程。</span><span class="sxs-lookup"><span data-stu-id="73719-113">This function tests whether the presentation descriptor contains any protected streams.</span></span>

<span data-ttu-id="73719-114">如果內容需要受保護的媒體路徑 (PMP) ，則媒體來源應該在串流描述項上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="73719-114">A media source should set this attribute on the stream descriptor if the content requires the protected media path (PMP).</span></span>

<span data-ttu-id="73719-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="73719-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="73719-116">範例</span><span class="sxs-lookup"><span data-stu-id="73719-116">Examples</span></span>


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="73719-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="73719-117">Requirements</span></span>



| <span data-ttu-id="73719-118">需求</span><span class="sxs-lookup"><span data-stu-id="73719-118">Requirement</span></span> | <span data-ttu-id="73719-119">值</span><span class="sxs-lookup"><span data-stu-id="73719-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73719-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73719-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73719-121">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73719-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="73719-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73719-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73719-123">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73719-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="73719-124">標頭</span><span class="sxs-lookup"><span data-stu-id="73719-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="73719-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="73719-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73719-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73719-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73719-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="73719-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73719-128">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="73719-128">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="73719-129">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="73719-129">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="73719-130">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="73719-130">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="73719-131">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="73719-131">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




