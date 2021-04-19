---
title: IMsRdpDeviceV2 CmClassGuid 屬性
description: 包含裝置的 configuration manager 安裝類別 GUID。
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- CmClassGuid 屬性遠端桌面服務
- CmClassGuid 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，CmClassGuid 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969135"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a><span data-ttu-id="121a2-106">IMsRdpDeviceV2：： CmClassGuid 屬性</span><span class="sxs-lookup"><span data-stu-id="121a2-106">IMsRdpDeviceV2::CmClassGuid property</span></span>

<span data-ttu-id="121a2-107">包含裝置的 configuration manager 安裝類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="121a2-107">Contains the configuration manager setup class GUID for the device.</span></span>

<span data-ttu-id="121a2-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="121a2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="121a2-109">語法</span><span class="sxs-lookup"><span data-stu-id="121a2-109">Syntax</span></span>


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a><span data-ttu-id="121a2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="121a2-110">Property value</span></span>

<span data-ttu-id="121a2-111">裝置的 configuration manager 安裝類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="121a2-111">The configuration manager setup class GUID for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="121a2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="121a2-112">Requirements</span></span>



| <span data-ttu-id="121a2-113">需求</span><span class="sxs-lookup"><span data-stu-id="121a2-113">Requirement</span></span> | <span data-ttu-id="121a2-114">值</span><span class="sxs-lookup"><span data-stu-id="121a2-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="121a2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="121a2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="121a2-116">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="121a2-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="121a2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="121a2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="121a2-118">Windows Server 2008 R2 包含 SP1</span><span class="sxs-lookup"><span data-stu-id="121a2-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="121a2-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="121a2-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="121a2-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="121a2-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="121a2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="121a2-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="121a2-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="121a2-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="121a2-123">IID</span><span class="sxs-lookup"><span data-stu-id="121a2-123">IID</span></span><br/>                      | <span data-ttu-id="121a2-124">IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="121a2-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="121a2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="121a2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="121a2-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="121a2-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





