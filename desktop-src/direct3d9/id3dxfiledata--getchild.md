---
description: ID3DXFileData：： System.windows.media.visualtreehelper.getchild 方法-抓取這個檔案資料物件中的子物件。
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
ms.openlocfilehash: 7fe6c0393e5cfb9ed8aeaf5808d33175e7f9bfe5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090376"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="b0511-103">ID3DXFileData：： System.windows.media.visualtreehelper.getchild 方法</span><span class="sxs-lookup"><span data-stu-id="b0511-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="b0511-104">抓取這個檔案資料物件中的子物件。</span><span class="sxs-lookup"><span data-stu-id="b0511-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0511-105">語法</span><span class="sxs-lookup"><span data-stu-id="b0511-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="b0511-106">參數</span><span class="sxs-lookup"><span data-stu-id="b0511-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0511-107">*uiChild* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b0511-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0511-108">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0511-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0511-109">要取出之子物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0511-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b0511-110">*ppChild* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b0511-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0511-111">類型： **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b0511-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="b0511-112">用來接收子物件介面指標之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="b0511-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0511-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b0511-113">Return value</span></span>

<span data-ttu-id="b0511-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0511-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0511-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b0511-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b0511-116">如果方法失敗，則傳回值可以是下列其中一個值： D3DXFERR \_ BADVALUE，D3DXFERR \_ NOMOREOBJECTS。</span><span class="sxs-lookup"><span data-stu-id="b0511-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0511-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0511-117">Requirements</span></span>



| <span data-ttu-id="b0511-118">需求</span><span class="sxs-lookup"><span data-stu-id="b0511-118">Requirement</span></span> | <span data-ttu-id="b0511-119">值</span><span class="sxs-lookup"><span data-stu-id="b0511-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0511-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b0511-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b0511-121"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="b0511-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="b0511-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="b0511-122">Library</span></span><br/> | <dl> <span data-ttu-id="b0511-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0511-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b0511-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0511-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0511-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="b0511-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
