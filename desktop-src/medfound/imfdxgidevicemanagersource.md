---
description: 提供從 Microsoft 媒體基礎 video 轉譯接收器取得 IMFDXGIDeviceManager 的功能。
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: IMFDXGIDeviceManagerSource 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691272"
---
# <a name="imfdxgidevicemanagersource-interface"></a><span data-ttu-id="8124f-103">IMFDXGIDeviceManagerSource 介面</span><span class="sxs-lookup"><span data-stu-id="8124f-103">IMFDXGIDeviceManagerSource interface</span></span>

<span data-ttu-id="8124f-104">提供從 Microsoft 媒體基礎 video 轉譯接收器取得 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 的功能。</span><span class="sxs-lookup"><span data-stu-id="8124f-104">Provides functionality for getting the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="members"></a><span data-ttu-id="8124f-105">成員</span><span class="sxs-lookup"><span data-stu-id="8124f-105">Members</span></span>

<span data-ttu-id="8124f-106">**IMFDXGIDeviceManagerSource** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="8124f-106">The **IMFDXGIDeviceManagerSource** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8124f-107">**IMFDXGIDeviceManagerSource** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8124f-107">**IMFDXGIDeviceManagerSource** also has these types of members:</span></span>

-   [<span data-ttu-id="8124f-108">方法</span><span class="sxs-lookup"><span data-stu-id="8124f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8124f-109">方法</span><span class="sxs-lookup"><span data-stu-id="8124f-109">Methods</span></span>

<span data-ttu-id="8124f-110">**IMFDXGIDeviceManagerSource** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8124f-110">The **IMFDXGIDeviceManagerSource** interface has these methods.</span></span>



| <span data-ttu-id="8124f-111">方法</span><span class="sxs-lookup"><span data-stu-id="8124f-111">Method</span></span>                                                      | <span data-ttu-id="8124f-112">描述</span><span class="sxs-lookup"><span data-stu-id="8124f-112">Description</span></span>                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8124f-113">**GetManager**</span><span class="sxs-lookup"><span data-stu-id="8124f-113">**GetManager**</span></span>](imfdxgidevicemanagersource-getmanager.md) | <span data-ttu-id="8124f-114">從媒體基礎影片轉譯接收器取得 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 。</span><span class="sxs-lookup"><span data-stu-id="8124f-114">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Media Foundation video rendering sink.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8124f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8124f-115">Requirements</span></span>



| <span data-ttu-id="8124f-116">需求</span><span class="sxs-lookup"><span data-stu-id="8124f-116">Requirement</span></span> | <span data-ttu-id="8124f-117">值</span><span class="sxs-lookup"><span data-stu-id="8124f-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8124f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8124f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8124f-119">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8124f-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="8124f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8124f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8124f-121">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8124f-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="8124f-122">Idl</span><span class="sxs-lookup"><span data-stu-id="8124f-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8124f-123"><dt>Mfidl .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8124f-123"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8124f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8124f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8124f-125">媒體基礎介面</span><span class="sxs-lookup"><span data-stu-id="8124f-125">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
