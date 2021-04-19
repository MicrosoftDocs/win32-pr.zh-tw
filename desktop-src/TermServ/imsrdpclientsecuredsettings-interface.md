---
title: IMsRdpClientSecuredSettings 介面
description: 包含方法，可取得並設定僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項屬性。 |IMsRdpClientSecuredSettings 介面
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- IMsRdpClientSecuredSettings 介面遠端桌面服務
- IMsRdpClientSecuredSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991422"
---
# <a name="imsrdpclientsecuredsettings-interface"></a><span data-ttu-id="567f2-106">IMsRdpClientSecuredSettings 介面</span><span class="sxs-lookup"><span data-stu-id="567f2-106">IMsRdpClientSecuredSettings interface</span></span>

<span data-ttu-id="567f2-107">包含方法，可取得並設定僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="567f2-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="567f2-108">成員</span><span class="sxs-lookup"><span data-stu-id="567f2-108">Members</span></span>

<span data-ttu-id="567f2-109">**IMsRdpClientSecuredSettings** 介面繼承自 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="567f2-109">The **IMsRdpClientSecuredSettings** interface inherits from [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span> <span data-ttu-id="567f2-110">**IMsRdpClientSecuredSettings** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="567f2-110">**IMsRdpClientSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="567f2-111">屬性</span><span class="sxs-lookup"><span data-stu-id="567f2-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="567f2-112">屬性</span><span class="sxs-lookup"><span data-stu-id="567f2-112">Properties</span></span>

<span data-ttu-id="567f2-113">**IMsRdpClientSecuredSettings** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="567f2-113">The **IMsRdpClientSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="567f2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="567f2-114">Property</span></span>                                                                                   | <span data-ttu-id="567f2-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="567f2-115">Access type</span></span>           | <span data-ttu-id="567f2-116">Description</span><span class="sxs-lookup"><span data-stu-id="567f2-116">Description</span></span>                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="567f2-117">**AudioRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="567f2-117">**AudioRedirectionMode**</span></span>](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | <span data-ttu-id="567f2-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="567f2-118">Read/write</span></span><br/> | <span data-ttu-id="567f2-119">音訊重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="567f2-119">The audio redirection settings.</span></span><br/>    |
| [<span data-ttu-id="567f2-120">**KeyboardHookMode**</span><span class="sxs-lookup"><span data-stu-id="567f2-120">**KeyboardHookMode**</span></span>](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | <span data-ttu-id="567f2-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="567f2-121">Read/write</span></span><br/> | <span data-ttu-id="567f2-122">鍵盤重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="567f2-122">The keyboard redirection settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="567f2-123">備註</span><span class="sxs-lookup"><span data-stu-id="567f2-123">Remarks</span></span>

<span data-ttu-id="567f2-124">連接控制項時無法設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="567f2-124">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="567f2-125">如需此介面之方法的詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。</span><span class="sxs-lookup"><span data-stu-id="567f2-125">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="567f2-126">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="567f2-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="567f2-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="567f2-127">Requirements</span></span>



| <span data-ttu-id="567f2-128">需求</span><span class="sxs-lookup"><span data-stu-id="567f2-128">Requirement</span></span> | <span data-ttu-id="567f2-129">值</span><span class="sxs-lookup"><span data-stu-id="567f2-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="567f2-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="567f2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="567f2-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="567f2-131">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="567f2-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="567f2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="567f2-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="567f2-133">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="567f2-134">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="567f2-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="567f2-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="567f2-135"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="567f2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="567f2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="567f2-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="567f2-137"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="567f2-138">IID</span><span class="sxs-lookup"><span data-stu-id="567f2-138">IID</span></span><br/>                      | <span data-ttu-id="567f2-139">IID \_ IMsRdpClientSecuredSettings 定義為605befcf-39c1-45cc-a811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="567f2-139">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="567f2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="567f2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="567f2-141">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="567f2-141">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="567f2-142">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="567f2-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





