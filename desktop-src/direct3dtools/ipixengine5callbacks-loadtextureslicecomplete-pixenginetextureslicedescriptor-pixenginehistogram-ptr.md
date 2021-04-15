---
description: 當材質配量載入已完成時，用來通知主機的回呼函式。
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureSliceComplete\_PixEngineTextureSliceDescriptor\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks：： LoadTextureSliceComplete 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CEEAB77F-0856-4DEC-991A-7CEB921C84BB
api_name:
- IPixEngine5Callbacks.LoadTextureSliceComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 674288841ea08ad38c519e88abac4c64a1f1ca7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467860"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptrspanipixengine5callbacksloadtextureslicecomplete-method"></a><span data-ttu-id="31e0b-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks：： LoadTextureSliceComplete 方法</span><span class="sxs-lookup"><span data-stu-id="31e0b-103"><span id="vspixengine.ipixengine5callbacks_loadtextureslicecomplete_pixenginetextureslicedescriptor_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureSliceComplete method</span></span>

<span data-ttu-id="31e0b-104">當材質配量載入已完成時，用來通知主機的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="31e0b-104">A callback function used to notify the host when a texture slice load has been completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="31e0b-105">Syntax</span></span>


```C++
HRESULT LoadTextureSliceComplete(
   PixEngineTextureSliceDescriptor sliceDesc,
   PixEngineHistogram*             histogram
);
```

## <a name="parameters"></a><span data-ttu-id="31e0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="31e0b-106">Parameters</span></span>

<span data-ttu-id="31e0b-107">*sliceDesc* </span><span class="sxs-lookup"><span data-stu-id="31e0b-107">*sliceDesc* </span></span>  
<span data-ttu-id="31e0b-108">已載入之配量的描述項。</span><span class="sxs-lookup"><span data-stu-id="31e0b-108">A descriptor of the loaded slice.</span></span>

<span data-ttu-id="31e0b-109">*長條圖* </span><span class="sxs-lookup"><span data-stu-id="31e0b-109">*histogram* </span></span>  
<span data-ttu-id="31e0b-110">已載入之配量的長條圖資料位址。</span><span class="sxs-lookup"><span data-stu-id="31e0b-110">The address of histogram data for the loaded slice.</span></span>

## <a name="return-value"></a><span data-ttu-id="31e0b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="31e0b-111">Return value</span></span>

<span data-ttu-id="31e0b-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="31e0b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31e0b-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="31e0b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e0b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="31e0b-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="31e0b-115">標頭</span><span class="sxs-lookup"><span data-stu-id="31e0b-115">Header</span></span></p></td><td><span data-ttu-id="31e0b-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="31e0b-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="31e0b-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="31e0b-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="31e0b-118">**IPixEngine5Callbacks**</span><span class="sxs-lookup"><span data-stu-id="31e0b-118">**IPixEngine5Callbacks**</span></span>](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
