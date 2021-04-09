---
description: 抓取這個檔案資料物件中的子物件數目。
ms.assetid: 4409819f-a346-40b1-8e12-86e8128ece47
title: 'ID3DXFileEnumObject：： GetChildren 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: cafa79844e89602d3b88756e04ca460f611516dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696703"
---
# <a name="id3dxfileenumobjectgetchildren-method"></a><span data-ttu-id="4f198-103">ID3DXFileEnumObject：： GetChildren 方法</span><span class="sxs-lookup"><span data-stu-id="4f198-103">ID3DXFileEnumObject::GetChildren method</span></span>

<span data-ttu-id="4f198-104">抓取這個檔案資料物件中的子物件數目。</span><span class="sxs-lookup"><span data-stu-id="4f198-104">Retrieves the number of child objects in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f198-105">語法</span><span class="sxs-lookup"><span data-stu-id="4f198-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="4f198-106">參數</span><span class="sxs-lookup"><span data-stu-id="4f198-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f198-107">*puiChildren* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4f198-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f198-108">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4f198-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4f198-109">用來接收此檔案資料物件中子物件數目之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="4f198-109">Address of a pointer to receive the number of child objects in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f198-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f198-110">Return value</span></span>

<span data-ttu-id="4f198-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4f198-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4f198-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4f198-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4f198-113">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="4f198-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f198-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f198-114">Requirements</span></span>



| <span data-ttu-id="4f198-115">需求</span><span class="sxs-lookup"><span data-stu-id="4f198-115">Requirement</span></span> | <span data-ttu-id="4f198-116">值</span><span class="sxs-lookup"><span data-stu-id="4f198-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f198-117">標頭</span><span class="sxs-lookup"><span data-stu-id="4f198-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4f198-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f198-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="4f198-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="4f198-119">Library</span></span><br/> | <dl> <span data-ttu-id="4f198-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f198-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4f198-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f198-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f198-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="4f198-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
