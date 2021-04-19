---
description: 抓取識別 DirectX 檔案物件的 GUID 指標。 已取代。
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'IDirectXFileObject：： GetId 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988179"
---
# <a name="idirectxfileobjectgetid-method"></a><span data-ttu-id="d0ac4-104">IDirectXFileObject：： GetId 方法</span><span class="sxs-lookup"><span data-stu-id="d0ac4-104">IDirectXFileObject::GetId method</span></span>

<span data-ttu-id="d0ac4-105">抓取識別 DirectX 檔案物件的 GUID 指標。</span><span class="sxs-lookup"><span data-stu-id="d0ac4-105">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="d0ac4-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="d0ac4-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ac4-107">語法</span><span class="sxs-lookup"><span data-stu-id="d0ac4-107">Syntax</span></span>


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="d0ac4-108">參數</span><span class="sxs-lookup"><span data-stu-id="d0ac4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ac4-109">*pGuid* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="d0ac4-109">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ac4-110">類型： **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="d0ac4-110">Type: **LPGUID**</span></span>

<span data-ttu-id="d0ac4-111">要接收物件識別碼之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="d0ac4-111">Pointer to a GUID to receive the object's ID.</span></span> <span data-ttu-id="d0ac4-112">如果物件沒有識別碼，此函式會將 GUID 設定為 **Null** guid。</span><span class="sxs-lookup"><span data-stu-id="d0ac4-112">The function will set the GUID to a **NULL** GUID if the object does not have an ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ac4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0ac4-113">Return value</span></span>

<span data-ttu-id="d0ac4-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0ac4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0ac4-115">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d0ac4-115">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d0ac4-116">如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="d0ac4-116">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ac4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0ac4-117">Requirements</span></span>



| <span data-ttu-id="d0ac4-118">需求</span><span class="sxs-lookup"><span data-stu-id="d0ac4-118">Requirement</span></span> | <span data-ttu-id="d0ac4-119">值</span><span class="sxs-lookup"><span data-stu-id="d0ac4-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ac4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d0ac4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d0ac4-121"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0ac4-121"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0ac4-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="d0ac4-122">Library</span></span><br/> | <dl> <span data-ttu-id="d0ac4-123"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0ac4-123"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ac4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0ac4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ac4-125">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="d0ac4-125">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 




