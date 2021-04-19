---
description: 指定非色彩樣式是否具有粗體樣式。
ms.assetid: fd34af7f-8847-43aa-9e69-264a08eba98b
title: FBoldIMEStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FBoldIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: f54e62feae710dd51cae688d380ccf7da1eda4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984814"
---
# <a name="fboldimestyle-function"></a><span data-ttu-id="7c0c3-103">FBoldIMEStyle 函式</span><span class="sxs-lookup"><span data-stu-id="7c0c3-103">FBoldIMEStyle function</span></span>

<span data-ttu-id="7c0c3-104">指定非色彩樣式是否具有粗體樣式。</span><span class="sxs-lookup"><span data-stu-id="7c0c3-104">Specifies whether a non-color style has the bold style.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c0c3-105">Syntax</span></span>


```C++
BOOL FBoldIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="7c0c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c0c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c0c3-107">*pimestyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c0c3-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0c3-108">從 [**PIMEStyleFromAttr**](pimestylefromattr.md)函數傳回的 **IMESTYLE** 結構。</span><span class="sxs-lookup"><span data-stu-id="7c0c3-108">An **IMESTYLE** structure returned from the [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c0c3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c0c3-109">Return value</span></span>

<span data-ttu-id="7c0c3-110">如果樣式具有粗體樣式，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="7c0c3-110">**TRUE** if the style has the bold style.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0c3-111">備註</span><span class="sxs-lookup"><span data-stu-id="7c0c3-111">Remarks</span></span>

<span data-ttu-id="7c0c3-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="7c0c3-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0c3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c0c3-113">Requirements</span></span>



| <span data-ttu-id="7c0c3-114">需求</span><span class="sxs-lookup"><span data-stu-id="7c0c3-114">Requirement</span></span> | <span data-ttu-id="7c0c3-115">值</span><span class="sxs-lookup"><span data-stu-id="7c0c3-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0c3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7c0c3-116">DLL</span></span><br/> | <dl> <span data-ttu-id="7c0c3-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c0c3-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c0c3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c0c3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0c3-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="7c0c3-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
