---
title: IWMDRMDeviceApp2 介面
description: IWMDRMDeviceApp2 介面會藉由提供新版本的 QueryDeviceStatus 方法來擴充 IWMDRMDeviceApp。
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- IWMDRMDeviceApp2 介面 windows Media 裝置管理員
- IWMDRMDeviceApp2 interface windows Media 裝置管理員，說明
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313136"
---
# <a name="iwmdrmdeviceapp2-interface"></a><span data-ttu-id="30b40-105">IWMDRMDeviceApp2 介面</span><span class="sxs-lookup"><span data-stu-id="30b40-105">IWMDRMDeviceApp2 interface</span></span>

<span data-ttu-id="30b40-106">**IWMDRMDeviceApp2** 介面會藉由提供新版本的 [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md)方法來擴充 [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) 。</span><span class="sxs-lookup"><span data-stu-id="30b40-106">The **IWMDRMDeviceApp2** interface extends [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) by providing a new version of the [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) method.</span></span> <span data-ttu-id="30b40-107">**QueryDeviceStatus2** 可讓呼叫端查詢特定的 DRM 需求。</span><span class="sxs-lookup"><span data-stu-id="30b40-107">**QueryDeviceStatus2** enables the caller to query for a specific DRM requirement.</span></span>

<span data-ttu-id="30b40-108">若要取得此介面，請呼叫 **CoCreateInstance** 並傳入 CLSID \_ WMDRMDeviceApp。</span><span class="sxs-lookup"><span data-stu-id="30b40-108">To get this interface, call **CoCreateInstance** and pass in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="30b40-109">此介面定義于從 WMDRMDeviceApp 建立的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="30b40-109">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="30b40-110">此標頭 **\# 包含**"wmdm .h"。</span><span class="sxs-lookup"><span data-stu-id="30b40-110">This header **\#includes** "wmdm.h".</span></span> <span data-ttu-id="30b40-111">您可能需要變更這個檔案名，以符合 WMDM 所建立的標頭。</span><span class="sxs-lookup"><span data-stu-id="30b40-111">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="30b40-112">成員</span><span class="sxs-lookup"><span data-stu-id="30b40-112">Members</span></span>

<span data-ttu-id="30b40-113">**IWMDRMDeviceApp2** 介面繼承自 [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)。</span><span class="sxs-lookup"><span data-stu-id="30b40-113">The **IWMDRMDeviceApp2** interface inherits from [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md).</span></span> <span data-ttu-id="30b40-114">**IWMDRMDeviceApp2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="30b40-114">**IWMDRMDeviceApp2** also has these types of members:</span></span>

-   [<span data-ttu-id="30b40-115">方法</span><span class="sxs-lookup"><span data-stu-id="30b40-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="30b40-116">方法</span><span class="sxs-lookup"><span data-stu-id="30b40-116">Methods</span></span>

<span data-ttu-id="30b40-117">**IWMDRMDeviceApp2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="30b40-117">The **IWMDRMDeviceApp2** interface has these methods.</span></span>



| <span data-ttu-id="30b40-118">方法</span><span class="sxs-lookup"><span data-stu-id="30b40-118">Method</span></span>                                                            | <span data-ttu-id="30b40-119">描述</span><span class="sxs-lookup"><span data-stu-id="30b40-119">Description</span></span>                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="30b40-120">**QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="30b40-120">**QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md) | <span data-ttu-id="30b40-121">查詢裝置的特定 DRM 狀態或功能。</span><span class="sxs-lookup"><span data-stu-id="30b40-121">Queries a device for a specific DRM status or capability.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="30b40-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30b40-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b40-123">**IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="30b40-123">**IWMDRMDeviceApp**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="30b40-124">**處理應用程式中受保護的內容**</span><span class="sxs-lookup"><span data-stu-id="30b40-124">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="30b40-125">**應用程式的介面**</span><span class="sxs-lookup"><span data-stu-id="30b40-125">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="30b40-126">**計量內容使用方式**</span><span class="sxs-lookup"><span data-stu-id="30b40-126">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

 





