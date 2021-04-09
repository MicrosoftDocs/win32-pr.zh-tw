---
description: 從呼叫堆疊傳回來源檔案資訊的回呼。
MS-HAID: vspixengine.ISourceFileInfoCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISourceFileInfoCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0430DFF0-F3EA-4645-9B91-E849C0F99609
api_name:
- ISourceFileInfoCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c627d07bfbf455a9c62a922f62adcab945d5741
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688468"
---
# <a name="span-idvspixengineisourcefileinfocallbackspanisourcefileinfocallback-interface"></a><span data-ttu-id="1bd11-103"><span id="vspixengine.isourcefileinfocallback"></span>ISourceFileInfoCallback 介面</span><span class="sxs-lookup"><span data-stu-id="1bd11-103"><span id="vspixengine.isourcefileinfocallback"></span>ISourceFileInfoCallback interface</span></span>

<span data-ttu-id="1bd11-104">從呼叫堆疊傳回來源檔案資訊的回呼。</span><span class="sxs-lookup"><span data-stu-id="1bd11-104">Callback to return source file info from a callstack.</span></span>

## <a name="members"></a><span data-ttu-id="1bd11-105">成員</span><span class="sxs-lookup"><span data-stu-id="1bd11-105">Members</span></span>

<span data-ttu-id="1bd11-106">**ISourceFileInfoCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1bd11-106">The **ISourceFileInfoCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1bd11-107">**ISourceFileInfoCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1bd11-107">**ISourceFileInfoCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="1bd11-108">方法</span><span class="sxs-lookup"><span data-stu-id="1bd11-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="1bd11-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="1bd11-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="1bd11-110">**ISourceFileInfoCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1bd11-110">The **ISourceFileInfoCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="1bd11-111">方法</span><span class="sxs-lookup"><span data-stu-id="1bd11-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="1bd11-112">描述</span><span class="sxs-lookup"><span data-stu-id="1bd11-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="1bd11-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="1bd11-113"><a href="/windows/desktop/direct3dtools/isourcefileinfocallback-resultcallback-dword-sourcefileinfo-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1bd11-114">回呼函式，用來通知主機與呼叫堆疊相關聯之來源檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1bd11-114">A callback function used to notify the host of information about source files associated with the callstack.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="1bd11-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bd11-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1bd11-116">標頭</span><span class="sxs-lookup"><span data-stu-id="1bd11-116">Header</span></span></p></td><td><span data-ttu-id="1bd11-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="1bd11-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
