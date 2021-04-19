---
description: 抓取這個 ID3DXFileSaveData 檔資料節點的 GUID。
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'ID3DXFileSaveData：： GetId 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982890"
---
# <a name="id3dxfilesavedatagetid-method"></a><span data-ttu-id="abcf0-103">ID3DXFileSaveData：： GetId 方法</span><span class="sxs-lookup"><span data-stu-id="abcf0-103">ID3DXFileSaveData::GetId method</span></span>

<span data-ttu-id="abcf0-104">抓取這個 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 檔資料節點的 GUID。</span><span class="sxs-lookup"><span data-stu-id="abcf0-104">Retrieves the GUID of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="abcf0-105">語法</span><span class="sxs-lookup"><span data-stu-id="abcf0-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="abcf0-106">參數</span><span class="sxs-lookup"><span data-stu-id="abcf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abcf0-107">*pId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="abcf0-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abcf0-108">類型： **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="abcf0-108">Type: **LPGUID**</span></span>

<span data-ttu-id="abcf0-109">用來接收此檔案資料節點識別碼之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="abcf0-109">Pointer to a GUID to receive the ID of this file data node.</span></span> <span data-ttu-id="abcf0-110">如果物件沒有識別碼，傳回的參數值將會是 GUID \_ Null。</span><span class="sxs-lookup"><span data-stu-id="abcf0-110">If the object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abcf0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="abcf0-111">Return value</span></span>

<span data-ttu-id="abcf0-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abcf0-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abcf0-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="abcf0-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="abcf0-114">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="abcf0-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="abcf0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="abcf0-115">Requirements</span></span>



| <span data-ttu-id="abcf0-116">需求</span><span class="sxs-lookup"><span data-stu-id="abcf0-116">Requirement</span></span> | <span data-ttu-id="abcf0-117">值</span><span class="sxs-lookup"><span data-stu-id="abcf0-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abcf0-118">標頭</span><span class="sxs-lookup"><span data-stu-id="abcf0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="abcf0-119"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="abcf0-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="abcf0-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="abcf0-120">Library</span></span><br/> | <dl> <span data-ttu-id="abcf0-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="abcf0-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="abcf0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abcf0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abcf0-123">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="abcf0-123">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




