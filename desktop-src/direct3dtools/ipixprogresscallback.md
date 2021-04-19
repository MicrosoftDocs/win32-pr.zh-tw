---
description: 從引擎回呼以傳回進度。
MS-HAID: vspixengine.IPixProgressCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixProgressCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B2DAF90B-5615-464F-84F9-A80912E09FB9
api_name:
- IPixProgressCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: afb3e962569b1871282577f3d46618374b59425f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106985383"
---
# <a name="span-idvspixengineipixprogresscallbackspanipixprogresscallback-interface"></a><span data-ttu-id="232d3-103"><span id="vspixengine.ipixprogresscallback"></span>IPixProgressCallback 介面</span><span class="sxs-lookup"><span data-stu-id="232d3-103"><span id="vspixengine.ipixprogresscallback"></span>IPixProgressCallback interface</span></span>

<span data-ttu-id="232d3-104">從引擎回呼以傳回進度。</span><span class="sxs-lookup"><span data-stu-id="232d3-104">Callback from engine to return progress.</span></span>

## <a name="members"></a><span data-ttu-id="232d3-105">成員</span><span class="sxs-lookup"><span data-stu-id="232d3-105">Members</span></span>

<span data-ttu-id="232d3-106">**IPixProgressCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="232d3-106">The **IPixProgressCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="232d3-107">**IPixProgressCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="232d3-107">**IPixProgressCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="232d3-108">方法</span><span class="sxs-lookup"><span data-stu-id="232d3-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="232d3-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="232d3-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="232d3-110">**IPixProgressCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="232d3-110">The **IPixProgressCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="232d3-111">方法</span><span class="sxs-lookup"><span data-stu-id="232d3-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="232d3-112">描述</span><span class="sxs-lookup"><span data-stu-id="232d3-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="232d3-113"><a href="/windows/desktop/direct3dtools/ipixprogresscallback-progress-dword-dword"><strong>進度</strong></a></span><span class="sxs-lookup"><span data-stu-id="232d3-113"><a href="/windows/desktop/direct3dtools/ipixprogresscallback-progress-dword-dword"><strong>Progress</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="232d3-114">回呼，會通知主機相關要求的進度。</span><span class="sxs-lookup"><span data-stu-id="232d3-114">A callback that notifies the host of the progress of an associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="232d3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="232d3-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="232d3-116">標頭</span><span class="sxs-lookup"><span data-stu-id="232d3-116">Header</span></span></p></td><td><span data-ttu-id="232d3-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="232d3-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
