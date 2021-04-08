---
title: ITfCoNtextRenderingMarkup 介面
description: ITfCoNtextRenderingMarkup 介面是由 TSF 管理員所執行，並由應用程式使用。 您可以使用 ITfCoNtext 物件的 IQueryInterface 來抓取這個介面。 這個介面可協助應用程式列舉呈現資訊。
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- ITfCoNtextRenderingMarkup 介面文字服務架構
- ITfCoNtextRenderingMarkup 介面文字服務架構，說明
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842467"
---
# <a name="itfcontextrenderingmarkup-interface"></a><span data-ttu-id="3c090-107">ITfCoNtextRenderingMarkup 介面</span><span class="sxs-lookup"><span data-stu-id="3c090-107">ITfContextRenderingMarkup interface</span></span>

<span data-ttu-id="3c090-108">**ITfCoNtextRenderingMarkup** 介面是由 TSF 管理員所執行，並由應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="3c090-108">The **ITfContextRenderingMarkup** interface is implemented by TSF manager and used by applications.</span></span> <span data-ttu-id="3c090-109">您可以使用 [ITfCoNtext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) 物件的 IQueryInterface 來抓取這個介面。</span><span class="sxs-lookup"><span data-stu-id="3c090-109">This interface can be retrieved using IQueryInterface from [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) object.</span></span> <span data-ttu-id="3c090-110">這個介面可協助應用程式列舉呈現資訊。</span><span class="sxs-lookup"><span data-stu-id="3c090-110">This interface helps the application enumerate rendering information.</span></span>



| <span data-ttu-id="3c090-111">ITfCoNtextRenderingMarkup 方法</span><span class="sxs-lookup"><span data-stu-id="3c090-111">ITfContextRenderingMarkup methods</span></span>                                                | <span data-ttu-id="3c090-112">Description</span><span class="sxs-lookup"><span data-stu-id="3c090-112">Description</span></span>                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="3c090-113">GetRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="3c090-113">GetRenderingMarkup</span></span>](itfcontextrenderingmarkup-getrenderingmarkup.md)           | <span data-ttu-id="3c090-114">抓取指定範圍之轉譯標記的列舉值。</span><span class="sxs-lookup"><span data-stu-id="3c090-114">Retrieves an enumerator of the rendering markups for the given range.</span></span> |
| [<span data-ttu-id="3c090-115">FindNextRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="3c090-115">FindNextRenderingMarkup</span></span>](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | <span data-ttu-id="3c090-116">此函數並未實作。</span><span class="sxs-lookup"><span data-stu-id="3c090-116">This function is not implemented.</span></span> <span data-ttu-id="3c090-117">它一律會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="3c090-117">It always returns E\_NOTIMPL.</span></span>       |



 

## <a name="members"></a><span data-ttu-id="3c090-118">成員</span><span class="sxs-lookup"><span data-stu-id="3c090-118">Members</span></span>

<span data-ttu-id="3c090-119">**ITfCoNtextRenderingMarkup** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面，但沒有其他成員。</span><span class="sxs-lookup"><span data-stu-id="3c090-119">The **ITfContextRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c090-120">備註</span><span class="sxs-lookup"><span data-stu-id="3c090-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c090-121">這個介面目前不在公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="3c090-121">This interface is not currently in the public header files.</span></span> <span data-ttu-id="3c090-122">若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="3c090-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 