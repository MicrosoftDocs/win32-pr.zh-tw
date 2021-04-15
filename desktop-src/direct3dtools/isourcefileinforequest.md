---
description: 從呼叫堆疊要求來源檔案資訊。
MS-HAID: vspixengine.ISourceFileInfoRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISourceFileInfoRequest 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 69C50343-32F0-46AE-B724-36EBD8AA8DF9
api_name:
- ISourceFileInfoRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b0aca47f2aa8a03db787cffcf911a30559aeeb82
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467762"
---
# <a name="span-idvspixengineisourcefileinforequestspanisourcefileinforequest-interface"></a><span data-ttu-id="e391a-103"><span id="vspixengine.isourcefileinforequest"></span>ISourceFileInfoRequest 介面</span><span class="sxs-lookup"><span data-stu-id="e391a-103"><span id="vspixengine.isourcefileinforequest"></span>ISourceFileInfoRequest interface</span></span>

<span data-ttu-id="e391a-104">從呼叫堆疊要求來源檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="e391a-104">Request for source file info from a callstack.</span></span>

## <a name="members"></a><span data-ttu-id="e391a-105">成員</span><span class="sxs-lookup"><span data-stu-id="e391a-105">Members</span></span>

<span data-ttu-id="e391a-106">**ISourceFileInfoRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e391a-106">The **ISourceFileInfoRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e391a-107">**ISourceFileInfoRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e391a-107">**ISourceFileInfoRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="e391a-108">方法</span><span class="sxs-lookup"><span data-stu-id="e391a-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e391a-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="e391a-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e391a-110">**ISourceFileInfoRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e391a-110">The **ISourceFileInfoRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e391a-111">方法</span><span class="sxs-lookup"><span data-stu-id="e391a-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e391a-112">描述</span><span class="sxs-lookup"><span data-stu-id="e391a-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e391a-113"><a href="/windows/desktop/direct3dtools/isourcefileinforequest-requestasync-eventid-isourcefileinfocallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="e391a-113"><a href="/windows/desktop/direct3dtools/isourcefileinforequest-requestasync-eventid-isourcefileinfocallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e391a-114">非同步要求，以取得與事件呼叫堆疊相關聯的原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="e391a-114">An asynchronous request to get the source files associated with the callstack of an event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e391a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e391a-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e391a-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e391a-116">Header</span></span></p></td><td><span data-ttu-id="e391a-117">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="e391a-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
