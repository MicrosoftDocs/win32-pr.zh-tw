---
title: IMsRdpClientSecuredSettings2 介面
description: 定義僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項的其他屬性。
ms.assetid: dde9824c-7adf-4783-bb1a-fb2bdbb7aead
ms.tgt_platform: multiple
keywords:
- IMsRdpClientSecuredSettings2 介面遠端桌面服務
- IMsRdpClientSecuredSettings2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ceaf322b51a4b619f8d73a898c444706d61f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969160"
---
# <a name="imsrdpclientsecuredsettings2-interface"></a><span data-ttu-id="19dd6-105">IMsRdpClientSecuredSettings2 介面</span><span class="sxs-lookup"><span data-stu-id="19dd6-105">IMsRdpClientSecuredSettings2 interface</span></span>

<span data-ttu-id="19dd6-106">定義僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="19dd6-106">Defines additional properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="19dd6-107">成員</span><span class="sxs-lookup"><span data-stu-id="19dd6-107">Members</span></span>

<span data-ttu-id="19dd6-108">**IMsRdpClientSecuredSettings2** 介面繼承自 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="19dd6-108">The **IMsRdpClientSecuredSettings2** interface inherits from [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md).</span></span> <span data-ttu-id="19dd6-109">**IMsRdpClientSecuredSettings2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="19dd6-109">**IMsRdpClientSecuredSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="19dd6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="19dd6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19dd6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="19dd6-111">Properties</span></span>

<span data-ttu-id="19dd6-112">**IMsRdpClientSecuredSettings2** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="19dd6-112">The **IMsRdpClientSecuredSettings2** interface has these properties.</span></span>



| <span data-ttu-id="19dd6-113">屬性</span><span class="sxs-lookup"><span data-stu-id="19dd6-113">Property</span></span>                                                   | <span data-ttu-id="19dd6-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="19dd6-114">Access type</span></span>           | <span data-ttu-id="19dd6-115">Description</span><span class="sxs-lookup"><span data-stu-id="19dd6-115">Description</span></span>                                                                                                          |
|:-----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19dd6-116">**Pcb**</span><span class="sxs-lookup"><span data-stu-id="19dd6-116">**PCB**</span></span>](imsrdpclientsecuredsettings2-pcb.md)<br/> | <span data-ttu-id="19dd6-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19dd6-117">Read/write</span></span><br/> | <span data-ttu-id="19dd6-118">指定 preconnection BLOB (PCB) 設定，以在連接到伺服器之前使用。</span><span class="sxs-lookup"><span data-stu-id="19dd6-118">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19dd6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="19dd6-119">Requirements</span></span>



| <span data-ttu-id="19dd6-120">需求</span><span class="sxs-lookup"><span data-stu-id="19dd6-120">Requirement</span></span> | <span data-ttu-id="19dd6-121">值</span><span class="sxs-lookup"><span data-stu-id="19dd6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19dd6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19dd6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19dd6-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19dd6-123">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="19dd6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19dd6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19dd6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19dd6-125">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="19dd6-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="19dd6-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="19dd6-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19dd6-127"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="19dd6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="19dd6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19dd6-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19dd6-129"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="19dd6-130">IID</span><span class="sxs-lookup"><span data-stu-id="19dd6-130">IID</span></span><br/>                      | <span data-ttu-id="19dd6-131">IID \_ IMsRdpClientSecuredSettings 定義為 25f2ce20-8b1d-4971-a7cd-549dae201fc0</span><span class="sxs-lookup"><span data-stu-id="19dd6-131">IID\_IMsRdpClientSecuredSettings is defined as 25f2ce20-8b1d-4971-a7cd-549dae201fc0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19dd6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19dd6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19dd6-133">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="19dd6-133">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





