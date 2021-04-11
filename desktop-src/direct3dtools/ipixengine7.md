---
description: IPixEngine6 介面的延伸模組，其中包含有關版本設定的新增功能。
MS-HAID: vspixengine.IPixEngine7
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine7 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D30020DF-B998-413F-B09B-179A31B0AED2
api_name:
- IPixEngine7
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2e6a228249c782aec6d4587a859deac13ed030d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317791"
---
# <a name="span-idvspixengineipixengine7spanipixengine7-interface"></a><span data-ttu-id="becb5-103"><span id="vspixengine.ipixengine7"></span>IPixEngine7 介面</span><span class="sxs-lookup"><span data-stu-id="becb5-103"><span id="vspixengine.ipixengine7"></span>IPixEngine7 interface</span></span>

<span data-ttu-id="becb5-104">IPixEngine6 介面的延伸模組，其中包含有關版本設定的新增功能。</span><span class="sxs-lookup"><span data-stu-id="becb5-104">Extensions to the IPixEngine6 interface containing additions around versioning.</span></span>

## <a name="members"></a><span data-ttu-id="becb5-105">成員</span><span class="sxs-lookup"><span data-stu-id="becb5-105">Members</span></span>

<span data-ttu-id="becb5-106">**IPixEngine7** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="becb5-106">The **IPixEngine7** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="becb5-107">**IPixEngine7** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="becb5-107">**IPixEngine7** also has these types of members:</span></span>

-   [<span data-ttu-id="becb5-108">方法</span><span class="sxs-lookup"><span data-stu-id="becb5-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="becb5-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="becb5-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="becb5-110">**IPixEngine7** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="becb5-110">The **IPixEngine7** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="becb5-111">方法</span><span class="sxs-lookup"><span data-stu-id="becb5-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="becb5-112">描述</span><span class="sxs-lookup"><span data-stu-id="becb5-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="becb5-113"><a href="/windows/desktop/direct3dtools/ipixengine7-initengineasync-resourcepair-arr-uint-iversioncallback-ptr-dword-dword"><strong>InitEngineAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="becb5-113"><a href="/windows/desktop/direct3dtools/ipixengine7-initengineasync-resourcepair-arr-uint-iversioncallback-ptr-dword-dword"><strong>InitEngineAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="becb5-114">以非同步方式將資源傳遞給引擎，例如錯誤訊息的字串。</span><span class="sxs-lookup"><span data-stu-id="becb5-114">Asynchronously passes resources to the engine, such as strings for error messages.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="becb5-115"><a href="/windows/desktop/direct3dtools/ipixengine7-setplaybackendpointasync-bool-bstr-bstr-remotingversion-iversioncallback-ptr-dword-dword"><strong>SetPlaybackEndpointAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="becb5-115"><a href="/windows/desktop/direct3dtools/ipixengine7-setplaybackendpointasync-bool-bstr-bstr-remotingversion-iversioncallback-ptr-dword-dword"><strong>SetPlaybackEndpointAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="becb5-116">以非同步方式設定用來連接到遠端引擎的端點位址。</span><span class="sxs-lookup"><span data-stu-id="becb5-116">Asynchronously sets the endpoint address used to connect to a remote engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="becb5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="becb5-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="becb5-118">標頭</span><span class="sxs-lookup"><span data-stu-id="becb5-118">Header</span></span></p></td><td><span data-ttu-id="becb5-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="becb5-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
