---
description: 更新物件的初始狀態;例如紋理或著色器。
MS-HAID: vspixengine.IPixEngine4\_UpdateObject\_UINT\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine4：： UpdateObject 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90B1DE4F-7DF5-44C9-9A57-1BFB6825EB58
api_name:
- IPixEngine4.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6f21bac93bea44cb7226897a89460788c3900b8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467574"
---
# <a name="span-idvspixengineipixengine4_updateobject_uint_dword_byte_arrspanipixengine4updateobject-method"></a><span data-ttu-id="53e41-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4：： UpdateObject 方法</span><span class="sxs-lookup"><span data-stu-id="53e41-103"><span id="vspixengine.ipixengine4_updateobject_uint_dword_byte_arr"></span>IPixEngine4::UpdateObject method</span></span>

<span data-ttu-id="53e41-104">更新物件的初始狀態;例如紋理或著色器。</span><span class="sxs-lookup"><span data-stu-id="53e41-104">Updates the initial state of an object; for example, a texture or shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e41-105">語法</span><span class="sxs-lookup"><span data-stu-id="53e41-105">Syntax</span></span>


```C++
HRESULT UpdateObject(
   UINT    objectAddress,
   DWORD   size,
   BYTE [] count1_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="53e41-106">參數</span><span class="sxs-lookup"><span data-stu-id="53e41-106">Parameters</span></span>

<span data-ttu-id="53e41-107">*objectAddress* </span><span class="sxs-lookup"><span data-stu-id="53e41-107">*objectAddress* </span></span>  
<span data-ttu-id="53e41-108">要更新之物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="53e41-108">The ID of the object to be updated.</span></span>

<span data-ttu-id="53e41-109">*大小* </span><span class="sxs-lookup"><span data-stu-id="53e41-109">*size* </span></span>  
<span data-ttu-id="53e41-110">更新承載的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="53e41-110">The size of the update payload in bytes.</span></span>

<span data-ttu-id="53e41-111">*count1 \_ 緩衝區* </span><span class="sxs-lookup"><span data-stu-id="53e41-111">*count1\_buffer* </span></span>  
<span data-ttu-id="53e41-112">更新裝載。</span><span class="sxs-lookup"><span data-stu-id="53e41-112">The update payload.</span></span>

## <a name="return-value"></a><span data-ttu-id="53e41-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="53e41-113">Return value</span></span>

<span data-ttu-id="53e41-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="53e41-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53e41-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53e41-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e41-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="53e41-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="53e41-117">標頭</span><span class="sxs-lookup"><span data-stu-id="53e41-117">Header</span></span></p></td><td><span data-ttu-id="53e41-118">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="53e41-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="53e41-119"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="53e41-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="53e41-120">**IPixEngine4**</span><span class="sxs-lookup"><span data-stu-id="53e41-120">**IPixEngine4**</span></span>](/windows/desktop/direct3dtools/ipixengine4)

 

 
