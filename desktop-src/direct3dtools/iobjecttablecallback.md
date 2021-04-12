---
description: 傳回物件資料表資料的回呼。
MS-HAID: vspixengine.IObjectTableCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D3B5ECD5-DBE1-4E37-8707-CFAEFEE551F1
api_name:
- IObjectTableCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4535164048c92e6af381d15ee388212fdc72da4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109869"
---
# <a name="span-idvspixengineiobjecttablecallbackspaniobjecttablecallback-interface"></a><span data-ttu-id="93d87-103"><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback 介面</span><span class="sxs-lookup"><span data-stu-id="93d87-103"><span id="vspixengine.iobjecttablecallback"></span>IObjectTableCallback interface</span></span>

<span data-ttu-id="93d87-104">傳回物件資料表資料的回呼。</span><span class="sxs-lookup"><span data-stu-id="93d87-104">Callback to return object table data.</span></span>

## <a name="members"></a><span data-ttu-id="93d87-105">成員</span><span class="sxs-lookup"><span data-stu-id="93d87-105">Members</span></span>

<span data-ttu-id="93d87-106">**IObjectTableCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="93d87-106">The **IObjectTableCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="93d87-107">**IObjectTableCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93d87-107">**IObjectTableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="93d87-108">方法</span><span class="sxs-lookup"><span data-stu-id="93d87-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="93d87-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="93d87-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="93d87-110">**IObjectTableCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="93d87-110">The **IObjectTableCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="93d87-111">方法</span><span class="sxs-lookup"><span data-stu-id="93d87-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="93d87-112">描述</span><span class="sxs-lookup"><span data-stu-id="93d87-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="93d87-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="93d87-113"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-getsupportedcolumns-dword-objecttablecolumnid-arr-bstr-arr"><strong>GetSupportedColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="93d87-114">取得物件資料表支援哪些資料行 (物件資料) 類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="93d87-114">Gets information about which columns (types of object data) are supported by the object table.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="93d87-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="93d87-115"><a href="/windows/desktop/direct3dtools/iobjecttablecallback-resultcallback-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="93d87-116">用來通知主機物件資料表資訊的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="93d87-116">A callback function used to notify the host of object table information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="93d87-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="93d87-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="93d87-118">標頭</span><span class="sxs-lookup"><span data-stu-id="93d87-118">Header</span></span></p></td><td><span data-ttu-id="93d87-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="93d87-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
