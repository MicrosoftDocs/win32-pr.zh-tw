---
description: 支援 IPortableDeviceConnector 介面的列舉，代表與電腦配對的 MTP/藍牙裝置。
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: 'IEnumPortableDeviceConnectors 介面 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192815"
---
# <a name="ienumportabledeviceconnectors-interface"></a><span data-ttu-id="32bcf-103">IEnumPortableDeviceConnectors 介面</span><span class="sxs-lookup"><span data-stu-id="32bcf-103">IEnumPortableDeviceConnectors interface</span></span>

<span data-ttu-id="32bcf-104">**IEnumPortableDeviceConnectors** 介面支援 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)介面的列舉，代表與電腦配對的 MTP/藍牙裝置。</span><span class="sxs-lookup"><span data-stu-id="32bcf-104">The **IEnumPortableDeviceConnectors** interface supports the enumeration of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces, representing MTP/Bluetooth devices that were paired with the PC.</span></span> <span data-ttu-id="32bcf-105">請注意，這將會取出所有先前配對的裝置，包括已配對但已中斷連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="32bcf-105">Note that this will retrieve all previously-paired devices, including devices that are paired but disconnected.</span></span> <span data-ttu-id="32bcf-106">若要判斷裝置是否仍在連線，請查詢該裝置的 **DEVPKEY \_ MTPBTH \_ IsConnected** 屬性。</span><span class="sxs-lookup"><span data-stu-id="32bcf-106">To determine if a device is still connected, query the **DEVPKEY\_MTPBTH\_IsConnected** property for that device.</span></span>

## <a name="members"></a><span data-ttu-id="32bcf-107">成員</span><span class="sxs-lookup"><span data-stu-id="32bcf-107">Members</span></span>

<span data-ttu-id="32bcf-108">**IEnumPortableDeviceConnectors** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="32bcf-108">The **IEnumPortableDeviceConnectors** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="32bcf-109">**IEnumPortableDeviceConnectors** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="32bcf-109">**IEnumPortableDeviceConnectors** also has these types of members:</span></span>

-   [<span data-ttu-id="32bcf-110">方法</span><span class="sxs-lookup"><span data-stu-id="32bcf-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="32bcf-111">方法</span><span class="sxs-lookup"><span data-stu-id="32bcf-111">Methods</span></span>

<span data-ttu-id="32bcf-112">**IEnumPortableDeviceConnectors** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="32bcf-112">The **IEnumPortableDeviceConnectors** interface has these methods.</span></span>



| <span data-ttu-id="32bcf-113">方法</span><span class="sxs-lookup"><span data-stu-id="32bcf-113">Method</span></span>                                               | <span data-ttu-id="32bcf-114">描述</span><span class="sxs-lookup"><span data-stu-id="32bcf-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32bcf-115">**克隆**</span><span class="sxs-lookup"><span data-stu-id="32bcf-115">**Clone**</span></span>](ienumportabledeviceconnectors-clone.md) | <span data-ttu-id="32bcf-116">建立目前 **IEnumPortableDeviceConnectors** 介面的複本。</span><span class="sxs-lookup"><span data-stu-id="32bcf-116">Creates a copy of the current **IEnumPortableDeviceConnectors** interface.</span></span><br/>                                                       |
| [<span data-ttu-id="32bcf-117">**下一步**</span><span class="sxs-lookup"><span data-stu-id="32bcf-117">**Next**</span></span>](ienumportabledeviceconnectors-next.md)   | <span data-ttu-id="32bcf-118">抓取列舉順序中的下一個或多個 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) 物件。</span><span class="sxs-lookup"><span data-stu-id="32bcf-118">Retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="32bcf-119">**重設**</span><span class="sxs-lookup"><span data-stu-id="32bcf-119">**Reset**</span></span>](ienumportabledeviceconnectors-reset.md) | <span data-ttu-id="32bcf-120">將列舉序列重設為開頭。</span><span class="sxs-lookup"><span data-stu-id="32bcf-120">Resets the enumeration sequence to the beginning.</span></span><br/>                                                                                |
| [<span data-ttu-id="32bcf-121">**跳過**</span><span class="sxs-lookup"><span data-stu-id="32bcf-121">**Skip**</span></span>](ienumportabledeviceconnectors-skip.md)   | <span data-ttu-id="32bcf-122">略過列舉序列中指定的裝置數目。</span><span class="sxs-lookup"><span data-stu-id="32bcf-122">Skips the specified number of devices in the enumeration sequence.</span></span><br/>                                                               |



 

## <a name="requirements"></a><span data-ttu-id="32bcf-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="32bcf-123">Requirements</span></span>



| <span data-ttu-id="32bcf-124">需求</span><span class="sxs-lookup"><span data-stu-id="32bcf-124">Requirement</span></span> | <span data-ttu-id="32bcf-125">值</span><span class="sxs-lookup"><span data-stu-id="32bcf-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32bcf-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32bcf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="32bcf-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32bcf-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="32bcf-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32bcf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="32bcf-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="32bcf-129">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="32bcf-130">標頭</span><span class="sxs-lookup"><span data-stu-id="32bcf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="32bcf-131"><dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt></span><span class="sxs-lookup"><span data-stu-id="32bcf-131"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="32bcf-132">Idl</span><span class="sxs-lookup"><span data-stu-id="32bcf-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32bcf-133"><dt>Portabledeviceconnectapi .idl</dt></span><span class="sxs-lookup"><span data-stu-id="32bcf-133"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="32bcf-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="32bcf-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="32bcf-135"><dt>PortableDeviceGuids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="32bcf-135"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

