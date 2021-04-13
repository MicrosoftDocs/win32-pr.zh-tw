---
description: IPixEngine4 介面的延伸模組，包含用於查看材質的新增專案。
MS-HAID: vspixengine.IPixEngine5
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8995B617-6830-4A07-8C83-B5925E033967
api_name:
- IPixEngine5
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 300ed31eae5d8ff4009f28691c5348db7cd89d6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510007"
---
# <a name="span-idvspixengineipixengine5spanipixengine5-interface"></a><span data-ttu-id="366d0-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5 介面</span><span class="sxs-lookup"><span data-stu-id="366d0-103"><span id="vspixengine.ipixengine5"></span>IPixEngine5 interface</span></span>

<span data-ttu-id="366d0-104">IPixEngine4 介面的延伸模組，包含用於查看材質的新增專案。</span><span class="sxs-lookup"><span data-stu-id="366d0-104">Extensions to the IPixEngine4 interface containing additions for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="366d0-105">成員</span><span class="sxs-lookup"><span data-stu-id="366d0-105">Members</span></span>

<span data-ttu-id="366d0-106">**IPixEngine5** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="366d0-106">The **IPixEngine5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="366d0-107">**IPixEngine5** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="366d0-107">**IPixEngine5** also has these types of members:</span></span>

-   [<span data-ttu-id="366d0-108">方法</span><span class="sxs-lookup"><span data-stu-id="366d0-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="366d0-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="366d0-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="366d0-110">**IPixEngine5** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="366d0-110">The **IPixEngine5** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="366d0-111">方法</span><span class="sxs-lookup"><span data-stu-id="366d0-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="366d0-112">描述</span><span class="sxs-lookup"><span data-stu-id="366d0-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="366d0-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="366d0-113"><a href="/windows/desktop/direct3dtools/ipixengine5-freetextureasync-uint-ipixengine5callbacks-ptr-dword-dword"><strong>FreeTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="366d0-114">釋出材質，並以非同步方式通知主機。</span><span class="sxs-lookup"><span data-stu-id="366d0-114">Frees a texture and notifies the host asynchronously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="366d0-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="366d0-115"><a href="/windows/desktop/direct3dtools/ipixengine5-loadhistogramasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadHistogramAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="366d0-116">載入長條圖資料的非同步要求。</span><span class="sxs-lookup"><span data-stu-id="366d0-116">An asynchronous request to load histogram data.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="366d0-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="366d0-117"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturefromfileasync-bstr-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureFromFileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="366d0-118">從檔案載入材質，並在完成時以非同步方式通知主機。</span><span class="sxs-lookup"><span data-stu-id="366d0-118">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="366d0-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="366d0-119"><a href="/windows/desktop/direct3dtools/ipixengine5-loadtexturesliceasync-uint-pixenginetexturesliceindex-int-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>LoadTextureSliceAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="366d0-120">載入紋理配量，並在完成時通知主機 asynchrnously。</span><span class="sxs-lookup"><span data-stu-id="366d0-120">Loads a texture slice and notifies the host asynchrnously when it completes.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="366d0-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="366d0-121"><a href="/windows/desktop/direct3dtools/ipixengine5-readtexelvalueasync-uint-pixenginetexturesliceindex-int-int-int-ipixengine5callbacks-ptr-dword-dword"><strong>ReadTexelValueAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="366d0-122">讀取材質值，並將結果傳回至主機 asynchrnously。</span><span class="sxs-lookup"><span data-stu-id="366d0-122">Reads a texel value and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="366d0-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="366d0-123"><a href="/previous-versions/windows/desktop/legacy/mt432769(v=vs.85)"><strong>RenderTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="366d0-124">將材質轉譯至檔案，並將結果傳回至主機 asynchrnously。</span><span class="sxs-lookup"><span data-stu-id="366d0-124">Renders a texture to a file and returns the result to the host asynchrnously.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="366d0-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="366d0-125"><a href="/windows/desktop/direct3dtools/ipixengine5-savetextureasync-uint-bstr-ipixengine5callbacks-ptr-dword-dword"><strong>SaveTextureAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="366d0-126">儲存材質。</span><span class="sxs-lookup"><span data-stu-id="366d0-126">Saves a texture.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="366d0-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="366d0-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="366d0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="366d0-128">Header</span></span></p></td><td><span data-ttu-id="366d0-129">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="366d0-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
