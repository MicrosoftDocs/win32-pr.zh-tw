---
description: 指定範例上的原始裝置時間戳記。
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: 'MFSampleExtension_DeviceReferenceSystemTime 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848445"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a><span data-ttu-id="2453e-103">MFSampleExtension \_ DeviceReferenceSystemTime 屬性</span><span class="sxs-lookup"><span data-stu-id="2453e-103">MFSampleExtension\_DeviceReferenceSystemTime attribute</span></span>

<span data-ttu-id="2453e-104">指定範例上的原始裝置時間戳記。</span><span class="sxs-lookup"><span data-stu-id="2453e-104">Specifies the original device timestamp on the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="2453e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="2453e-105">Data type</span></span>

<span data-ttu-id="2453e-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="2453e-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="2453e-107">備註</span><span class="sxs-lookup"><span data-stu-id="2453e-107">Remarks</span></span>

<span data-ttu-id="2453e-108">這是媒體範例的裝置參考時間戳記（以100ns 解析）。</span><span class="sxs-lookup"><span data-stu-id="2453e-108">This is the a device reference time stamp of media samples in 100ns resolution.</span></span> <span data-ttu-id="2453e-109">根據產生範例的來源而定，此時間戳記不一定會包含查詢效能計數器的實際值 (QPC) 。</span><span class="sxs-lookup"><span data-stu-id="2453e-109">This time stamp may or may not carry the actual value of the query performance counter (QPC), depending on the source producing the samples.</span></span> <span data-ttu-id="2453e-110">媒體管線中的其他元件可能會修改此值。</span><span class="sxs-lookup"><span data-stu-id="2453e-110">This value may be modified by other components in the media pipeline.</span></span> <span data-ttu-id="2453e-111">MFTs 插入至 capture 管線時無法使用這個值。</span><span class="sxs-lookup"><span data-stu-id="2453e-111">This value is not available to MFTs inserted into the capture pipeline.</span></span>

## <a name="requirements"></a><span data-ttu-id="2453e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2453e-112">Requirements</span></span>



| <span data-ttu-id="2453e-113">需求</span><span class="sxs-lookup"><span data-stu-id="2453e-113">Requirement</span></span> | <span data-ttu-id="2453e-114">值</span><span class="sxs-lookup"><span data-stu-id="2453e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2453e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2453e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2453e-116">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2453e-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="2453e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2453e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2453e-118">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2453e-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2453e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2453e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2453e-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="2453e-120"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="2453e-121">Idl</span><span class="sxs-lookup"><span data-stu-id="2453e-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2453e-122"><dt>Mfcaptureengine .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2453e-122"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2453e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2453e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2453e-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2453e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




