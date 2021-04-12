---
description: 抓取此檔案資料物件中的範本識別碼。
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'ID3DXFileData：： GetType 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386489"
---
# <a name="id3dxfiledatagettype-method"></a><span data-ttu-id="69324-103">ID3DXFileData：： GetType 方法</span><span class="sxs-lookup"><span data-stu-id="69324-103">ID3DXFileData::GetType method</span></span>

<span data-ttu-id="69324-104">抓取此檔案資料物件中的範本識別碼。</span><span class="sxs-lookup"><span data-stu-id="69324-104">Retrieves the template ID in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="69324-105">語法</span><span class="sxs-lookup"><span data-stu-id="69324-105">Syntax</span></span>


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a><span data-ttu-id="69324-106">參數</span><span class="sxs-lookup"><span data-stu-id="69324-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69324-107">*pType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69324-107">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69324-108">類型： **Const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="69324-108">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="69324-109">GUID 的指標，代表這個檔案資料物件中的範本。</span><span class="sxs-lookup"><span data-stu-id="69324-109">Pointer to the GUID representing the template in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69324-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="69324-110">Return value</span></span>

<span data-ttu-id="69324-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69324-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69324-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="69324-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="69324-113">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="69324-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="69324-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="69324-114">Requirements</span></span>



| <span data-ttu-id="69324-115">需求</span><span class="sxs-lookup"><span data-stu-id="69324-115">Requirement</span></span> | <span data-ttu-id="69324-116">值</span><span class="sxs-lookup"><span data-stu-id="69324-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69324-117">標頭</span><span class="sxs-lookup"><span data-stu-id="69324-117">Header</span></span><br/>  | <dl> <span data-ttu-id="69324-118"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="69324-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="69324-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="69324-119">Library</span></span><br/> | <dl> <span data-ttu-id="69324-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="69324-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="69324-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69324-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69324-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="69324-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




