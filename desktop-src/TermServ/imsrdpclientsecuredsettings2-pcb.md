---
title: IMsRdpClientSecuredSettings2 PCB 屬性
description: 指定 preconnection BLOB (PCB) 設定，以在連接到伺服器之前使用。 |IMsRdpClientSecuredSettings2 PCB 屬性
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- PCB 屬性遠端桌面服務
- PCB 屬性遠端桌面服務，IMsRdpClientSecuredSettings2 介面
- IMsRdpClientSecuredSettings2 介面遠端桌面服務，PCB 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981980"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a><span data-ttu-id="1d54a-107">IMsRdpClientSecuredSettings2：:P CB 屬性</span><span class="sxs-lookup"><span data-stu-id="1d54a-107">IMsRdpClientSecuredSettings2::PCB property</span></span>

<span data-ttu-id="1d54a-108">指定 preconnection BLOB (PCB) 設定，以在連接到伺服器之前使用。</span><span class="sxs-lookup"><span data-stu-id="1d54a-108">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="1d54a-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d54a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d54a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d54a-110">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="1d54a-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="1d54a-111">Property value</span></span>

<span data-ttu-id="1d54a-112">PCB 設定。</span><span class="sxs-lookup"><span data-stu-id="1d54a-112">The PCB setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d54a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d54a-113">Requirements</span></span>



| <span data-ttu-id="1d54a-114">需求</span><span class="sxs-lookup"><span data-stu-id="1d54a-114">Requirement</span></span> | <span data-ttu-id="1d54a-115">值</span><span class="sxs-lookup"><span data-stu-id="1d54a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d54a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d54a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1d54a-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d54a-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="1d54a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d54a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1d54a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d54a-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1d54a-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1d54a-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d54a-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d54a-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d54a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1d54a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d54a-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d54a-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d54a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d54a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d54a-125">**IMsRdpClientSecuredSettings2**</span><span class="sxs-lookup"><span data-stu-id="1d54a-125">**IMsRdpClientSecuredSettings2**</span></span>](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





