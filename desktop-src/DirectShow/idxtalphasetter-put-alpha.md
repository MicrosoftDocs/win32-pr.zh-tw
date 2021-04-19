---
description: Put \_ Alpha 方法會指定整個影像的 Alpha 值。
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'IDxtAlphaSetter：:p ut_Alpha 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994359"
---
# <a name="idxtalphasetterput_alpha-method"></a><span data-ttu-id="5187d-103">IDxtAlphaSetter：:p 的 ui \_ Alpha 方法</span><span class="sxs-lookup"><span data-stu-id="5187d-103">IDxtAlphaSetter::put\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="5187d-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5187d-104">\[Deprecated.</span></span> <span data-ttu-id="5187d-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5187d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5187d-106">`put_Alpha`方法會指定整個影像的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="5187d-106">The `put_Alpha` method specifies the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="5187d-107">語法</span><span class="sxs-lookup"><span data-stu-id="5187d-107">Syntax</span></span>


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="5187d-108">參數</span><span class="sxs-lookup"><span data-stu-id="5187d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5187d-109">*Alpha* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5187d-109">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5187d-110">Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="5187d-110">The alpha value.</span></span> <span data-ttu-id="5187d-111">此值將會套用至整個目標映射。</span><span class="sxs-lookup"><span data-stu-id="5187d-111">This value will be applied to the entire target image.</span></span> <span data-ttu-id="5187d-112">若要停用此屬性，請設定負數值。</span><span class="sxs-lookup"><span data-stu-id="5187d-112">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5187d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5187d-113">Return value</span></span>

<span data-ttu-id="5187d-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5187d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5187d-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5187d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5187d-116">備註</span><span class="sxs-lookup"><span data-stu-id="5187d-116">Remarks</span></span>

<span data-ttu-id="5187d-117">如果您將這個屬性設定為非負數值，您也必須藉由呼叫 **put \_ AlphaRamp** 與負數值，來停用 Alpha 曲線的屬性。</span><span class="sxs-lookup"><span data-stu-id="5187d-117">If you set this property to a non-negative value, you must also disable the alpha ramp property, by calling **put\_AlphaRamp** with a negative value.</span></span> <span data-ttu-id="5187d-118">否則效果將不會正確呈現。</span><span class="sxs-lookup"><span data-stu-id="5187d-118">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="5187d-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5187d-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5187d-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5187d-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5187d-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5187d-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5187d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5187d-122">Requirements</span></span>



| <span data-ttu-id="5187d-123">需求</span><span class="sxs-lookup"><span data-stu-id="5187d-123">Requirement</span></span> | <span data-ttu-id="5187d-124">值</span><span class="sxs-lookup"><span data-stu-id="5187d-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5187d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5187d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5187d-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5187d-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5187d-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="5187d-127">Library</span></span><br/> | <dl> <span data-ttu-id="5187d-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5187d-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5187d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5187d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5187d-130">**IDxtAlphaSetter 介面**</span><span class="sxs-lookup"><span data-stu-id="5187d-130">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="5187d-131">**IDxtAlphaSetter：:p 的 \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="5187d-131">**IDxtAlphaSetter::put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




