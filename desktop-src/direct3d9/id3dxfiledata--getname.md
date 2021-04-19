---
description: 抓取這個檔案資料物件的名稱。
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'ID3DXFileData：： GetName 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992126"
---
# <a name="id3dxfiledatagetname-method"></a><span data-ttu-id="52b88-103">ID3DXFileData：： GetName 方法</span><span class="sxs-lookup"><span data-stu-id="52b88-103">ID3DXFileData::GetName method</span></span>

<span data-ttu-id="52b88-104">抓取這個檔案資料物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="52b88-104">Retrieves the name of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b88-105">語法</span><span class="sxs-lookup"><span data-stu-id="52b88-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="52b88-106">參數</span><span class="sxs-lookup"><span data-stu-id="52b88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52b88-107">*>szname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52b88-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b88-108">類型： **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52b88-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52b88-109">用來接收此檔案資料物件名稱的指標位址。</span><span class="sxs-lookup"><span data-stu-id="52b88-109">Address of a pointer to receive the name of this file data object.</span></span> <span data-ttu-id="52b88-110">如果此參數為 **Null**，則 puiSize 會傳回字串的大小。</span><span class="sxs-lookup"><span data-stu-id="52b88-110">If this parameter is **NULL**, then puiSize will return the size of the string.</span></span> <span data-ttu-id="52b88-111">如果 >szname 指向有效的記憶體，則會將這個檔案資料物件的名稱複製到 >szname 上，直到 puiSize 指定的字元數。</span><span class="sxs-lookup"><span data-stu-id="52b88-111">If szName points to valid memory, the name of this file data object will be copied into szName up to the number of characters given by puiSize.</span></span>

</dd> <dt>

<span data-ttu-id="52b88-112">*puiSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="52b88-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52b88-113">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="52b88-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52b88-114">字串大小的指標，代表這個檔案資料物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="52b88-114">Pointer to the size of the string that represents the name of this file data object.</span></span> <span data-ttu-id="52b88-115">如果 >szname 提供名稱的參考，則這個參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="52b88-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="52b88-116">如果 >szname 為 **Null**，此參數將會傳回字串的大小。</span><span class="sxs-lookup"><span data-stu-id="52b88-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52b88-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="52b88-117">Return value</span></span>

<span data-ttu-id="52b88-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52b88-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52b88-119">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="52b88-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="52b88-120">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="52b88-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="52b88-121">備註</span><span class="sxs-lookup"><span data-stu-id="52b88-121">Remarks</span></span>

<span data-ttu-id="52b88-122">若要讓這個方法成功，>szname 或 *puiSize* 必須為非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="52b88-122">For this method to succeed, either szName or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="52b88-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="52b88-123">Requirements</span></span>



| <span data-ttu-id="52b88-124">需求</span><span class="sxs-lookup"><span data-stu-id="52b88-124">Requirement</span></span> | <span data-ttu-id="52b88-125">值</span><span class="sxs-lookup"><span data-stu-id="52b88-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52b88-126">標頭</span><span class="sxs-lookup"><span data-stu-id="52b88-126">Header</span></span><br/>  | <dl> <span data-ttu-id="52b88-127"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="52b88-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="52b88-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="52b88-128">Library</span></span><br/> | <dl> <span data-ttu-id="52b88-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52b88-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="52b88-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52b88-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b88-131">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="52b88-131">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
