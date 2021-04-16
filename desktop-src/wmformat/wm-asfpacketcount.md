---
title: WM/ASFPacketCount
description: WM/ASFPacketCount 屬性包含 ASF 檔案的 data 區段中的封包計數。
ms.assetid: 97035a4e-4de9-4c9e-9288-addf6eccddc7
keywords:
- WM/ASFPacketCount windows Media 格式
topic_type:
- apiref
api_name:
- WM/ASFPacketCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59667e2895164ddfdb2ed688c55ac424315cd822
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507780"
---
# <a name="wmasfpacketcount"></a><span data-ttu-id="abc46-104">WM/ASFPacketCount</span><span class="sxs-lookup"><span data-stu-id="abc46-104">WM/ASFPacketCount</span></span>

<span data-ttu-id="abc46-105">**WM/ASFPacketCount** 屬性包含 ASF 檔案的 data 區段中的封包計數。</span><span class="sxs-lookup"><span data-stu-id="abc46-105">The **WM/ASFPacketCount** attribute contains a count of the packets in the data section of the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="abc46-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="abc46-106">Global Constant</span></span>

<span data-ttu-id="abc46-107">g \_ wszWMASFPacketCount</span><span class="sxs-lookup"><span data-stu-id="abc46-107">g\_wszWMASFPacketCount</span></span>

## <a name="data-type"></a><span data-ttu-id="abc46-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="abc46-108">Data Type</span></span>

<span data-ttu-id="abc46-109">**WMT \_ 類型 \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="abc46-109">**WMT\_TYPE\_QWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="abc46-110">備註</span><span class="sxs-lookup"><span data-stu-id="abc46-110">Remarks</span></span>

<span data-ttu-id="abc46-111">這個屬性是唯讀的，而且會套用至整個檔案 (stream 0) 。</span><span class="sxs-lookup"><span data-stu-id="abc46-111">This attribute is read-only, and applies to the entire file (stream 0).</span></span>

<span data-ttu-id="abc46-112">您只能從中繼資料編輯器物件使用 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面的方法，以抓取此屬性。</span><span class="sxs-lookup"><span data-stu-id="abc46-112">You can only retrieve this attribute by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface from the metadata editor object.</span></span>

## <a name="see-also"></a><span data-ttu-id="abc46-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abc46-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc46-114">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="abc46-114">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




