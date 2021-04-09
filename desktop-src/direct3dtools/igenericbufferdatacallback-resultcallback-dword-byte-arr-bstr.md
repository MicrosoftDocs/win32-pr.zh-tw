---
description: 回呼，會通知主機 assocaited 要求所傳回的泛型緩衝區資訊。
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IGenericBufferDataCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: be2d6aa7cd5e844cd5d1297c16de2ebb21c939a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688252"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span data-ttu-id="3a1e2-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="3a1e2-103"><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback::ResultCallback method</span></span>

<span data-ttu-id="3a1e2-104">回呼，會通知主機 assocaited 要求所傳回的泛型緩衝區資訊。</span><span class="sxs-lookup"><span data-stu-id="3a1e2-104">A callback that notifies the host of generic buffer information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="3a1e2-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a><span data-ttu-id="3a1e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="3a1e2-106">Parameters</span></span>

<span data-ttu-id="3a1e2-107">*大小* </span><span class="sxs-lookup"><span data-stu-id="3a1e2-107">*size* </span></span>  
<span data-ttu-id="3a1e2-108">緩衝區內容的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a1e2-108">The size of the buffer contents in bytes.</span></span>

<span data-ttu-id="3a1e2-109">*count0 \_ 緩衝區* </span><span class="sxs-lookup"><span data-stu-id="3a1e2-109">*count0\_buffer* </span></span>  
<span data-ttu-id="3a1e2-110">緩衝區內容。</span><span class="sxs-lookup"><span data-stu-id="3a1e2-110">The buffer contents.</span></span> <span data-ttu-id="3a1e2-111">在大部分的情況下，這是 XML 資料。</span><span class="sxs-lookup"><span data-stu-id="3a1e2-111">In most cases this is XML data.</span></span>

<span data-ttu-id="3a1e2-112">*類型* </span><span class="sxs-lookup"><span data-stu-id="3a1e2-112">*type* </span></span>  
<span data-ttu-id="3a1e2-113">COM 字串，表示緩衝區中傳回的內容類型。</span><span class="sxs-lookup"><span data-stu-id="3a1e2-113">A COM string that indicates the type of content returned in the buffer.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a1e2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a1e2-114">Return value</span></span>

<span data-ttu-id="3a1e2-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3a1e2-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a1e2-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3a1e2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1e2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a1e2-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3a1e2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="3a1e2-118">Header</span></span></p></td><td><span data-ttu-id="3a1e2-119">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="3a1e2-119">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3a1e2-120"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a1e2-120"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3a1e2-121">**IGenericBufferDataCallback**</span><span class="sxs-lookup"><span data-stu-id="3a1e2-121">**IGenericBufferDataCallback**</span></span>](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
