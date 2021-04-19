---
description: Put \_ Filename 方法會指定要供媒體偵測器使用的原始程式檔名稱。
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: 'IMediaDet：:p ut_Filename 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 542b84d3a1eec79b8408c7642bc08680fdc036ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990206"
---
# <a name="imediadetput_filename-method"></a><span data-ttu-id="43067-103">IMediaDet：:p 的內容 \_ 名稱方法</span><span class="sxs-lookup"><span data-stu-id="43067-103">IMediaDet::put\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="43067-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="43067-104">\[Deprecated.</span></span> <span data-ttu-id="43067-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="43067-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="43067-106">`put_Filename`方法會指定要供媒體偵測器使用的原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="43067-106">The `put_Filename` method specifies the name of the source file for the media detector to use.</span></span>

<span data-ttu-id="43067-107">請勿在相同的 MediaDet 物件上呼叫這個方法兩次。</span><span class="sxs-lookup"><span data-stu-id="43067-107">Do not call this method twice on the same MediaDet object.</span></span> <span data-ttu-id="43067-108">若要使用這個介面搭配多個原始程式檔，請建立 MediaDet 物件的個別實例。</span><span class="sxs-lookup"><span data-stu-id="43067-108">To use this interface with more than one source file, create separate instances of the MediaDet object.</span></span>

## <a name="syntax"></a><span data-ttu-id="43067-109">語法</span><span class="sxs-lookup"><span data-stu-id="43067-109">Syntax</span></span>


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="43067-110">參數</span><span class="sxs-lookup"><span data-stu-id="43067-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43067-111">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43067-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43067-112">來源的檔案名。</span><span class="sxs-lookup"><span data-stu-id="43067-112">File name of the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43067-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="43067-113">Return value</span></span>

<span data-ttu-id="43067-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="43067-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43067-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="43067-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="43067-116">備註</span><span class="sxs-lookup"><span data-stu-id="43067-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43067-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="43067-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="43067-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="43067-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="43067-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="43067-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43067-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="43067-120">Requirements</span></span>



| <span data-ttu-id="43067-121">需求</span><span class="sxs-lookup"><span data-stu-id="43067-121">Requirement</span></span> | <span data-ttu-id="43067-122">值</span><span class="sxs-lookup"><span data-stu-id="43067-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43067-123">標頭</span><span class="sxs-lookup"><span data-stu-id="43067-123">Header</span></span><br/>  | <dl> <span data-ttu-id="43067-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="43067-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="43067-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="43067-125">Library</span></span><br/> | <dl> <span data-ttu-id="43067-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43067-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43067-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43067-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43067-128">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="43067-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="43067-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="43067-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




