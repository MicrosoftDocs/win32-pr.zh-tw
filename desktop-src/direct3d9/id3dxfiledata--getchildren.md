---
description: 捕獲此檔案資料物件中的子係數目。
ms.assetid: ebc6905b-a453-4a15-adae-956ce7034084
title: 'ID3DXFileData：： GetChildren 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: dd6932801f3d4b079efa6f1ed2688505dbd7828b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982213"
---
# <a name="id3dxfiledatagetchildren-method"></a><span data-ttu-id="66ce0-103">ID3DXFileData：： GetChildren 方法</span><span class="sxs-lookup"><span data-stu-id="66ce0-103">ID3DXFileData::GetChildren method</span></span>

<span data-ttu-id="66ce0-104">捕獲此檔案資料物件中的子係數目。</span><span class="sxs-lookup"><span data-stu-id="66ce0-104">Retrieves the number of children in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ce0-105">語法</span><span class="sxs-lookup"><span data-stu-id="66ce0-105">Syntax</span></span>


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a><span data-ttu-id="66ce0-106">參數</span><span class="sxs-lookup"><span data-stu-id="66ce0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ce0-107">*puiChildren* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66ce0-107">*puiChildren* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66ce0-108">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="66ce0-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="66ce0-109">用來接收此檔案資料物件中子係數目之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="66ce0-109">Address of a pointer to receive the number of children in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ce0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="66ce0-110">Return value</span></span>

<span data-ttu-id="66ce0-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66ce0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66ce0-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="66ce0-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="66ce0-113">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="66ce0-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ce0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="66ce0-114">Requirements</span></span>



| <span data-ttu-id="66ce0-115">需求</span><span class="sxs-lookup"><span data-stu-id="66ce0-115">Requirement</span></span> | <span data-ttu-id="66ce0-116">值</span><span class="sxs-lookup"><span data-stu-id="66ce0-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66ce0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="66ce0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="66ce0-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="66ce0-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="66ce0-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="66ce0-119">Library</span></span><br/> | <dl> <span data-ttu-id="66ce0-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="66ce0-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="66ce0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66ce0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ce0-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="66ce0-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
