---
description: 抓取這個 ID3DXFileSaveObject 檔資料節點的指標。
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'ID3DXFileSaveData：： GetSave 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196435"
---
# <a name="id3dxfilesavedatagetsave-method"></a><span data-ttu-id="1ef4d-103">ID3DXFileSaveData：： GetSave 方法</span><span class="sxs-lookup"><span data-stu-id="1ef4d-103">ID3DXFileSaveData::GetSave method</span></span>

<span data-ttu-id="1ef4d-104">抓取這個 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 檔資料節點的指標。</span><span class="sxs-lookup"><span data-stu-id="1ef4d-104">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef4d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ef4d-105">Syntax</span></span>


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="1ef4d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ef4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef4d-107">*ppObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1ef4d-107">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef4d-108">類型： **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1ef4d-108">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="1ef4d-109">代表此檔案資料節點之 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 介面的指標位址。</span><span class="sxs-lookup"><span data-stu-id="1ef4d-109">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface representing this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef4d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ef4d-110">Return value</span></span>

<span data-ttu-id="1ef4d-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ef4d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ef4d-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1ef4d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1ef4d-113">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="1ef4d-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef4d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ef4d-114">Requirements</span></span>



| <span data-ttu-id="1ef4d-115">需求</span><span class="sxs-lookup"><span data-stu-id="1ef4d-115">Requirement</span></span> | <span data-ttu-id="1ef4d-116">值</span><span class="sxs-lookup"><span data-stu-id="1ef4d-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef4d-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1ef4d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1ef4d-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ef4d-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="1ef4d-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ef4d-119">Library</span></span><br/> | <dl> <span data-ttu-id="1ef4d-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ef4d-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1ef4d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ef4d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef4d-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="1ef4d-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




