---
description: 取得事件清單) 支援的事件資料行 (類型相關資訊。
MS-HAID: vspixengine.IFrameEventsCallback\_GetSupportedEventColumns\_DWORD\_EventColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsCallback：： GetSupportedEventColumns 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F1BFF189-A22C-4058-A427-74653998DD27
api_name:
- IFrameEventsCallback.GetSupportedEventColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5b7bc9f74998a061ea63fca925263b7b4a0a4d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467747"
---
# <a name="span-idvspixengineiframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arrspaniframeeventscallbackgetsupportedeventcolumns-method"></a><span data-ttu-id="fe8ba-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback：： GetSupportedEventColumns 方法</span><span class="sxs-lookup"><span data-stu-id="fe8ba-103"><span id="vspixengine.iframeeventscallback_getsupportedeventcolumns_dword_eventcolumnid_arr_bstr_arr"></span>IFrameEventsCallback::GetSupportedEventColumns method</span></span>

<span data-ttu-id="fe8ba-104">取得事件清單) 支援的事件資料行 (類型相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe8ba-104">Gets information about which columns (types of event data) are supported by the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe8ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe8ba-105">Syntax</span></span>


```C++
HRESULT GetSupportedEventColumns(
   DWORD            numColumns,
   EventColumnID [] count0_pIDs,
   BSTR []          count0_pBstrNames
);
```

## <a name="parameters"></a><span data-ttu-id="fe8ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe8ba-106">Parameters</span></span>

<span data-ttu-id="fe8ba-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="fe8ba-107">*numColumns* </span></span>  
<span data-ttu-id="fe8ba-108">支援的資料行數目</span><span class="sxs-lookup"><span data-stu-id="fe8ba-108">The number of columns supported by</span></span>

<span data-ttu-id="fe8ba-109">*count0 \_ pid* </span><span class="sxs-lookup"><span data-stu-id="fe8ba-109">*count0\_pIDs* </span></span>  
<span data-ttu-id="fe8ba-110">事件清單所支援之每個資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe8ba-110">The IDs of each column supported by the event list.</span></span>

<span data-ttu-id="fe8ba-111">*count0 \_ pBstrNames* </span><span class="sxs-lookup"><span data-stu-id="fe8ba-111">*count0\_pBstrNames* </span></span>  
<span data-ttu-id="fe8ba-112">事件清單所支援之每個資料行的名稱，做為 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="fe8ba-112">The names of each column, as a COM string, supported by the event list.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe8ba-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe8ba-113">Return value</span></span>

<span data-ttu-id="fe8ba-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fe8ba-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe8ba-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe8ba-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8ba-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe8ba-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fe8ba-117">標頭</span><span class="sxs-lookup"><span data-stu-id="fe8ba-117">Header</span></span></p></td><td><span data-ttu-id="fe8ba-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fe8ba-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fe8ba-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe8ba-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fe8ba-120">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="fe8ba-120">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
