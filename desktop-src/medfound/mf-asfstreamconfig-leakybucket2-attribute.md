---
description: 設定尖峰 &\# 0034; 有漏洞 bucket&\# 0034; 參數 (請參閱備註) ，以編碼 Windows Media 檔案。 這些參數會用於尖峰位元速率。 使用 IMFASFStreamConfig 介面設定這個屬性。
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: 'MF_ASFSTREAMCONFIG_LEAKYBUCKET2 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990327"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a><span data-ttu-id="7c361-105">MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2 屬性</span><span class="sxs-lookup"><span data-stu-id="7c361-105">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2 attribute</span></span>

<span data-ttu-id="7c361-106">設定尖峰 "有漏洞 bucket" 參數 (請參閱備註) 來編碼 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="7c361-106">Sets the peak "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="7c361-107">這些參數會用於尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="7c361-107">These parameters are used for the peak bit rate.</span></span> <span data-ttu-id="7c361-108">使用 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="7c361-108">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c361-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="7c361-109">Data type</span></span>

<span data-ttu-id="7c361-110">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="7c361-110">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="7c361-111">備註</span><span class="sxs-lookup"><span data-stu-id="7c361-111">Remarks</span></span>

<span data-ttu-id="7c361-112">這個屬性的值是三個 **DWORD** 的陣列，順序如下：</span><span class="sxs-lookup"><span data-stu-id="7c361-112">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="7c361-113">位元速率，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="7c361-113">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="7c361-114">緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7c361-114">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="7c361-115">初始緩衝區飽和度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7c361-115">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="7c361-116">如需有關有漏洞 bucket 概念的詳細資訊，請參閱 Windows Media Format SDK 檔中 [的有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="7c361-116">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="7c361-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="7c361-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c361-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c361-118">Requirements</span></span>



| <span data-ttu-id="7c361-119">需求</span><span class="sxs-lookup"><span data-stu-id="7c361-119">Requirement</span></span> | <span data-ttu-id="7c361-120">值</span><span class="sxs-lookup"><span data-stu-id="7c361-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c361-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c361-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c361-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c361-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7c361-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c361-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c361-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c361-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7c361-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7c361-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c361-126"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c361-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c361-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c361-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c361-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7c361-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c361-129">ASF 屬性</span><span class="sxs-lookup"><span data-stu-id="7c361-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c361-130">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="7c361-130">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="7c361-131">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="7c361-131">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="7c361-132">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="7c361-132">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




