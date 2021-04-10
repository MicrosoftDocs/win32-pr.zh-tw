---
description: IWiaUIExtension2 介面提供的方法會將預設的系統提供的使用者介面取代為自訂的使用者介面，並提供自訂裝置圖示。
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: 'IWiaUIExtension2 介面 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943465"
---
# <a name="iwiauiextension2-interface"></a><span data-ttu-id="e0de7-103">IWiaUIExtension2 介面</span><span class="sxs-lookup"><span data-stu-id="e0de7-103">IWiaUIExtension2 interface</span></span>

<span data-ttu-id="e0de7-104">IWiaUIExtension2 介面提供的方法會將預設的系統提供的使用者介面取代為自訂的使用者介面，並提供自訂裝置圖示。</span><span class="sxs-lookup"><span data-stu-id="e0de7-104">The IWiaUIExtension2 interface provides methods that replace the default, system-supplied user interface with a custom user interface, and that provide a custom device icon.</span></span> <span data-ttu-id="e0de7-105">裝置廠商可以執行此介面，為其裝置提供自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="e0de7-105">Device vendors can implement this interface to provide custom user interfaces for their devices.</span></span>

## <a name="members"></a><span data-ttu-id="e0de7-106">成員</span><span class="sxs-lookup"><span data-stu-id="e0de7-106">Members</span></span>

<span data-ttu-id="e0de7-107">**IWiaUIExtension2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e0de7-107">The **IWiaUIExtension2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e0de7-108">**IWiaUIExtension2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e0de7-108">**IWiaUIExtension2** also has these types of members:</span></span>

-   [<span data-ttu-id="e0de7-109">方法</span><span class="sxs-lookup"><span data-stu-id="e0de7-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e0de7-110">方法</span><span class="sxs-lookup"><span data-stu-id="e0de7-110">Methods</span></span>

<span data-ttu-id="e0de7-111">**IWiaUIExtension2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e0de7-111">The **IWiaUIExtension2** interface has these methods.</span></span>



| <span data-ttu-id="e0de7-112">方法</span><span class="sxs-lookup"><span data-stu-id="e0de7-112">Method</span></span>                                                       | <span data-ttu-id="e0de7-113">描述</span><span class="sxs-lookup"><span data-stu-id="e0de7-113">Description</span></span>                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0de7-114">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="e0de7-114">**DeviceDialog**</span></span>](-wia-iwiauiextension2-devicedialog.md)   | <span data-ttu-id="e0de7-115">提供可取代預設系統使用者介面的自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="e0de7-115">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="e0de7-116">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="e0de7-116">**GetDeviceIcon**</span></span>](-wia-iwiauiextension2-getdeviceicon.md) | <span data-ttu-id="e0de7-117">取得自訂裝置圖示。</span><span class="sxs-lookup"><span data-stu-id="e0de7-117">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="e0de7-118">備註</span><span class="sxs-lookup"><span data-stu-id="e0de7-118">Remarks</span></span>



| <span data-ttu-id="e0de7-119">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="e0de7-119">IUnknown Methods</span></span>                                        | <span data-ttu-id="e0de7-120">Description</span><span class="sxs-lookup"><span data-stu-id="e0de7-120">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="e0de7-121">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="e0de7-121">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="e0de7-122">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e0de7-122">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="e0de7-123">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="e0de7-123">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="e0de7-124">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="e0de7-124">Increments reference count.</span></span>               |
| [<span data-ttu-id="e0de7-125">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="e0de7-125">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="e0de7-126">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="e0de7-126">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="e0de7-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0de7-127">Requirements</span></span>



| <span data-ttu-id="e0de7-128">需求</span><span class="sxs-lookup"><span data-stu-id="e0de7-128">Requirement</span></span> | <span data-ttu-id="e0de7-129">值</span><span class="sxs-lookup"><span data-stu-id="e0de7-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0de7-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0de7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e0de7-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0de7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e0de7-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0de7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e0de7-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0de7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0de7-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e0de7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0de7-135"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0de7-135"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
