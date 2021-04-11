---
description: 抓取物件之範本的 GUID。 已取代。
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'IDirectXFileData：： GetType 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116261"
---
# <a name="idirectxfiledatagettype-method"></a><span data-ttu-id="2ad26-104">IDirectXFileData：： GetType 方法</span><span class="sxs-lookup"><span data-stu-id="2ad26-104">IDirectXFileData::GetType method</span></span>

<span data-ttu-id="2ad26-105">抓取物件之範本的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2ad26-105">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="2ad26-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="2ad26-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ad26-107">語法</span><span class="sxs-lookup"><span data-stu-id="2ad26-107">Syntax</span></span>


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a><span data-ttu-id="2ad26-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ad26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad26-109">*ppguid* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="2ad26-109">*ppguid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2ad26-110">類型： **Const [**GUID**](guid.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="2ad26-110">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="2ad26-111">接收物件的範本 GUID 之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="2ad26-111">Address of a pointer to receive the GUID of the object's template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad26-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ad26-112">Return value</span></span>

<span data-ttu-id="2ad26-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ad26-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ad26-114">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2ad26-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="2ad26-115">如果方法失敗，則傳回值可以是 DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="2ad26-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad26-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ad26-116">Requirements</span></span>



| <span data-ttu-id="2ad26-117">需求</span><span class="sxs-lookup"><span data-stu-id="2ad26-117">Requirement</span></span> | <span data-ttu-id="2ad26-118">值</span><span class="sxs-lookup"><span data-stu-id="2ad26-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad26-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2ad26-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2ad26-120"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ad26-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ad26-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="2ad26-121">Library</span></span><br/> | <dl> <span data-ttu-id="2ad26-122"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ad26-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ad26-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ad26-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad26-124">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="2ad26-124">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 




