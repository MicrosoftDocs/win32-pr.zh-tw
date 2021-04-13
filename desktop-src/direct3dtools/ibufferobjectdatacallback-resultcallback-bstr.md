---
description: 回呼，會通知主機 assocaited 要求寫入檔案的緩衝區資訊。
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IBufferObjectDataCallback：： ResultCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385832"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span data-ttu-id="73f92-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback：： ResultCallback 方法</span><span class="sxs-lookup"><span data-stu-id="73f92-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback::ResultCallback method</span></span>

<span data-ttu-id="73f92-104">回呼，會通知主機 assocaited 要求寫入檔案的緩衝區資訊。</span><span class="sxs-lookup"><span data-stu-id="73f92-104">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f92-105">語法</span><span class="sxs-lookup"><span data-stu-id="73f92-105">Syntax</span></span>

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a><span data-ttu-id="73f92-106">參數</span><span class="sxs-lookup"><span data-stu-id="73f92-106">Parameters</span></span>

<span data-ttu-id="73f92-107">檔案COM 字串，其中包含寫入結果之檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="73f92-107">*File* A COM string that contains the pathname of the file where results are written.</span></span>

## <a name="return-value"></a><span data-ttu-id="73f92-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="73f92-108">Return value</span></span>

<span data-ttu-id="73f92-109">如果這個方法成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="73f92-109">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="73f92-110">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73f92-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73f92-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="73f92-111">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="73f92-112">標頭</span><span class="sxs-lookup"><span data-stu-id="73f92-112">Header</span></span></p></td><td><span data-ttu-id="73f92-113">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="73f92-113">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="73f92-114"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="73f92-114"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="73f92-115">**IBufferObjectDataCallback**</span><span class="sxs-lookup"><span data-stu-id="73f92-115">**IBufferObjectDataCallback**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
