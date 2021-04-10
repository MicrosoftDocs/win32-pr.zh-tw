---
description: 要求將已平平的材質寫入為 DDS 檔。
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITileRequest 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ceb630661cfe67bc8beb28b2d1de2480726ec594
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688079"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span data-ttu-id="b957e-103"><span id="vspixengine.itilerequest"></span>ITileRequest 介面</span><span class="sxs-lookup"><span data-stu-id="b957e-103"><span id="vspixengine.itilerequest"></span>ITileRequest interface</span></span>

<span data-ttu-id="b957e-104">要求將已平平的材質寫入為 DDS 檔。</span><span class="sxs-lookup"><span data-stu-id="b957e-104">Request for a tiled texture to be written as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="b957e-105">成員</span><span class="sxs-lookup"><span data-stu-id="b957e-105">Members</span></span>

<span data-ttu-id="b957e-106">**ITileRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b957e-106">The **ITileRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b957e-107">**ITileRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b957e-107">**ITileRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="b957e-108">方法</span><span class="sxs-lookup"><span data-stu-id="b957e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="b957e-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="b957e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="b957e-110">**ITileRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b957e-110">The **ITileRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="b957e-111">方法</span><span class="sxs-lookup"><span data-stu-id="b957e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="b957e-112">描述</span><span class="sxs-lookup"><span data-stu-id="b957e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="b957e-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="b957e-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b957e-114">要求取得磚的原始內容。</span><span class="sxs-lookup"><span data-stu-id="b957e-114">Requests to get the raw contents of a tile.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="b957e-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="b957e-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b957e-116">要求將磚材質的內容取得為。DDS (DirectDraw 介面) 檔。</span><span class="sxs-lookup"><span data-stu-id="b957e-116">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="b957e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b957e-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b957e-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b957e-118">Header</span></span></p></td><td><span data-ttu-id="b957e-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="b957e-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
