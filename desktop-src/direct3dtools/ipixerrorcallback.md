---
description: 從引擎回呼以處理錯誤。
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixErrorCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385630"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span data-ttu-id="4b38a-103"><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback 介面</span><span class="sxs-lookup"><span data-stu-id="4b38a-103"><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback interface</span></span>

<span data-ttu-id="4b38a-104">從引擎回呼以處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b38a-104">Callback from engine to handle errors.</span></span>

## <a name="members"></a><span data-ttu-id="4b38a-105">成員</span><span class="sxs-lookup"><span data-stu-id="4b38a-105">Members</span></span>

<span data-ttu-id="4b38a-106">**IPixErrorCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="4b38a-106">The **IPixErrorCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4b38a-107">**IPixErrorCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4b38a-107">**IPixErrorCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="4b38a-108">方法</span><span class="sxs-lookup"><span data-stu-id="4b38a-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="4b38a-109"><span id="methods"></span>方法</span><span class="sxs-lookup"><span data-stu-id="4b38a-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="4b38a-110">**IPixErrorCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4b38a-110">The **IPixErrorCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="4b38a-111">方法</span><span class="sxs-lookup"><span data-stu-id="4b38a-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="4b38a-112">描述</span><span class="sxs-lookup"><span data-stu-id="4b38a-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4b38a-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b38a-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4b38a-114">回呼，會通知主機相關要求所傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4b38a-114">A callback that notifies the host of errors returned by the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="4b38a-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b38a-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4b38a-116">回呼，會通知主機相關要求所傳回的訊息。</span><span class="sxs-lookup"><span data-stu-id="4b38a-116">A callback that notifies the host of messages returned by the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="4b38a-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b38a-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="4b38a-118">回呼，會通知主機相關要求所傳回的警告。</span><span class="sxs-lookup"><span data-stu-id="4b38a-118">A callback that notifies the host of warnings returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="4b38a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b38a-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4b38a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4b38a-120">Header</span></span></p></td><td><span data-ttu-id="4b38a-121">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="4b38a-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
