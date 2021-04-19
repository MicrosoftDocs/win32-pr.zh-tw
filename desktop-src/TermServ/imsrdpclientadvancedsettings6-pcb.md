---
title: IMsRdpClientAdvancedSettings6 PCB 屬性
description: 指定 preconnection BLOB (PCB) 設定，以在連接到伺服器之前使用。 |IMsRdpClientAdvancedSettings6 PCB 屬性
ms.assetid: 3f3e6f09-2c26-44ab-9bcc-2636b71b57e2
ms.tgt_platform: multiple
keywords:
- PCB 屬性遠端桌面服務
- PCB 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，PCB 屬性
- PCB 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，PCB 屬性
- PCB 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，PCB 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.PCB
- IMsRdpClientAdvancedSettings6.get_PCB
- IMsRdpClientAdvancedSettings6.put_PCB
- IMsRdpClientAdvancedSettings7.PCB
- IMsRdpClientAdvancedSettings7.get_PCB
- IMsRdpClientAdvancedSettings7.put_PCB
- IMsRdpClientAdvancedSettings8.PCB
- IMsRdpClientAdvancedSettings8.get_PCB
- IMsRdpClientAdvancedSettings8.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da9cfa12ec944ea8f745ec3399c2a53f6b7c6b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106985837"
---
# <a name="imsrdpclientadvancedsettings6pcb-property"></a><span data-ttu-id="65e92-111">IMsRdpClientAdvancedSettings6：:P CB 屬性</span><span class="sxs-lookup"><span data-stu-id="65e92-111">IMsRdpClientAdvancedSettings6::PCB property</span></span>

<span data-ttu-id="65e92-112">指定 preconnection BLOB (PCB) 設定，以在連接到伺服器之前使用。</span><span class="sxs-lookup"><span data-stu-id="65e92-112">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="65e92-113">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="65e92-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e92-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="65e92-114">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *pbstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="65e92-115">屬性值</span><span class="sxs-lookup"><span data-stu-id="65e92-115">Property value</span></span>

<span data-ttu-id="65e92-116">指定要在連接之前使用的 BLOB 設定。</span><span class="sxs-lookup"><span data-stu-id="65e92-116">Specifies the BLOB setting to use prior to connecting.</span></span>

## <a name="remarks"></a><span data-ttu-id="65e92-117">備註</span><span class="sxs-lookup"><span data-stu-id="65e92-117">Remarks</span></span>

<span data-ttu-id="65e92-118">只有遠端桌面連線6.1 和7.0 用戶端支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="65e92-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

<span data-ttu-id="65e92-119">伺服器會使用 BLOB 設定來識別連接的目標進程。</span><span class="sxs-lookup"><span data-stu-id="65e92-119">The server uses the BLOB setting to identify the target process for the connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e92-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="65e92-120">Requirements</span></span>



| <span data-ttu-id="65e92-121">需求</span><span class="sxs-lookup"><span data-stu-id="65e92-121">Requirement</span></span> | <span data-ttu-id="65e92-122">值</span><span class="sxs-lookup"><span data-stu-id="65e92-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e92-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65e92-123">Minimum supported client</span></span><br/> | <span data-ttu-id="65e92-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65e92-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="65e92-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65e92-125">Minimum supported server</span></span><br/> | <span data-ttu-id="65e92-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65e92-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="65e92-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="65e92-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="65e92-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65e92-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="65e92-129">DLL</span><span class="sxs-lookup"><span data-stu-id="65e92-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65e92-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65e92-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="65e92-131">IID</span><span class="sxs-lookup"><span data-stu-id="65e92-131">IID</span></span><br/>                      | <span data-ttu-id="65e92-132">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="65e92-132">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65e92-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65e92-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e92-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="65e92-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="65e92-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="65e92-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="65e92-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="65e92-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





