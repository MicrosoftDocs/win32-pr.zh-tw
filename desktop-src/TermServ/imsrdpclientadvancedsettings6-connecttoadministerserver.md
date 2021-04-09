---
title: IMsRdpClientAdvancedSettings6 ConnectToAdministerServer 屬性
description: 取得或指定 ActiveX 控制項是否應該基於系統管理目的嘗試連接至伺服器。
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- ConnectToAdministerServer 屬性遠端桌面服務
- ConnectToAdministerServer 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ConnectToAdministerServer 屬性
- ConnectToAdministerServer 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ConnectToAdministerServer 屬性
- ConnectToAdministerServer 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ConnectToAdministerServer 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025102"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a><span data-ttu-id="a4e0c-110">IMsRdpClientAdvancedSettings6：： ConnectToAdministerServer 屬性</span><span class="sxs-lookup"><span data-stu-id="a4e0c-110">IMsRdpClientAdvancedSettings6::ConnectToAdministerServer property</span></span>

<span data-ttu-id="a4e0c-111">取得或指定 ActiveX 控制項是否應該基於系統管理目的嘗試連接至伺服器。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-111">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span>

<span data-ttu-id="a4e0c-112">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e0c-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4e0c-113">Syntax</span></span>


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a><span data-ttu-id="a4e0c-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="a4e0c-114">Property value</span></span>

<span data-ttu-id="a4e0c-115">**變異 \_TRUE** 表示讓 ActiveX 控制項基於系統管理目的嘗試連接到伺服器;否則 **\_ 為 VARIANT FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-115">**VARIANT\_TRUE** to cause the ActiveX control to attempt to connect to the server for administrative purposes; otherwise **VARIANT\_FALSE**.</span></span> <span data-ttu-id="a4e0c-116">預設值為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-116">The default value is **VARIANT\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4e0c-117">備註</span><span class="sxs-lookup"><span data-stu-id="a4e0c-117">Remarks</span></span>

<span data-ttu-id="a4e0c-118">若要使用 **ConnectToAdministerServer**，您必須執行遠端桌面連線 (RDC) 用戶端6.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-118">To use **ConnectToAdministerServer**, you must be running Remote Desktop Connection (RDC) client version 6.1 or later.</span></span>

> [!Note]  
> <span data-ttu-id="a4e0c-119">RDC 6.1 版 (6.0.6001) 支援遠端桌面通訊協定6.1。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-119">RDC version 6.1 (6.0.6001) supports Remote Desktop Protocol 6.1.</span></span> <span data-ttu-id="a4e0c-120">RDC 6.1 隨附于 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-120">RDC 6.1 is included with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

 

<span data-ttu-id="a4e0c-121">**ConnectToAdministerServer** 會將您連線至遠端伺服器上用於系統管理目的的會話。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-121">**ConnectToAdministerServer** connects you to a session that is used for administrative purposes on the remote server.</span></span> <span data-ttu-id="a4e0c-122">如果遠端桌面工作階段主機 (RD 工作階段主機) 角色服務安裝在遠端伺服器上， **ConnectToAdministerServer** 會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="a4e0c-122">If the Remote Desktop Session Host (RD Session Host) role service is installed on the remote server, **ConnectToAdministerServer** does the following:</span></span>

-   <span data-ttu-id="a4e0c-123">停用會話的遠端桌面服務用戶端存取授權。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-123">Disables Remote Desktop Services client access licensing for the session.</span></span>
-   <span data-ttu-id="a4e0c-124">停用會話的時區重新導向。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-124">Disables time zone redirection for the session.</span></span>
-   <span data-ttu-id="a4e0c-125">停用會話的遠端桌面連線代理人 (RD 連線代理人) 重新導向。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-125">Disables Remote Desktop Connection Broker (RD Connection Broker) redirection for the session.</span></span>
-   <span data-ttu-id="a4e0c-126">停用會話的隨插即用裝置重新導向。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-126">Disables Plug and Play device redirection for the session.</span></span>
-   <span data-ttu-id="a4e0c-127">將會話的遠端會話主題變更為 Windows 傳統。</span><span class="sxs-lookup"><span data-stu-id="a4e0c-127">Changes the remote session theme to Windows Classic for the session.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e0c-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4e0c-128">Requirements</span></span>



| <span data-ttu-id="a4e0c-129">需求</span><span class="sxs-lookup"><span data-stu-id="a4e0c-129">Requirement</span></span> | <span data-ttu-id="a4e0c-130">值</span><span class="sxs-lookup"><span data-stu-id="a4e0c-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e0c-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4e0c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e0c-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4e0c-132">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a4e0c-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4e0c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e0c-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4e0c-134">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a4e0c-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a4e0c-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4e0c-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e0c-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a4e0c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a4e0c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4e0c-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e0c-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a4e0c-139">IID</span><span class="sxs-lookup"><span data-stu-id="a4e0c-139">IID</span></span><br/>                      | <span data-ttu-id="a4e0c-140">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="a4e0c-140">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4e0c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4e0c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e0c-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a4e0c-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a4e0c-143">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a4e0c-143">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a4e0c-144">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a4e0c-144">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





