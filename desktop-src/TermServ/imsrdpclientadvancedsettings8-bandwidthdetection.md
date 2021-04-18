---
title: IMsRdpClientAdvancedSettings8 BandwidthDetection 屬性
description: 指定是否自動偵測頻寬變更。
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- BandwidthDetection 屬性遠端桌面服務
- BandwidthDetection 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，BandwidthDetection 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f915aeff1159e675026cfc13906e69c96208f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965479"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a><span data-ttu-id="df74d-106">IMsRdpClientAdvancedSettings8：： BandwidthDetection 屬性</span><span class="sxs-lookup"><span data-stu-id="df74d-106">IMsRdpClientAdvancedSettings8::BandwidthDetection property</span></span>

<span data-ttu-id="df74d-107">指定是否自動偵測頻寬變更。</span><span class="sxs-lookup"><span data-stu-id="df74d-107">Specifies if bandwidth changes are automatically detected.</span></span>

<span data-ttu-id="df74d-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="df74d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="df74d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="df74d-109">Syntax</span></span>


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a><span data-ttu-id="df74d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="df74d-110">Property value</span></span>

<span data-ttu-id="df74d-111">**變異 \_** 如果自動偵測到頻寬變更，則為 TRUE，否則為 **VARIANT \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="df74d-111">**VARIANT\_TRUE** if bandwidth changes are automatically detected or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="df74d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="df74d-112">Requirements</span></span>



| <span data-ttu-id="df74d-113">需求</span><span class="sxs-lookup"><span data-stu-id="df74d-113">Requirement</span></span> | <span data-ttu-id="df74d-114">值</span><span class="sxs-lookup"><span data-stu-id="df74d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df74d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df74d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="df74d-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="df74d-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="df74d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df74d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="df74d-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="df74d-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="df74d-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="df74d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="df74d-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df74d-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df74d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="df74d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df74d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df74d-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df74d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df74d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df74d-124">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="df74d-124">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





