---
description: 回呼，以傳回建立著色器追蹤所產生的指示。
MS-HAID: vspixengine.IDebugShaderCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A4A3FD3-15E5-4DB5-8777-55797E32ABA3
api_name:
- IDebugShaderCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 676d76a0dbc199880badebc904a4eb66d2ad4d0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967011"
---
# <a name="span-idvspixengineidebugshadercallbackspanidebugshadercallback-interface"></a><span data-ttu-id="a9b1f-103"><span id="vspixengine.idebugshadercallback"></span>IDebugShaderCallback 介面</span><span class="sxs-lookup"><span data-stu-id="a9b1f-103"><span id="vspixengine.idebugshadercallback"></span>IDebugShaderCallback interface</span></span>

<span data-ttu-id="a9b1f-104">回呼，以傳回建立著色器追蹤所產生的指示。</span><span class="sxs-lookup"><span data-stu-id="a9b1f-104">Callback to return the instructions generated from creating a shader trace.</span></span>

## <a name="members"></a><span data-ttu-id="a9b1f-105">成員</span><span class="sxs-lookup"><span data-stu-id="a9b1f-105">Members</span></span>

<span data-ttu-id="a9b1f-106">**IDebugShaderCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="a9b1f-106">The **IDebugShaderCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a9b1f-107">**IDebugShaderCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a9b1f-107">**IDebugShaderCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="a9b1f-108">方法</span><span class="sxs-lookup"><span data-stu-id="a9b1f-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="a9b1f-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="a9b1f-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="a9b1f-110">**IDebugShaderCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a9b1f-110">The **IDebugShaderCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="a9b1f-111">方法</span><span class="sxs-lookup"><span data-stu-id="a9b1f-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="a9b1f-112">描述</span><span class="sxs-lookup"><span data-stu-id="a9b1f-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a9b1f-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="a9b1f-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a9b1f-114">回呼，會通知主機相關要求所傳回的 instructrion 資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b1f-114">A callback that notifies the host of instructrion information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="a9b1f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9b1f-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a9b1f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a9b1f-116">Header</span></span></p></td><td><span data-ttu-id="a9b1f-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="a9b1f-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
