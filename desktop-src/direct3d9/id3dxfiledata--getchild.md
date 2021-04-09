---
description: 抓取這個檔案資料物件中的子物件。
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: 'ID3DXFileData：： System.windows.media.visualtreehelper.getchild 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 37982ca1e4801b7d70bec503ff9510fc66772651
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946158"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="5441d-103">ID3DXFileData：： System.windows.media.visualtreehelper.getchild 方法</span><span class="sxs-lookup"><span data-stu-id="5441d-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="5441d-104">抓取這個檔案資料物件中的子物件。</span><span class="sxs-lookup"><span data-stu-id="5441d-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5441d-105">語法</span><span class="sxs-lookup"><span data-stu-id="5441d-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="5441d-106">參數</span><span class="sxs-lookup"><span data-stu-id="5441d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5441d-107">*uiChild* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5441d-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5441d-108">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5441d-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5441d-109">要取出之子物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5441d-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5441d-110">*ppChild* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5441d-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5441d-111">類型： **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5441d-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="5441d-112">用來接收子物件介面指標之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="5441d-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5441d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5441d-113">Return value</span></span>

<span data-ttu-id="5441d-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5441d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5441d-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5441d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5441d-116">如果方法失敗，則傳回值可以是下列其中一個值： D3DXFERR \_ BADVALUE，D3DXFERR \_ NOMOREOBJECTS。</span><span class="sxs-lookup"><span data-stu-id="5441d-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="5441d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5441d-117">Requirements</span></span>



| <span data-ttu-id="5441d-118">需求</span><span class="sxs-lookup"><span data-stu-id="5441d-118">Requirement</span></span> | <span data-ttu-id="5441d-119">值</span><span class="sxs-lookup"><span data-stu-id="5441d-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5441d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5441d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5441d-121"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="5441d-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="5441d-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="5441d-122">Library</span></span><br/> | <dl> <span data-ttu-id="5441d-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5441d-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5441d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5441d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5441d-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="5441d-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
