---
description: 未使用。 先前是管線階段資料的要求。
MS-HAID: vspixengine.IPipeLineStagesRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6EB81F-F60F-49CF-9F34-FABDA05ED3F8
api_name:
- IPipeLineStagesRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4dfa67e0770b1c709ee80bffd01831859ad4c45a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971292"
---
# <a name="span-idvspixengineipipelinestagesrequestspanipipelinestagesrequest-interface"></a><span data-ttu-id="8ab0e-104"><span id="vspixengine.ipipelinestagesrequest"></span>IPipeLineStagesRequest 介面</span><span class="sxs-lookup"><span data-stu-id="8ab0e-104"><span id="vspixengine.ipipelinestagesrequest"></span>IPipeLineStagesRequest interface</span></span>

<span data-ttu-id="8ab0e-105">未使用。</span><span class="sxs-lookup"><span data-stu-id="8ab0e-105">Not used.</span></span> <span data-ttu-id="8ab0e-106">先前是管線階段資料的要求。</span><span class="sxs-lookup"><span data-stu-id="8ab0e-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="8ab0e-107">成員</span><span class="sxs-lookup"><span data-stu-id="8ab0e-107">Members</span></span>

<span data-ttu-id="8ab0e-108">**IPipeLineStagesRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="8ab0e-108">The **IPipeLineStagesRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8ab0e-109">**IPipeLineStagesRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8ab0e-109">**IPipeLineStagesRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="8ab0e-110">方法</span><span class="sxs-lookup"><span data-stu-id="8ab0e-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="8ab0e-111"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="8ab0e-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="8ab0e-112">**IPipeLineStagesRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8ab0e-112">The **IPipeLineStagesRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="8ab0e-113">方法</span><span class="sxs-lookup"><span data-stu-id="8ab0e-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="8ab0e-114">描述</span><span class="sxs-lookup"><span data-stu-id="8ab0e-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="8ab0e-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ab0e-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8ab0e-116">取得 [圖形管線階段] 視窗預覽影像的非同步要求。</span><span class="sxs-lookup"><span data-stu-id="8ab0e-116">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="8ab0e-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ab0e-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8ab0e-118">非同步要求，以取得用於指定之框架和事件的階段清單。</span><span class="sxs-lookup"><span data-stu-id="8ab0e-118">An asynchronous request to get a list of stages used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="8ab0e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ab0e-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8ab0e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="8ab0e-120">Header</span></span></p></td><td><span data-ttu-id="8ab0e-121">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="8ab0e-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
