---
description: 將資源傳遞給引擎，例如錯誤訊息的字串。
MS-HAID: vspixengine.IPixEngine3\_SetupResources\_ResourcePair\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine3：： SetupResources 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1BB4BE17-51A2-4BA4-81F5-3678B7D5802B
api_name:
- IPixEngine3.SetupResources
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c2b103c5c27bf3929f72d909c9000a1e252e8dee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109320"
---
# <a name="span-idvspixengineipixengine3_setupresources_resourcepair_arr_uintspanipixengine3setupresources-method"></a><span data-ttu-id="1ff33-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3：： SetupResources 方法</span><span class="sxs-lookup"><span data-stu-id="1ff33-103"><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3::SetupResources method</span></span>

<span data-ttu-id="1ff33-104">將資源傳遞給引擎，例如錯誤訊息的字串。</span><span class="sxs-lookup"><span data-stu-id="1ff33-104">Passes resources to the engine, such as strings for error messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff33-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ff33-105">Syntax</span></span>


```C++
HRESULT SetupResources(
   ResourcePair [] count1_resources,
   UINT            count
);
```

## <a name="parameters"></a><span data-ttu-id="1ff33-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ff33-106">Parameters</span></span>

<span data-ttu-id="1ff33-107">*count1 \_ 資源* </span><span class="sxs-lookup"><span data-stu-id="1ff33-107">*count1\_resources* </span></span>  
<span data-ttu-id="1ff33-108">傳遞的資源資源。</span><span class="sxs-lookup"><span data-stu-id="1ff33-108">The resources resources passed.</span></span>

<span data-ttu-id="1ff33-109">*計數* </span><span class="sxs-lookup"><span data-stu-id="1ff33-109">*count* </span></span>  
<span data-ttu-id="1ff33-110">傳遞的資源數目。</span><span class="sxs-lookup"><span data-stu-id="1ff33-110">The number of resources passed.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ff33-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ff33-111">Return value</span></span>

<span data-ttu-id="1ff33-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1ff33-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1ff33-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1ff33-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff33-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ff33-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1ff33-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1ff33-115">Header</span></span></p></td><td><span data-ttu-id="1ff33-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="1ff33-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1ff33-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ff33-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1ff33-118">**IPixEngine3**</span><span class="sxs-lookup"><span data-stu-id="1ff33-118">**IPixEngine3**</span></span>](/windows/desktop/direct3dtools/ipixengine3)

 

 
