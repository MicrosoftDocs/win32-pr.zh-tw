---
description: 要求取得此物件資料表要求類型所支援之資料行 (欄位) 的相關資訊。
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableRequest：： RequestSupportedColumnsAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6773a69061e7a17d2271e1a53f89f6f2def1a6c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510348"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="f28a3-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest：： RequestSupportedColumnsAsync 方法</span><span class="sxs-lookup"><span data-stu-id="f28a3-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="f28a3-104">要求取得此物件資料表要求類型所支援之資料行 (欄位) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f28a3-104">Requests to get information about what columns (fields) this object table request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="f28a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="f28a3-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f28a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="f28a3-106">Parameters</span></span>

<span data-ttu-id="f28a3-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="f28a3-107">*requestCallback* </span></span>  
<span data-ttu-id="f28a3-108">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="f28a3-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="f28a3-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="f28a3-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f28a3-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="f28a3-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f28a3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f28a3-111">Return value</span></span>

<span data-ttu-id="f28a3-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f28a3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f28a3-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f28a3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f28a3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f28a3-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f28a3-115">標頭</span><span class="sxs-lookup"><span data-stu-id="f28a3-115">Header</span></span></p></td><td><span data-ttu-id="f28a3-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="f28a3-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f28a3-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="f28a3-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f28a3-118">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="f28a3-118">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
