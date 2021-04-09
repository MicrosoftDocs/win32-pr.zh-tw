---
description: 回呼，用來通知主機物件已更新。
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IUpdateObjectCallback：： UpdateComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109297"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span data-ttu-id="44c80-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback：： UpdateComplete 方法</span><span class="sxs-lookup"><span data-stu-id="44c80-103"><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>IUpdateObjectCallback::UpdateComplete method</span></span>

<span data-ttu-id="44c80-104">回呼，用來通知主機物件已更新。</span><span class="sxs-lookup"><span data-stu-id="44c80-104">A callback used to notify the host that an object was updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="44c80-105">語法</span><span class="sxs-lookup"><span data-stu-id="44c80-105">Syntax</span></span>


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a><span data-ttu-id="44c80-106">參數</span><span class="sxs-lookup"><span data-stu-id="44c80-106">Parameters</span></span>

<span data-ttu-id="44c80-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="44c80-107">*objectAddress* </span></span>  
<span data-ttu-id="44c80-108">已更新之物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="44c80-108">The ID of the object that was updated.</span></span>

<span data-ttu-id="44c80-109">*結果* </span><span class="sxs-lookup"><span data-stu-id="44c80-109">*result* </span></span>  
<span data-ttu-id="44c80-110">指出更新是否成功。</span><span class="sxs-lookup"><span data-stu-id="44c80-110">Indicates whether or not the update succeeded.</span></span>

## <a name="return-value"></a><span data-ttu-id="44c80-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="44c80-111">Return value</span></span>

<span data-ttu-id="44c80-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="44c80-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44c80-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="44c80-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44c80-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="44c80-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="44c80-115">標頭</span><span class="sxs-lookup"><span data-stu-id="44c80-115">Header</span></span></p></td><td><span data-ttu-id="44c80-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="44c80-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="44c80-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="44c80-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="44c80-118">**IUpdateObjectCallback**</span><span class="sxs-lookup"><span data-stu-id="44c80-118">**IUpdateObjectCallback**</span></span>](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
