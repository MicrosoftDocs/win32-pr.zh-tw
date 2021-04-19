---
description: 指出範例中的 NALUs 長度。 這是在對 h.264 解碼器壓縮的輸入範例上設定的 MF BLOB。
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: 'MF_NALU_LENGTH_INFORMATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992029"
---
# <a name="mf_nalu_length_information-attribute"></a><span data-ttu-id="7c916-104">MF \_ NALU \_ 長度 \_ 資訊屬性</span><span class="sxs-lookup"><span data-stu-id="7c916-104">MF\_NALU\_LENGTH\_INFORMATION attribute</span></span>

<span data-ttu-id="7c916-105">指出範例中的 NALUs 長度。</span><span class="sxs-lookup"><span data-stu-id="7c916-105">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="7c916-106">這是在對 h.264 解碼器壓縮的輸入範例上設定的 MF **BLOB** 。</span><span class="sxs-lookup"><span data-stu-id="7c916-106">This is a MF **BLOB** that is set on compressed input samples to the H.264 decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c916-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="7c916-107">Data type</span></span>

<span data-ttu-id="7c916-108">**Blob**</span><span class="sxs-lookup"><span data-stu-id="7c916-108">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="7c916-109">備註</span><span class="sxs-lookup"><span data-stu-id="7c916-109">Remarks</span></span>

<span data-ttu-id="7c916-110">若要設定此屬性，媒體的類型必須是 MEDIASUBTYPE \_ H264，而且必須在 MEDIASUBTYPE H264 的輸入媒體類型上設定 [ [MF \_ NALU \_ 長度] \_ 設定](mf-nalu-length-set.md) 屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7c916-110">In order for this attribute to be set, the media must be of type MEDIASUBTYPE\_H264 and the [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) attribute must be set on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="7c916-111">在 \_ \_ 輸入範例上將 MF NALU 長度資訊設定 \_ 為 **BLOB** ，範例中的每個 NALU 都有一個 DWORD。</span><span class="sxs-lookup"><span data-stu-id="7c916-111">Set MF\_NALU\_LENGTH\_INFORMATION as a **BLOB** on the input sample, with one DWORD for each NALU in the sample.</span></span> <span data-ttu-id="7c916-112">例如，如果有 AUD (9 個位元組) ，SPS (25 個位元組) 、PPS (10 個位元組) 、IDR slice1 (50 k) 、IDR 配量 2 (60 k) ，然後在 **BLOB** 中應該會有5個具有值9、25、10、50 k、60 k 的 dword。</span><span class="sxs-lookup"><span data-stu-id="7c916-112">For example, if there are AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), IDR slice 2 (60 k), then there should be 5 DWORDs with values 9, 25, 10, 50 k, 60 k in the **BLOB**.</span></span>

<span data-ttu-id="7c916-113">以下是設定 **blob** 的一些程式碼，其中 **rgdwNALULengthInfo** 是 DWORD 類型的陣列，而 **UiNaluLengthIdx** 則是設定為 **BLOB** 的有效 NALU 長度。</span><span class="sxs-lookup"><span data-stu-id="7c916-113">Here some code that sets the **BLOB**, where **rgdwNALULengthInfo** is an array of type DWORD and **uiNaluLengthIdx** is the valid NALU lengths set to the **BLOB**.</span></span>


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a><span data-ttu-id="7c916-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c916-114">Requirements</span></span>



| <span data-ttu-id="7c916-115">需求</span><span class="sxs-lookup"><span data-stu-id="7c916-115">Requirement</span></span> | <span data-ttu-id="7c916-116">值</span><span class="sxs-lookup"><span data-stu-id="7c916-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c916-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c916-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c916-118">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c916-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7c916-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c916-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c916-120">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c916-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7c916-121">標頭</span><span class="sxs-lookup"><span data-stu-id="7c916-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c916-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c916-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c916-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c916-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c916-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7c916-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c916-125">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="7c916-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




