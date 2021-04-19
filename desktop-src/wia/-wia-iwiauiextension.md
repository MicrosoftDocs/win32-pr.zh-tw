---
description: IWiaUIExtension 介面提供的方法可取代預設系統使用者介面、提供自訂裝置點陣圖標誌，以及提供自訂裝置圖示。
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: 'IWiaUIExtension 介面 (Wiadevd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997493"
---
# <a name="iwiauiextension-interface"></a><span data-ttu-id="cb9f3-103">IWiaUIExtension 介面</span><span class="sxs-lookup"><span data-stu-id="cb9f3-103">IWiaUIExtension interface</span></span>

<span data-ttu-id="cb9f3-104">**IWiaUIExtension** 介面提供的方法可取代預設系統使用者介面、提供自訂裝置點陣圖標誌，以及提供自訂裝置圖示。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-104">The **IWiaUIExtension** interface provides methods that replace the default system user interface, provide a custom device bitmap logo, and provide a custom device icon.</span></span>

## <a name="members"></a><span data-ttu-id="cb9f3-105">成員</span><span class="sxs-lookup"><span data-stu-id="cb9f3-105">Members</span></span>

<span data-ttu-id="cb9f3-106">**IWiaUIExtension** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-106">The **IWiaUIExtension** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cb9f3-107">**IWiaUIExtension** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cb9f3-107">**IWiaUIExtension** also has these types of members:</span></span>

-   [<span data-ttu-id="cb9f3-108">方法</span><span class="sxs-lookup"><span data-stu-id="cb9f3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cb9f3-109">方法</span><span class="sxs-lookup"><span data-stu-id="cb9f3-109">Methods</span></span>

<span data-ttu-id="cb9f3-110">**IWiaUIExtension** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-110">The **IWiaUIExtension** interface has these methods.</span></span>



| <span data-ttu-id="cb9f3-111">方法</span><span class="sxs-lookup"><span data-stu-id="cb9f3-111">Method</span></span>                                                                  | <span data-ttu-id="cb9f3-112">描述</span><span class="sxs-lookup"><span data-stu-id="cb9f3-112">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb9f3-113">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="cb9f3-113">**DeviceDialog**</span></span>](-wia-iwiauiextension-devicedialog.md)               | <span data-ttu-id="cb9f3-114">提供可取代預設系統使用者介面的自訂使用者介面。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-114">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="cb9f3-115">**GetDeviceBitmapLogo**</span><span class="sxs-lookup"><span data-stu-id="cb9f3-115">**GetDeviceBitmapLogo**</span></span>](-wia-iwiauiextension-getdevicebitmaplogo.md) | <span data-ttu-id="cb9f3-116">取得裝置的自訂點陣圖標誌。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-116">Gets a custom bitmap logo for the device.</span></span><br/>                                         |
| [<span data-ttu-id="cb9f3-117">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="cb9f3-117">**GetDeviceIcon**</span></span>](-wia-iwiauiextension-getdeviceicon.md)             | <span data-ttu-id="cb9f3-118">取得自訂裝置圖示。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-118">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="cb9f3-119">備註</span><span class="sxs-lookup"><span data-stu-id="cb9f3-119">Remarks</span></span>



| <span data-ttu-id="cb9f3-120">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="cb9f3-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="cb9f3-121">Description</span><span class="sxs-lookup"><span data-stu-id="cb9f3-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="cb9f3-122">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="cb9f3-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="cb9f3-123">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="cb9f3-124">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="cb9f3-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="cb9f3-125">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="cb9f3-126">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="cb9f3-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="cb9f3-127">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="cb9f3-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="cb9f3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb9f3-128">Requirements</span></span>



| <span data-ttu-id="cb9f3-129">需求</span><span class="sxs-lookup"><span data-stu-id="cb9f3-129">Requirement</span></span> | <span data-ttu-id="cb9f3-130">值</span><span class="sxs-lookup"><span data-stu-id="cb9f3-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9f3-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb9f3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cb9f3-132">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb9f3-132">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cb9f3-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb9f3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cb9f3-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb9f3-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cb9f3-135">標頭</span><span class="sxs-lookup"><span data-stu-id="cb9f3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb9f3-136"><dt>Wiadevd。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb9f3-136"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
