---
description: 抓取此檔案資料物件的 GUID。
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'ID3DXFileData：： GetId 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696708"
---
# <a name="id3dxfiledatagetid-method"></a><span data-ttu-id="e459d-103">ID3DXFileData：： GetId 方法</span><span class="sxs-lookup"><span data-stu-id="e459d-103">ID3DXFileData::GetId method</span></span>

<span data-ttu-id="e459d-104">抓取此檔案資料物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e459d-104">Retrieves the GUID of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e459d-105">語法</span><span class="sxs-lookup"><span data-stu-id="e459d-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="e459d-106">參數</span><span class="sxs-lookup"><span data-stu-id="e459d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e459d-107">*pId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e459d-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e459d-108">類型： **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="e459d-108">Type: **LPGUID**</span></span>

<span data-ttu-id="e459d-109">GUID 的指標，用來接收此檔案資料物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e459d-109">Pointer to a GUID to receive the ID of this file data object.</span></span> <span data-ttu-id="e459d-110">如果檔案資料物件沒有識別碼，傳回的參數值將會是 GUID \_ Null。</span><span class="sxs-lookup"><span data-stu-id="e459d-110">If the file data object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e459d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e459d-111">Return value</span></span>

<span data-ttu-id="e459d-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e459d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e459d-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e459d-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e459d-114">如果方法失敗，則會傳回下列值： D3DXFERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="e459d-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e459d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e459d-115">Requirements</span></span>



| <span data-ttu-id="e459d-116">需求</span><span class="sxs-lookup"><span data-stu-id="e459d-116">Requirement</span></span> | <span data-ttu-id="e459d-117">值</span><span class="sxs-lookup"><span data-stu-id="e459d-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e459d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e459d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e459d-119"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="e459d-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e459d-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e459d-120">Library</span></span><br/> | <dl> <span data-ttu-id="e459d-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e459d-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e459d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e459d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e459d-123">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="e459d-123">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




