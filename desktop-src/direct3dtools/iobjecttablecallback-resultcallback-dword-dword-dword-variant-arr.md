---
description: 用來通知主機物件資料表資訊的回呼函數。
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688375"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span data-ttu-id="9ef1f-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="9ef1f-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback::ResultCallback method</span></span>

<span data-ttu-id="9ef1f-104">用來通知主機物件資料表資訊的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="9ef1f-104">A callback function used to notify the host of object table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ef1f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9ef1f-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="9ef1f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9ef1f-106">Parameters</span></span>

<span data-ttu-id="9ef1f-107">*numElements* </span><span class="sxs-lookup"><span data-stu-id="9ef1f-107">*numElements* </span></span>  
<span data-ttu-id="9ef1f-108">所有物件之所有資料行中的總欄位數。</span><span class="sxs-lookup"><span data-stu-id="9ef1f-108">The total number of fields in all columns of all objects.</span></span>

<span data-ttu-id="9ef1f-109">*numRows* </span><span class="sxs-lookup"><span data-stu-id="9ef1f-109">*numRows* </span></span>  
<span data-ttu-id="9ef1f-110">正在傳送的物件數目。</span><span class="sxs-lookup"><span data-stu-id="9ef1f-110">The number of objects being transferred.</span></span>

<span data-ttu-id="9ef1f-111">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="9ef1f-111">*numColumns* </span></span>  
<span data-ttu-id="9ef1f-112">針對每個物件傳送的資訊 (欄位) 的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="9ef1f-112">The number of columns (fields) of information being transferred for each object.</span></span>

<span data-ttu-id="9ef1f-113">*count0 \_ pRowData* </span><span class="sxs-lookup"><span data-stu-id="9ef1f-113">*count0\_pRowData* </span></span>  
<span data-ttu-id="9ef1f-114">物件的相關資訊;每個物件的每個欄位都有一個專案。</span><span class="sxs-lookup"><span data-stu-id="9ef1f-114">Information about the objects; one item for each field of each object.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ef1f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ef1f-115">Return value</span></span>

<span data-ttu-id="9ef1f-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9ef1f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ef1f-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9ef1f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef1f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ef1f-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9ef1f-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9ef1f-119">Header</span></span></p></td><td><span data-ttu-id="9ef1f-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="9ef1f-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9ef1f-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ef1f-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9ef1f-122">**IObjectTableCallback**</span><span class="sxs-lookup"><span data-stu-id="9ef1f-122">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
