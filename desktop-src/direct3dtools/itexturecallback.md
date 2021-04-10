---
description: 回呼，以將材質寫入為 DDS 檔。
MS-HAID: vspixengine.ITextureCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITextureCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2558C90A-7235-4A36-859C-0E74BD0B712A
api_name:
- ITextureCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 831de15656960cdc72ef2db50c1f3d13b8491e38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688363"
---
# <a name="span-idvspixengineitexturecallbackspanitexturecallback-interface"></a><span data-ttu-id="9f0a1-103"><span id="vspixengine.itexturecallback"></span>ITextureCallback 介面</span><span class="sxs-lookup"><span data-stu-id="9f0a1-103"><span id="vspixengine.itexturecallback"></span>ITextureCallback interface</span></span>

<span data-ttu-id="9f0a1-104">回呼，以將材質寫入為 DDS 檔。</span><span class="sxs-lookup"><span data-stu-id="9f0a1-104">Callback to write a texture as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="9f0a1-105">成員</span><span class="sxs-lookup"><span data-stu-id="9f0a1-105">Members</span></span>

<span data-ttu-id="9f0a1-106">**ITextureCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="9f0a1-106">The **ITextureCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9f0a1-107">**ITextureCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9f0a1-107">**ITextureCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="9f0a1-108">方法</span><span class="sxs-lookup"><span data-stu-id="9f0a1-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="9f0a1-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="9f0a1-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="9f0a1-110">**ITextureCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9f0a1-110">The **ITextureCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="9f0a1-111">方法</span><span class="sxs-lookup"><span data-stu-id="9f0a1-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="9f0a1-112">描述</span><span class="sxs-lookup"><span data-stu-id="9f0a1-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="9f0a1-113"><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f0a1-113"><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="9f0a1-114">通知主機的回呼。包含相關要求結果的 DDS (DirectDraw 介面) 檔案已就緒。</span><span class="sxs-lookup"><span data-stu-id="9f0a1-114">A callback that notifies the host that the .DDS (DirectDraw Surface) file containing results from the associated request are ready.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="9f0a1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f0a1-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9f0a1-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9f0a1-116">Header</span></span></p></td><td><span data-ttu-id="9f0a1-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9f0a1-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
