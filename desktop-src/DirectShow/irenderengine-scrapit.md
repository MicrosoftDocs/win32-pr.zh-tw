---
description: ScrapIt 方法會捨棄轉譯引擎的篩選圖形以及所有相關聯的物件。
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: 'IRenderEngine：： ScrapIt 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f9febbe20cfd5ab9a6577a6e00989c7d6fc4145
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979575"
---
# <a name="irenderenginescrapit-method"></a><span data-ttu-id="73616-103">IRenderEngine：： ScrapIt 方法</span><span class="sxs-lookup"><span data-stu-id="73616-103">IRenderEngine::ScrapIt method</span></span>

> [!Note]  
> <span data-ttu-id="73616-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="73616-104">\[Deprecated.</span></span> <span data-ttu-id="73616-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="73616-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="73616-106">`ScrapIt`方法會捨棄轉譯引擎的篩選圖形以及所有相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="73616-106">The `ScrapIt` method discards the render engine's filter graph and all associated objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="73616-107">語法</span><span class="sxs-lookup"><span data-stu-id="73616-107">Syntax</span></span>


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a><span data-ttu-id="73616-108">參數</span><span class="sxs-lookup"><span data-stu-id="73616-108">Parameters</span></span>

<span data-ttu-id="73616-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="73616-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73616-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="73616-110">Return value</span></span>

<span data-ttu-id="73616-111">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="73616-111">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="73616-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="73616-112">Return code</span></span>                                                                                            | <span data-ttu-id="73616-113">Description</span><span class="sxs-lookup"><span data-stu-id="73616-113">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="73616-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="73616-114"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="73616-115">成功。</span><span class="sxs-lookup"><span data-stu-id="73616-115">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="73616-116"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="73616-116"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="73616-117">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="73616-117">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73616-118">備註</span><span class="sxs-lookup"><span data-stu-id="73616-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73616-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="73616-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="73616-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="73616-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="73616-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="73616-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73616-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="73616-122">Requirements</span></span>



| <span data-ttu-id="73616-123">需求</span><span class="sxs-lookup"><span data-stu-id="73616-123">Requirement</span></span> | <span data-ttu-id="73616-124">值</span><span class="sxs-lookup"><span data-stu-id="73616-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73616-125">標頭</span><span class="sxs-lookup"><span data-stu-id="73616-125">Header</span></span><br/>  | <dl> <span data-ttu-id="73616-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="73616-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="73616-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="73616-127">Library</span></span><br/> | <dl> <span data-ttu-id="73616-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="73616-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73616-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73616-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73616-130">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="73616-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="73616-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="73616-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




