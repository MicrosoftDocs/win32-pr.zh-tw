---
description: SetMediaName 方法會指定此來源物件所表示之原始程式檔的名稱。
ms.assetid: 60307c87-9dce-4e60-b14b-07d2c8604dd8
title: 'IAMTimelineSrc：： SetMediaName 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a770c697f72c8776e9ec7070272ab09fc0dd6af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984852"
---
# <a name="iamtimelinesrcsetmedianame-method"></a><span data-ttu-id="318de-103">IAMTimelineSrc：： SetMediaName 方法</span><span class="sxs-lookup"><span data-stu-id="318de-103">IAMTimelineSrc::SetMediaName method</span></span>

> [!Note]  
> <span data-ttu-id="318de-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="318de-104">\[Deprecated.</span></span> <span data-ttu-id="318de-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="318de-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="318de-106">`SetMediaName`方法會指定此來源物件所表示之原始程式檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="318de-106">The `SetMediaName` method specifies the name of the source file represented by this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="318de-107">語法</span><span class="sxs-lookup"><span data-stu-id="318de-107">Syntax</span></span>


```C++
HRESULT SetMediaName(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="318de-108">參數</span><span class="sxs-lookup"><span data-stu-id="318de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="318de-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="318de-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="318de-110">指定媒體檔名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="318de-110">String that specifies the name of the media file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="318de-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="318de-111">Return value</span></span>

<span data-ttu-id="318de-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="318de-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="318de-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="318de-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="318de-114">備註</span><span class="sxs-lookup"><span data-stu-id="318de-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="318de-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="318de-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="318de-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="318de-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="318de-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="318de-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="318de-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="318de-118">Requirements</span></span>



| <span data-ttu-id="318de-119">需求</span><span class="sxs-lookup"><span data-stu-id="318de-119">Requirement</span></span> | <span data-ttu-id="318de-120">值</span><span class="sxs-lookup"><span data-stu-id="318de-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="318de-121">標頭</span><span class="sxs-lookup"><span data-stu-id="318de-121">Header</span></span><br/>  | <dl> <span data-ttu-id="318de-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="318de-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="318de-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="318de-123">Library</span></span><br/> | <dl> <span data-ttu-id="318de-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="318de-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="318de-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="318de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="318de-126">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="318de-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="318de-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="318de-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




