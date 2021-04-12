---
title: IMsRdpClientAdvancedSettings8 介面
description: 公開管理遠端桌面 ActiveX 控制項之 advanced 設定的方法和屬性。
ms.assetid: 9e1de47d-f194-4d9e-8e47-7c13a0677aaa
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fce32baf792563e64d2f8b8e1ad2bd56a31c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384182"
---
# <a name="imsrdpclientadvancedsettings8-interface"></a><span data-ttu-id="1e635-105">IMsRdpClientAdvancedSettings8 介面</span><span class="sxs-lookup"><span data-stu-id="1e635-105">IMsRdpClientAdvancedSettings8 interface</span></span>

<span data-ttu-id="1e635-106">公開管理遠端桌面 ActiveX 控制項之 advanced 設定的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="1e635-106">Exposes methods and properties that manage advanced settings of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="1e635-107">若要取得這個介面的實例，請使用 [**IMsRdpClient8：： AdvancedSettings9**](imsrdpclient8-advancedsettings9.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1e635-107">To obtain an instance of this interface, use the [**IMsRdpClient8::AdvancedSettings9**](imsrdpclient8-advancedsettings9.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="1e635-108">成員</span><span class="sxs-lookup"><span data-stu-id="1e635-108">Members</span></span>

<span data-ttu-id="1e635-109">**IMsRdpClientAdvancedSettings8** 介面繼承自 [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)。</span><span class="sxs-lookup"><span data-stu-id="1e635-109">The **IMsRdpClientAdvancedSettings8** interface inherits from [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md).</span></span> <span data-ttu-id="1e635-110">**IMsRdpClientAdvancedSettings8** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1e635-110">**IMsRdpClientAdvancedSettings8** also has these types of members:</span></span>

-   [<span data-ttu-id="1e635-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1e635-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e635-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1e635-112">Properties</span></span>

<span data-ttu-id="1e635-113">**IMsRdpClientAdvancedSettings8** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1e635-113">The **IMsRdpClientAdvancedSettings8** interface has these properties.</span></span>



| <span data-ttu-id="1e635-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1e635-114">Property</span></span>                                                                                  | <span data-ttu-id="1e635-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="1e635-115">Access type</span></span>           | <span data-ttu-id="1e635-116">Description</span><span class="sxs-lookup"><span data-stu-id="1e635-116">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="1e635-117">**BandwidthDetection**</span><span class="sxs-lookup"><span data-stu-id="1e635-117">**BandwidthDetection**</span></span>](imsrdpclientadvancedsettings8-bandwidthdetection.md)<br/> | <span data-ttu-id="1e635-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1e635-118">Read/write</span></span><br/> | <span data-ttu-id="1e635-119">指定是否自動偵測頻寬變更。</span><span class="sxs-lookup"><span data-stu-id="1e635-119">Specifies if bandwidth changes are automatically detected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1e635-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e635-120">Requirements</span></span>



| <span data-ttu-id="1e635-121">需求</span><span class="sxs-lookup"><span data-stu-id="1e635-121">Requirement</span></span> | <span data-ttu-id="1e635-122">值</span><span class="sxs-lookup"><span data-stu-id="1e635-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e635-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e635-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1e635-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1e635-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="1e635-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e635-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1e635-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e635-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="1e635-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1e635-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e635-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e635-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e635-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1e635-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e635-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e635-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



 

 





