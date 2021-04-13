---
title: IMsRdpPreferredRedirectionInfo 介面
description: 提供屬性，以使用重新導向伺服器來控制。
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- IMsRdpPreferredRedirectionInfo 介面遠端桌面服務
- IMsRdpPreferredRedirectionInfo 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464576"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a><span data-ttu-id="dd4d5-105">IMsRdpPreferredRedirectionInfo 介面</span><span class="sxs-lookup"><span data-stu-id="dd4d5-105">IMsRdpPreferredRedirectionInfo interface</span></span>

<span data-ttu-id="dd4d5-106">提供屬性，以使用重新導向伺服器來控制。</span><span class="sxs-lookup"><span data-stu-id="dd4d5-106">Provides a property to control using a redirection server.</span></span>

## <a name="members"></a><span data-ttu-id="dd4d5-107">成員</span><span class="sxs-lookup"><span data-stu-id="dd4d5-107">Members</span></span>

<span data-ttu-id="dd4d5-108">**IMsRdpPreferredRedirectionInfo** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="dd4d5-108">The **IMsRdpPreferredRedirectionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dd4d5-109">**IMsRdpPreferredRedirectionInfo** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dd4d5-109">**IMsRdpPreferredRedirectionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="dd4d5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="dd4d5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd4d5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dd4d5-111">Properties</span></span>

<span data-ttu-id="dd4d5-112">**IMsRdpPreferredRedirectionInfo** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dd4d5-112">The **IMsRdpPreferredRedirectionInfo** interface has these properties.</span></span>



| <span data-ttu-id="dd4d5-113">屬性</span><span class="sxs-lookup"><span data-stu-id="dd4d5-113">Property</span></span>                                                                                               | <span data-ttu-id="dd4d5-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="dd4d5-114">Access type</span></span>           | <span data-ttu-id="dd4d5-115">Description</span><span class="sxs-lookup"><span data-stu-id="dd4d5-115">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="dd4d5-116">**UseRedirectionServerName**</span><span class="sxs-lookup"><span data-stu-id="dd4d5-116">**UseRedirectionServerName**</span></span>](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | <span data-ttu-id="dd4d5-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="dd4d5-117">Read/write</span></span><br/> | <span data-ttu-id="dd4d5-118">取得和設定是否使用重新導向伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dd4d5-118">Gets and sets whether to use the redirection server name.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dd4d5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd4d5-119">Requirements</span></span>



| <span data-ttu-id="dd4d5-120">需求</span><span class="sxs-lookup"><span data-stu-id="dd4d5-120">Requirement</span></span> | <span data-ttu-id="dd4d5-121">值</span><span class="sxs-lookup"><span data-stu-id="dd4d5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4d5-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd4d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4d5-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dd4d5-123">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="dd4d5-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd4d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4d5-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd4d5-125">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="dd4d5-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dd4d5-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd4d5-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd4d5-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="dd4d5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dd4d5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd4d5-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd4d5-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="dd4d5-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="dd4d5-130">CLSID</span></span><br/>                    | <span data-ttu-id="dd4d5-131">CLSID \_ MsRdpClient10 定義為 C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span><span class="sxs-lookup"><span data-stu-id="dd4d5-131">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="dd4d5-132">CLSID \_ MsRdpClient10NotSafeForScripting 定義為 A0C63C30-F08D-4AB4-907C-34905D770C7D</span><span class="sxs-lookup"><span data-stu-id="dd4d5-132">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="dd4d5-133">CLSID \_ MsRdpClient7 定義為 A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="dd4d5-133">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="dd4d5-134">CLSID \_ MsRdpClient7NotSafeForScripting 定義為54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="dd4d5-134">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="dd4d5-135">CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="dd4d5-135">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="dd4d5-136">CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="dd4d5-136">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="dd4d5-137">CLSID \_ MsRdpClient9 定義為301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="dd4d5-137">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="dd4d5-138">CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="dd4d5-138">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="dd4d5-139">IID</span><span class="sxs-lookup"><span data-stu-id="dd4d5-139">IID</span></span><br/>                      | <span data-ttu-id="dd4d5-140">IID \_ IMsRdpPreferredRedirectionInfo 定義為 FDD029F9-9574-4DEF-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="dd4d5-140">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

