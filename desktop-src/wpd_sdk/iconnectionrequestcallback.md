---
description: 定義單一回呼方法。
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: 'IConnectionRequestCallback 介面 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945344"
---
# <a name="iconnectionrequestcallback-interface"></a><span data-ttu-id="d3ee1-103">IConnectionRequestCallback 介面</span><span class="sxs-lookup"><span data-stu-id="d3ee1-103">IConnectionRequestCallback interface</span></span>

<span data-ttu-id="d3ee1-104">**IConnectionRequestCallback** 介面會定義單一回呼方法。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-104">The **IConnectionRequestCallback** interface defines a single callback method.</span></span> <span data-ttu-id="d3ee1-105">Windows 可攜式裝置 (WPD) 應用程式會將這個選擇性元件物件模型 (COM) 介面，以接收已完成要求的通知，以及解除擱置的要求。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-105">A Windows Portable Devices (WPD) application implements this optional Component Object Model (COM) interface to receive notifications about completed requests and to cancel pending requests.</span></span> <span data-ttu-id="d3ee1-106">要求會使用 [**IPortableDeviceConnector：： Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) 和 [**IPortableDeviceConnector：:D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) 方法來傳送。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-106">The requests are sent using the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="members"></a><span data-ttu-id="d3ee1-107">成員</span><span class="sxs-lookup"><span data-stu-id="d3ee1-107">Members</span></span>

<span data-ttu-id="d3ee1-108">**IConnectionRequestCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-108">The **IConnectionRequestCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d3ee1-109">**IConnectionRequestCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d3ee1-109">**IConnectionRequestCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="d3ee1-110">方法</span><span class="sxs-lookup"><span data-stu-id="d3ee1-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d3ee1-111">方法</span><span class="sxs-lookup"><span data-stu-id="d3ee1-111">Methods</span></span>

<span data-ttu-id="d3ee1-112">**IConnectionRequestCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-112">The **IConnectionRequestCallback** interface has these methods.</span></span>



| <span data-ttu-id="d3ee1-113">方法</span><span class="sxs-lookup"><span data-stu-id="d3ee1-113">Method</span></span>                                                      | <span data-ttu-id="d3ee1-114">描述</span><span class="sxs-lookup"><span data-stu-id="d3ee1-114">Description</span></span>                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3ee1-115">**OnComplete**</span><span class="sxs-lookup"><span data-stu-id="d3ee1-115">**OnComplete**</span></span>](iconnectionrequestcallback-oncomplete.md) | <span data-ttu-id="d3ee1-116">通知應用程式先前已排程的要求已完成。</span><span class="sxs-lookup"><span data-stu-id="d3ee1-116">Notifies an application that a previously scheduled request has completed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d3ee1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3ee1-117">Requirements</span></span>



| <span data-ttu-id="d3ee1-118">需求</span><span class="sxs-lookup"><span data-stu-id="d3ee1-118">Requirement</span></span> | <span data-ttu-id="d3ee1-119">值</span><span class="sxs-lookup"><span data-stu-id="d3ee1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ee1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3ee1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ee1-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3ee1-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="d3ee1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3ee1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ee1-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="d3ee1-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="d3ee1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d3ee1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ee1-125"><dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ee1-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="d3ee1-126">Idl</span><span class="sxs-lookup"><span data-stu-id="d3ee1-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3ee1-127"><dt>Portabledeviceconnectapi .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3ee1-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="d3ee1-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3ee1-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3ee1-129"><dt>PortableDeviceGuids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3ee1-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

