---
description: 設定平均 &\# 0034; 有漏洞 bucket&\# 0034; 參數 (請參閱備註) ，以編碼 Windows Media 檔案。 使用 IMFASFStreamConfig 介面設定這個屬性。
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: 'MF_ASFSTREAMCONFIG_LEAKYBUCKET1 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982325"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a><span data-ttu-id="5e9cb-104">MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1 屬性</span><span class="sxs-lookup"><span data-stu-id="5e9cb-104">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1 attribute</span></span>

<span data-ttu-id="5e9cb-105">設定「有漏洞值區」的平均參數 (查看針對 Windows Media 檔案進行編碼的備註) 。</span><span class="sxs-lookup"><span data-stu-id="5e9cb-105">Sets the average "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="5e9cb-106">使用 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5e9cb-106">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e9cb-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="5e9cb-107">Data type</span></span>

<span data-ttu-id="5e9cb-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="5e9cb-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="5e9cb-109">備註</span><span class="sxs-lookup"><span data-stu-id="5e9cb-109">Remarks</span></span>

<span data-ttu-id="5e9cb-110">這個屬性的值是三個 **DWORD** 的陣列，順序如下：</span><span class="sxs-lookup"><span data-stu-id="5e9cb-110">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="5e9cb-111">位元速率，以每秒位數為單位。</span><span class="sxs-lookup"><span data-stu-id="5e9cb-111">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="5e9cb-112">緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5e9cb-112">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="5e9cb-113">初始緩衝區飽和度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5e9cb-113">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="5e9cb-114">如需有關有漏洞 bucket 概念的詳細資訊，請參閱 Windows Media Format SDK 檔中 [的有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="5e9cb-114">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="5e9cb-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5e9cb-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9cb-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e9cb-116">Requirements</span></span>



| <span data-ttu-id="5e9cb-117">需求</span><span class="sxs-lookup"><span data-stu-id="5e9cb-117">Requirement</span></span> | <span data-ttu-id="5e9cb-118">值</span><span class="sxs-lookup"><span data-stu-id="5e9cb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9cb-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e9cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5e9cb-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e9cb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5e9cb-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e9cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5e9cb-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e9cb-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e9cb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5e9cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e9cb-124"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e9cb-124"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e9cb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e9cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9cb-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5e9cb-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e9cb-127">ASF 屬性</span><span class="sxs-lookup"><span data-stu-id="5e9cb-127">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e9cb-128">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="5e9cb-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="5e9cb-129">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="5e9cb-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="5e9cb-130">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="5e9cb-130">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




