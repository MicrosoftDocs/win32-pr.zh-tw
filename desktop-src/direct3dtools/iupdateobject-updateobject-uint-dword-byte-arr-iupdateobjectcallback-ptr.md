---
description: 要求更新物件的初始狀態;例如紋理或著色器。
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IUpdateObject：： UpdateObject 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b04918878de15a2b9a5b004d3dff252ab3ddc9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467761"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span data-ttu-id="78968-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject：： UpdateObject 方法</span><span class="sxs-lookup"><span data-stu-id="78968-103"><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>IUpdateObject::UpdateObject method</span></span>

<span data-ttu-id="78968-104">要求更新物件的初始狀態;例如紋理或著色器。</span><span class="sxs-lookup"><span data-stu-id="78968-104">A request to update the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="78968-105">語法</span><span class="sxs-lookup"><span data-stu-id="78968-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="78968-106">參數</span><span class="sxs-lookup"><span data-stu-id="78968-106">Parameters</span></span>

<span data-ttu-id="78968-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="78968-107">*objectAddress* </span></span>  
<span data-ttu-id="78968-108">要更新之物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="78968-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="78968-109">*大小* </span><span class="sxs-lookup"><span data-stu-id="78968-109">*size* </span></span>  
<span data-ttu-id="78968-110">更新承載的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="78968-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="78968-111">*count1 \_ 緩衝區* </span><span class="sxs-lookup"><span data-stu-id="78968-111">*count1\_buffer* </span></span>  
<span data-ttu-id="78968-112">更新裝載。</span><span class="sxs-lookup"><span data-stu-id="78968-112">The update payload.</span></span>

<span data-ttu-id="78968-113">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="78968-113">*pCallback* </span></span>  
<span data-ttu-id="78968-114">用來通知主機物件已更新之函式的位址。</span><span class="sxs-lookup"><span data-stu-id="78968-114">The address of a function used to notify the host that the object was updated.</span></span>

## <a name="return-value"></a><span data-ttu-id="78968-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="78968-115">Return value</span></span>

<span data-ttu-id="78968-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="78968-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78968-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="78968-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78968-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="78968-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="78968-119">標頭</span><span class="sxs-lookup"><span data-stu-id="78968-119">Header</span></span></p></td><td><span data-ttu-id="78968-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="78968-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="78968-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="78968-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="78968-122">**IUpdateObject**</span><span class="sxs-lookup"><span data-stu-id="78968-122">**IUpdateObject**</span></span>](/windows/desktop/direct3dtools/iupdateobject)

 

 
