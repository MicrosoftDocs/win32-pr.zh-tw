---
description: 抓取此檔案資料節點的範本識別碼。
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: 'ID3DXFileSaveData：： GetType 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b774f71b4be111efcdbdaf8bc41b40d4b0efaa95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992135"
---
# <a name="id3dxfilesavedatagettype-method"></a><span data-ttu-id="8573e-103">ID3DXFileSaveData：： GetType 方法</span><span class="sxs-lookup"><span data-stu-id="8573e-103">ID3DXFileSaveData::GetType method</span></span>

<span data-ttu-id="8573e-104">抓取此檔案資料節點的範本識別碼。</span><span class="sxs-lookup"><span data-stu-id="8573e-104">Retrieves the template ID of this file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="8573e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8573e-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a><span data-ttu-id="8573e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8573e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8573e-107">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8573e-107">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8573e-108">類型： **[ **GUID**](guid.md)\***</span><span class="sxs-lookup"><span data-stu-id="8573e-108">Type: **[**GUID**](guid.md)\***</span></span>

<span data-ttu-id="8573e-109">GUID 的指標，代表這個檔案資料節點中的範本。</span><span class="sxs-lookup"><span data-stu-id="8573e-109">Pointer to the GUID representing the template in this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8573e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8573e-110">Return value</span></span>

<span data-ttu-id="8573e-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8573e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8573e-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="8573e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8573e-113">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADOBJECT，D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="8573e-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="8573e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8573e-114">Requirements</span></span>



| <span data-ttu-id="8573e-115">需求</span><span class="sxs-lookup"><span data-stu-id="8573e-115">Requirement</span></span> | <span data-ttu-id="8573e-116">值</span><span class="sxs-lookup"><span data-stu-id="8573e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8573e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8573e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8573e-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="8573e-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="8573e-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8573e-119">Library</span></span><br/> | <dl> <span data-ttu-id="8573e-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8573e-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8573e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8573e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8573e-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="8573e-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




