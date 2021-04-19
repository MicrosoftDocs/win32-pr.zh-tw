---
description: GetMediaLength2 方法會抓取此來源物件的媒體長度。 這個方法相當於 IAMTimelineSrc：： GetMediaLength，但會接受 REFTIME 的值。
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'IAMTimelineSrc：： GetMediaLength2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998373"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a><span data-ttu-id="d4e08-104">IAMTimelineSrc：： GetMediaLength2 方法</span><span class="sxs-lookup"><span data-stu-id="d4e08-104">IAMTimelineSrc::GetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="d4e08-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d4e08-105">\[Deprecated.</span></span> <span data-ttu-id="d4e08-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d4e08-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d4e08-107">方法會抓取 `GetMediaLength2` 此來源物件的媒體長度。</span><span class="sxs-lookup"><span data-stu-id="d4e08-107">The `GetMediaLength2` method retrieves the media length of this source object.</span></span> <span data-ttu-id="d4e08-108">這個方法相當於 [**IAMTimelineSrc：： GetMediaLength**](iamtimelinesrc-getmedialength.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="d4e08-108">This method is equivalent to [**IAMTimelineSrc::GetMediaLength**](iamtimelinesrc-getmedialength.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e08-109">語法</span><span class="sxs-lookup"><span data-stu-id="d4e08-109">Syntax</span></span>


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="d4e08-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4e08-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e08-111">*pLength*</span><span class="sxs-lookup"><span data-stu-id="d4e08-111">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="d4e08-112">接收媒體長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d4e08-112">Receives the media length in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4e08-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4e08-113">Return value</span></span>

<span data-ttu-id="d4e08-114">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="d4e08-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="d4e08-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d4e08-115">Return code</span></span>                                                                                     | <span data-ttu-id="d4e08-116">Description</span><span class="sxs-lookup"><span data-stu-id="d4e08-116">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="d4e08-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d4e08-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="d4e08-118">成功。</span><span class="sxs-lookup"><span data-stu-id="d4e08-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="d4e08-119"><dt>**E \_ NOTDETERMINED**</dt></span><span class="sxs-lookup"><span data-stu-id="d4e08-119"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="d4e08-120">未在這個物件上設定媒體時間。</span><span class="sxs-lookup"><span data-stu-id="d4e08-120">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="d4e08-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d4e08-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="d4e08-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="d4e08-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="d4e08-123">備註</span><span class="sxs-lookup"><span data-stu-id="d4e08-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d4e08-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d4e08-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d4e08-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d4e08-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d4e08-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d4e08-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4e08-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4e08-127">Requirements</span></span>



| <span data-ttu-id="d4e08-128">需求</span><span class="sxs-lookup"><span data-stu-id="d4e08-128">Requirement</span></span> | <span data-ttu-id="d4e08-129">值</span><span class="sxs-lookup"><span data-stu-id="d4e08-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e08-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d4e08-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d4e08-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4e08-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d4e08-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4e08-132">Library</span></span><br/> | <dl> <span data-ttu-id="d4e08-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4e08-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4e08-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4e08-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e08-135">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="d4e08-135">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d4e08-136">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="d4e08-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




