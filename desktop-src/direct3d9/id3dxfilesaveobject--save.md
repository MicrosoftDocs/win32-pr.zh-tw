---
description: 將資料物件和其子系儲存至磁片上的. x 檔案。
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'ID3DXFileSaveObject：： Save 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386457"
---
# <a name="id3dxfilesaveobjectsave-method"></a><span data-ttu-id="282c1-103">ID3DXFileSaveObject：： Save 方法</span><span class="sxs-lookup"><span data-stu-id="282c1-103">ID3DXFileSaveObject::Save method</span></span>

<span data-ttu-id="282c1-104">將資料物件和其子系儲存至磁片上的. x 檔案。</span><span class="sxs-lookup"><span data-stu-id="282c1-104">Saves a data object and its children to a .x file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="282c1-105">語法</span><span class="sxs-lookup"><span data-stu-id="282c1-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="282c1-106">參數</span><span class="sxs-lookup"><span data-stu-id="282c1-106">Parameters</span></span>

<span data-ttu-id="282c1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="282c1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="282c1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="282c1-108">Return value</span></span>

<span data-ttu-id="282c1-109">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="282c1-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="282c1-110">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="282c1-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="282c1-111">如果方法失敗，則傳回值可以是下列值： D3DXFERR \_ BADOBJECT。</span><span class="sxs-lookup"><span data-stu-id="282c1-111">If the method fails, the return value can be the following: D3DXFERR\_BADOBJECT.</span></span>

## <a name="remarks"></a><span data-ttu-id="282c1-112">備註</span><span class="sxs-lookup"><span data-stu-id="282c1-112">Remarks</span></span>

<span data-ttu-id="282c1-113">在這個方法成功之後，您就無法再呼叫 [**ID3DXFileSaveObject：： AddDataObject**](id3dxfilesaveobject--adddataobject.md)、 [**ID3DXFileSaveData：： AddDataObject**](id3dxfilesavedata--adddataobject.md) 和 [**ID3DXFileSaveData：： AddDataReference**](id3dxfilesavedata--adddatareference.md) ，直到建立新的 [**ID3DXFile**](id3dxfile.md) 物件為止。</span><span class="sxs-lookup"><span data-stu-id="282c1-113">After this method succeeds, [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) and [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) can no longer be called until a new [**ID3DXFile**](id3dxfile.md) object is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="282c1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="282c1-114">Requirements</span></span>



| <span data-ttu-id="282c1-115">需求</span><span class="sxs-lookup"><span data-stu-id="282c1-115">Requirement</span></span> | <span data-ttu-id="282c1-116">值</span><span class="sxs-lookup"><span data-stu-id="282c1-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="282c1-117">標頭</span><span class="sxs-lookup"><span data-stu-id="282c1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="282c1-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="282c1-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="282c1-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="282c1-119">Library</span></span><br/> | <dl> <span data-ttu-id="282c1-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="282c1-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="282c1-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="282c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="282c1-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="282c1-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




