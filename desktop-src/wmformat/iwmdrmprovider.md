---
title: IWMDRMProvider 介面
description: IWMDRMProvider 介面所提供的方法會建立 Microsoft Windows Media DRM 用戶端擴充 Api 的其他物件。您可以藉由呼叫 WMDRMCreateProvider 函式，取得這個介面實例的指標。
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- IWMDRMProvider 介面 windows 媒體格式
- IWMDRMProvider 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682836"
---
# <a name="iwmdrmprovider-interface"></a><span data-ttu-id="332fc-105">IWMDRMProvider 介面</span><span class="sxs-lookup"><span data-stu-id="332fc-105">IWMDRMProvider interface</span></span>

<span data-ttu-id="332fc-106">**IWMDRMProvider** 介面提供的方法會建立 Microsoft WINDOWS Media DRM 用戶端擴充 api 的其他物件。</span><span class="sxs-lookup"><span data-stu-id="332fc-106">The **IWMDRMProvider** interface provides a method that creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="332fc-107">您可以藉由呼叫 [**WMDRMCreateProvider**](wmdrmcreateprovider.md) 函式來取得這個介面實例的指標。</span><span class="sxs-lookup"><span data-stu-id="332fc-107">You can obtain a pointer to an instance of this interface by calling the [**WMDRMCreateProvider**](wmdrmcreateprovider.md) function.</span></span> <span data-ttu-id="332fc-108">若要取得可建立安全物件之這個介面實例的指標，您必須呼叫 [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="332fc-108">To obtain a pointer to an instance of this interface that can create secure objects, you must call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="332fc-109">成員</span><span class="sxs-lookup"><span data-stu-id="332fc-109">Members</span></span>

<span data-ttu-id="332fc-110">**IWMDRMProvider** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="332fc-110">The **IWMDRMProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="332fc-111">**IWMDRMProvider** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="332fc-111">**IWMDRMProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="332fc-112">方法</span><span class="sxs-lookup"><span data-stu-id="332fc-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="332fc-113">方法</span><span class="sxs-lookup"><span data-stu-id="332fc-113">Methods</span></span>

<span data-ttu-id="332fc-114">**IWMDRMProvider** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="332fc-114">The **IWMDRMProvider** interface has these methods.</span></span>



| <span data-ttu-id="332fc-115">方法</span><span class="sxs-lookup"><span data-stu-id="332fc-115">Method</span></span>                                              | <span data-ttu-id="332fc-116">描述</span><span class="sxs-lookup"><span data-stu-id="332fc-116">Description</span></span>                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="332fc-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="332fc-117">**CreateObject**</span></span>](iwmdrmprovider-createobject.md) | <span data-ttu-id="332fc-118">抓取指定介面的指標，視需要建立執行物件。</span><span class="sxs-lookup"><span data-stu-id="332fc-118">Retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="332fc-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="332fc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332fc-120">**介面**</span><span class="sxs-lookup"><span data-stu-id="332fc-120">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

