---
description: 回呼，以傳回所有支援的介面版本。 這可讓取用者不會與 capture 引擎同步。
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IVersionCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c53008e625d63e2e876bef9ab8cbdd376508c2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106990919"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span data-ttu-id="e8eab-104"><span id="vspixengine.iversioncallback"></span>IVersionCallback 介面</span><span class="sxs-lookup"><span data-stu-id="e8eab-104"><span id="vspixengine.iversioncallback"></span>IVersionCallback interface</span></span>

<span data-ttu-id="e8eab-105">回呼，以傳回所有支援的介面版本。</span><span class="sxs-lookup"><span data-stu-id="e8eab-105">Callback to return the versions of all the interfaces supported.</span></span> <span data-ttu-id="e8eab-106">這可讓取用者不會與 capture 引擎同步。</span><span class="sxs-lookup"><span data-stu-id="e8eab-106">This allows the consumer to be out of sync with the capture engine.</span></span>

## <a name="members"></a><span data-ttu-id="e8eab-107">成員</span><span class="sxs-lookup"><span data-stu-id="e8eab-107">Members</span></span>

<span data-ttu-id="e8eab-108">**IVersionCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e8eab-108">The **IVersionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e8eab-109">**IVersionCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e8eab-109">**IVersionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="e8eab-110">方法</span><span class="sxs-lookup"><span data-stu-id="e8eab-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e8eab-111"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="e8eab-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e8eab-112">**IVersionCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e8eab-112">The **IVersionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e8eab-113">方法</span><span class="sxs-lookup"><span data-stu-id="e8eab-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e8eab-114">描述</span><span class="sxs-lookup"><span data-stu-id="e8eab-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e8eab-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8eab-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e8eab-116">回呼函式，用來通知主機支援的介面。</span><span class="sxs-lookup"><span data-stu-id="e8eab-116">A callback function used to notify the host of which interfaces are supported.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e8eab-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8eab-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e8eab-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e8eab-118">Header</span></span></p></td><td><span data-ttu-id="e8eab-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="e8eab-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
