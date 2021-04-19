---
description: 指定以硬體為基礎的媒體基礎轉換 (MFT) 是否已連線到另一個以硬體為基礎的 MFT。
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: 'MFT_CONNECTED_TO_HW_STREAM 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995827"
---
# <a name="mft_connected_to_hw_stream-attribute"></a><span data-ttu-id="18b87-103">\_連接 \_ 至 \_ HW \_ STREAM 屬性的 MFT</span><span class="sxs-lookup"><span data-stu-id="18b87-103">MFT\_CONNECTED\_TO\_HW\_STREAM attribute</span></span>

<span data-ttu-id="18b87-104">指定以硬體為基礎的媒體基礎轉換 (MFT) 是否已連線到另一個以硬體為基礎的 MFT。</span><span class="sxs-lookup"><span data-stu-id="18b87-104">Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.</span></span>

## <a name="data-type"></a><span data-ttu-id="18b87-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="18b87-105">Data type</span></span>

<span data-ttu-id="18b87-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="18b87-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="18b87-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="18b87-107">Get/set</span></span>

<span data-ttu-id="18b87-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="18b87-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="18b87-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="18b87-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="18b87-110">備註</span><span class="sxs-lookup"><span data-stu-id="18b87-110">Remarks</span></span>

<span data-ttu-id="18b87-111">應用程式通常不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="18b87-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="18b87-112">這個屬性會與以硬體為基礎的 MFTs 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="18b87-112">This attribute is used with hardware-based MFTs.</span></span> <span data-ttu-id="18b87-113">當兩個硬體 MFTs 在拓撲內連接時，拓撲載入器會在下列物件上將此屬性設定為 **TRUE** ：</span><span class="sxs-lookup"><span data-stu-id="18b87-113">When two hardware MFTs are connected within a topology, the topology loader sets this attribute to **TRUE** on the following objects:</span></span>

-   <span data-ttu-id="18b87-114">上游 MFT 的輸出資料流程</span><span class="sxs-lookup"><span data-stu-id="18b87-114">The output stream of the upstream MFT</span></span>
-   <span data-ttu-id="18b87-115">下游 MFT 的輸入資料流程</span><span class="sxs-lookup"><span data-stu-id="18b87-115">The input stream of the downstream MFT</span></span>

<span data-ttu-id="18b87-116">為了取得輸出資料流程的屬性存放區，拓撲載入器會呼叫上游 MFT 上的 [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) 。</span><span class="sxs-lookup"><span data-stu-id="18b87-116">To get the attribute store for the output stream, the topology loader calls [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) on the upstream MFT.</span></span> <span data-ttu-id="18b87-117">為了取得輸入資料流程的屬性存放區，拓撲載入器會在下游 MFT 上呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) 。</span><span class="sxs-lookup"><span data-stu-id="18b87-117">To get the attribute store for the input stream, the topology loader calls [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) on the downstream MFT.</span></span>

<span data-ttu-id="18b87-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="18b87-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="18b87-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="18b87-119">Requirements</span></span>



| <span data-ttu-id="18b87-120">需求</span><span class="sxs-lookup"><span data-stu-id="18b87-120">Requirement</span></span> | <span data-ttu-id="18b87-121">值</span><span class="sxs-lookup"><span data-stu-id="18b87-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b87-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18b87-122">Minimum supported client</span></span><br/> | <span data-ttu-id="18b87-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18b87-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="18b87-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18b87-124">Minimum supported server</span></span><br/> | <span data-ttu-id="18b87-125">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18b87-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="18b87-126">標頭</span><span class="sxs-lookup"><span data-stu-id="18b87-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="18b87-127"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="18b87-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18b87-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18b87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b87-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="18b87-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18b87-130">硬體 MFTs</span><span class="sxs-lookup"><span data-stu-id="18b87-130">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="18b87-131">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="18b87-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




