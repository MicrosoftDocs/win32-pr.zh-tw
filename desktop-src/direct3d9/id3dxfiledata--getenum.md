---
description: 抓取這個檔案資料物件中的列舉物件。
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'ID3DXFileData：： GetEnum 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001517"
---
# <a name="id3dxfiledatagetenum-method"></a><span data-ttu-id="0775e-103">ID3DXFileData：： GetEnum 方法</span><span class="sxs-lookup"><span data-stu-id="0775e-103">ID3DXFileData::GetEnum method</span></span>

<span data-ttu-id="0775e-104">抓取這個檔案資料物件中的列舉物件。</span><span class="sxs-lookup"><span data-stu-id="0775e-104">Retrieves the enumeration object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0775e-105">語法</span><span class="sxs-lookup"><span data-stu-id="0775e-105">Syntax</span></span>


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="0775e-106">參數</span><span class="sxs-lookup"><span data-stu-id="0775e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0775e-107">*ppObj* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0775e-107">*ppObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0775e-108">類型： **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0775e-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="0775e-109">在此檔案資料物件中接收列舉物件之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="0775e-109">Address of a pointer to receive the enumeration object in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0775e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0775e-110">Return value</span></span>

<span data-ttu-id="0775e-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0775e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0775e-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0775e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0775e-113">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="0775e-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="0775e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0775e-114">Requirements</span></span>



| <span data-ttu-id="0775e-115">需求</span><span class="sxs-lookup"><span data-stu-id="0775e-115">Requirement</span></span> | <span data-ttu-id="0775e-116">值</span><span class="sxs-lookup"><span data-stu-id="0775e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0775e-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0775e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0775e-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="0775e-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="0775e-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0775e-119">Library</span></span><br/> | <dl> <span data-ttu-id="0775e-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0775e-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0775e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0775e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0775e-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="0775e-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




