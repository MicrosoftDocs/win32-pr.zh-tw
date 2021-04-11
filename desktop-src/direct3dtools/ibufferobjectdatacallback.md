---
description: 回呼，以緩衝區形式傳回物件的內容，以供支援 (緩衝區、紋理) 的物件使用。
MS-HAID: vspixengine.IBufferObjectDataCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IBufferObjectDataCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAE4CE9A-B8EB-4ED6-9F48-D00C19B27A2E
api_name:
- IBufferObjectDataCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e5fb7deebd7d1b16d333ae59edab9372b54ad8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108945"
---
# <a name="span-idvspixengineibufferobjectdatacallbackspanibufferobjectdatacallback-interface"></a><span data-ttu-id="ea73e-103"><span id="vspixengine.ibufferobjectdatacallback"></span>IBufferObjectDataCallback 介面</span><span class="sxs-lookup"><span data-stu-id="ea73e-103"><span id="vspixengine.ibufferobjectdatacallback"></span>IBufferObjectDataCallback interface</span></span>

<span data-ttu-id="ea73e-104">回呼，以緩衝區形式傳回物件的內容，以供支援 (緩衝區、紋理) 的物件使用。</span><span class="sxs-lookup"><span data-stu-id="ea73e-104">Callback to return the contents of an object in buffer form for those that support it (buffers, textures).</span></span>

## <a name="members"></a><span data-ttu-id="ea73e-105">成員</span><span class="sxs-lookup"><span data-stu-id="ea73e-105">Members</span></span>

<span data-ttu-id="ea73e-106">**IBufferObjectDataCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="ea73e-106">The **IBufferObjectDataCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ea73e-107">**IBufferObjectDataCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ea73e-107">**IBufferObjectDataCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="ea73e-108">方法</span><span class="sxs-lookup"><span data-stu-id="ea73e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ea73e-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="ea73e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ea73e-110">**IBufferObjectDataCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ea73e-110">The **IBufferObjectDataCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ea73e-111">方法</span><span class="sxs-lookup"><span data-stu-id="ea73e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ea73e-112">描述</span><span class="sxs-lookup"><span data-stu-id="ea73e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ea73e-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea73e-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ea73e-114">回呼，會通知主機 assocaited 要求寫入檔案的緩衝區資訊。</span><span class="sxs-lookup"><span data-stu-id="ea73e-114">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ea73e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea73e-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ea73e-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ea73e-116">Header</span></span></p></td><td><span data-ttu-id="ea73e-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="ea73e-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
