---
title: IMsRdpClient9 TransportSettings4 屬性
description: 抓取支援 IMsRdpClientTransportSettings4 介面的物件。
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- TransportSettings4 屬性遠端桌面服務
- TransportSettings4 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，TransportSettings4 屬性
- TransportSettings4 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，TransportSettings4 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765d2ad5a50e0608e4c11731742debbaede51737
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317128"
---
# <a name="imsrdpclient9transportsettings4-property"></a><span data-ttu-id="b35d7-108">IMsRdpClient9：： TransportSettings4 屬性</span><span class="sxs-lookup"><span data-stu-id="b35d7-108">IMsRdpClient9::TransportSettings4 property</span></span>

<span data-ttu-id="b35d7-109">抓取支援 [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="b35d7-109">Retrieves an object that supports the [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface.</span></span>

<span data-ttu-id="b35d7-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="b35d7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35d7-111">語法</span><span class="sxs-lookup"><span data-stu-id="b35d7-111">Syntax</span></span>


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a><span data-ttu-id="b35d7-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="b35d7-112">Property value</span></span>

<span data-ttu-id="b35d7-113">傳回 [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="b35d7-113">Returns an [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b35d7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b35d7-114">Requirements</span></span>



| <span data-ttu-id="b35d7-115">需求</span><span class="sxs-lookup"><span data-stu-id="b35d7-115">Requirement</span></span> | <span data-ttu-id="b35d7-116">值</span><span class="sxs-lookup"><span data-stu-id="b35d7-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35d7-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b35d7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b35d7-118">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b35d7-118">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b35d7-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b35d7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b35d7-120">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b35d7-120">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="b35d7-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b35d7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b35d7-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b35d7-122"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="b35d7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b35d7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b35d7-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b35d7-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="b35d7-125">IID</span><span class="sxs-lookup"><span data-stu-id="b35d7-125">IID</span></span><br/>                      | <span data-ttu-id="b35d7-126">CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="b35d7-126">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="b35d7-127">CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="b35d7-127">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="b35d7-128">IID \_ IMsRdpClient9 定義為28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="b35d7-128">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b35d7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b35d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35d7-130">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b35d7-130">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b35d7-131">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b35d7-131">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





