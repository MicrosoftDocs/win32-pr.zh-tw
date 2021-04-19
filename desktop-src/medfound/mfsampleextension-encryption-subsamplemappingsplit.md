---
description: 設定範例的子樣本對應，指出範例資料中的明確和加密的位元組。
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: 'MFSampleExtension_Encryption_SubSampleMappingSplit 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986806"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a><span data-ttu-id="c9637-103">MFSampleExtension \_ Encryption \_ SubSampleMappingSplit 屬性</span><span class="sxs-lookup"><span data-stu-id="c9637-103">MFSampleExtension\_Encryption\_SubSampleMappingSplit attribute</span></span>

<span data-ttu-id="c9637-104">設定範例的子樣本對應，指出範例資料中的明確和加密的位元組。</span><span class="sxs-lookup"><span data-stu-id="c9637-104">Sets the sub-sample mapping for the sample indicating the clear and encrypted bytes in the sample data.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9637-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c9637-105">Data type</span></span>

<span data-ttu-id="c9637-106">**Blob**</span><span class="sxs-lookup"><span data-stu-id="c9637-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="c9637-107">備註</span><span class="sxs-lookup"><span data-stu-id="c9637-107">Remarks</span></span>

<span data-ttu-id="c9637-108">**BLOB** 應該包含位元組範圍的陣列，做為 dword，其中每兩個 dword 都會進行設定。</span><span class="sxs-lookup"><span data-stu-id="c9637-108">The **BLOB** should contain an array of byte ranges as DWORDs where every two DWORDs makes a set.</span></span> <span data-ttu-id="c9637-109">每個集合中的第一個 DWORD 是清除位元組的數目，而集合的第二個 dword 是已加密的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="c9637-109">The first DWORD in each set is the number of clear bytes and the second DWORD of the set is the number of encrypted bytes.</span></span> <span data-ttu-id="c9637-110">請注意，0對0不是有效的集合 (其中一個值可以是0，但不是兩個) 。</span><span class="sxs-lookup"><span data-stu-id="c9637-110">Note that a pair of 0s is not a valid set (either value can be 0, but not both).</span></span> <span data-ttu-id="c9637-111">位元組範圍陣列指出要解密的範圍，包括整個範例不應解密的可能性。</span><span class="sxs-lookup"><span data-stu-id="c9637-111">The array of byte ranges indicate which ranges to decrypt, including the possibility that the entire sample should not be decrypted.</span></span> <span data-ttu-id="c9637-112">建議您不要在清除範例上設定這項功能，雖然您可以使用適當的值來設定相同的結果來達到相同的結果。</span><span class="sxs-lookup"><span data-stu-id="c9637-112">It is recommended that this should not be set on clear samples, though it is possible to achieve the same result by setting it with the appropriate values.</span></span>

## <a name="examples"></a><span data-ttu-id="c9637-113">範例</span><span class="sxs-lookup"><span data-stu-id="c9637-113">Examples</span></span>

<span data-ttu-id="c9637-114">下列範例顯示如何設定 MFSampleExtension \_ 加密 \_ SubSampleMappingSplit。</span><span class="sxs-lookup"><span data-stu-id="c9637-114">The following example shows how to set MFSampleExtension\_Encryption\_SubSampleMappingSplit.</span></span>


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a><span data-ttu-id="c9637-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9637-115">Requirements</span></span>



| <span data-ttu-id="c9637-116">需求</span><span class="sxs-lookup"><span data-stu-id="c9637-116">Requirement</span></span> | <span data-ttu-id="c9637-117">值</span><span class="sxs-lookup"><span data-stu-id="c9637-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9637-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9637-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9637-119">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9637-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="c9637-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9637-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9637-121">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9637-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c9637-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c9637-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9637-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9637-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9637-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9637-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9637-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c9637-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9637-126">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="c9637-126">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="c9637-127">MFSampleExtension \_ 內容 \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="c9637-127">MFSampleExtension\_Content\_KeyID</span></span>](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




