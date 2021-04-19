---
title: IDRMStatusCallback 介面
description: IDRMStatusCallback 介面會提供一種方法，來接收非同步 DRM 呼叫的狀態。
ms.assetid: d036e259-2451-4020-9516-9631f0ff4095
keywords:
- IDRMStatusCallback 介面 windows 媒體格式
- IDRMStatusCallback 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IDRMStatusCallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 415d04e3934d39ad43787596f4dab16970241b0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966861"
---
# <a name="idrmstatuscallback-interface"></a><span data-ttu-id="5cb5b-105">IDRMStatusCallback 介面</span><span class="sxs-lookup"><span data-stu-id="5cb5b-105">IDRMStatusCallback interface</span></span>

<span data-ttu-id="5cb5b-106">**IDRMStatusCallback** 介面會提供一種方法，來接收非同步 DRM 呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="5cb5b-106">The **IDRMStatusCallback** interface provides a method for receiving status on asynchronous DRM calls.</span></span>

## <a name="members"></a><span data-ttu-id="5cb5b-107">成員</span><span class="sxs-lookup"><span data-stu-id="5cb5b-107">Members</span></span>

<span data-ttu-id="5cb5b-108">**IDRMStatusCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="5cb5b-108">The **IDRMStatusCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5cb5b-109">**IDRMStatusCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5cb5b-109">**IDRMStatusCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="5cb5b-110">方法</span><span class="sxs-lookup"><span data-stu-id="5cb5b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5cb5b-111">方法</span><span class="sxs-lookup"><span data-stu-id="5cb5b-111">Methods</span></span>

<span data-ttu-id="5cb5b-112">**IDRMStatusCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5cb5b-112">The **IDRMStatusCallback** interface has these methods.</span></span>



| <span data-ttu-id="5cb5b-113">方法</span><span class="sxs-lookup"><span data-stu-id="5cb5b-113">Method</span></span>                                          | <span data-ttu-id="5cb5b-114">描述</span><span class="sxs-lookup"><span data-stu-id="5cb5b-114">Description</span></span>                                                      |
|:------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="5cb5b-115">**OnStatus**</span><span class="sxs-lookup"><span data-stu-id="5cb5b-115">**OnStatus**</span></span>](idrmstatuscallback-onstatus.md) | <span data-ttu-id="5cb5b-116">接收來自非同步進程的狀態訊息。</span><span class="sxs-lookup"><span data-stu-id="5cb5b-116">Receives status messages from asynchronous processes.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5cb5b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cb5b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb5b-118">**介面**</span><span class="sxs-lookup"><span data-stu-id="5cb5b-118">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

