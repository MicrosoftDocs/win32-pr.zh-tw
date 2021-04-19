---
description: Get \_ MaskName 方法會抓取要當做抹除遮罩使用的 JPEG 檔案名。
ms.assetid: b21913c0-4269-41f9-b2f0-ae69be9c0871
title: 'IDxtJpeg：： get_MaskName 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a00c8104ee19cac33a00ff9062006338a19e283b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977641"
---
# <a name="idxtjpegget_maskname-method"></a><span data-ttu-id="1d63b-103">IDxtJpeg：： get \_ MaskName 方法</span><span class="sxs-lookup"><span data-stu-id="1d63b-103">IDxtJpeg::get\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="1d63b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1d63b-104">\[Deprecated.</span></span> <span data-ttu-id="1d63b-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1d63b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1d63b-106">`get_MaskName`方法會抓取要當做抹除遮罩使用之 JPEG 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d63b-106">The `get_MaskName` method retrieves the name of a JPEG file to be used as the wipe mask.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d63b-107">語法</span><span class="sxs-lookup"><span data-stu-id="1d63b-107">Syntax</span></span>


```C++
HRESULT get_MaskName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1d63b-108">參數</span><span class="sxs-lookup"><span data-stu-id="1d63b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d63b-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="1d63b-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-110">接收檔案名。</span><span class="sxs-lookup"><span data-stu-id="1d63b-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d63b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d63b-111">Return value</span></span>

<span data-ttu-id="1d63b-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1d63b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1d63b-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1d63b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d63b-114">備註</span><span class="sxs-lookup"><span data-stu-id="1d63b-114">Remarks</span></span>

<span data-ttu-id="1d63b-115">如果抹除轉換使用其支援的其中一個內建的 SMPTE 抹除，則此屬性的值為空字串。</span><span class="sxs-lookup"><span data-stu-id="1d63b-115">If the wipe transition is using one of the built-in SMPTE wipes that it supports, the value of this property is an empty string.</span></span>

<span data-ttu-id="1d63b-116">呼叫端必須使用 **SysFreeString** 函數釋放傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="1d63b-116">The caller must release the returned string, using the **SysFreeString** function.</span></span>

> [!Note]  
> <span data-ttu-id="1d63b-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="1d63b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1d63b-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1d63b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1d63b-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="1d63b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d63b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d63b-120">Requirements</span></span>



| <span data-ttu-id="1d63b-121">需求</span><span class="sxs-lookup"><span data-stu-id="1d63b-121">Requirement</span></span> | <span data-ttu-id="1d63b-122">值</span><span class="sxs-lookup"><span data-stu-id="1d63b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d63b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1d63b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1d63b-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d63b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1d63b-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d63b-125">Library</span></span><br/> | <dl> <span data-ttu-id="1d63b-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d63b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d63b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d63b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d63b-128">**IDxtJpeg 介面**</span><span class="sxs-lookup"><span data-stu-id="1d63b-128">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="1d63b-129">**IDxtJpeg：： get \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="1d63b-129">**IDxtJpeg::get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)
</dt> </dl>

 

 




