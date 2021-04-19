---
description: AddProp 方法會將屬性加入至屬性 setter，以及定義時間範圍內屬性值的時間值配對陣列。
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'IPropertySetter：： AddProp 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977437"
---
# <a name="ipropertysetteraddprop-method"></a><span data-ttu-id="b4e50-103">IPropertySetter：： AddProp 方法</span><span class="sxs-lookup"><span data-stu-id="b4e50-103">IPropertySetter::AddProp method</span></span>

> [!Note]  
> <span data-ttu-id="b4e50-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b4e50-104">\[Deprecated.</span></span> <span data-ttu-id="b4e50-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b4e50-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b4e50-106">`AddProp`方法會將屬性加入至屬性 setter，以及定義時間範圍內屬性值的時間值配對陣列。</span><span class="sxs-lookup"><span data-stu-id="b4e50-106">The `AddProp` method adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e50-107">語法</span><span class="sxs-lookup"><span data-stu-id="b4e50-107">Syntax</span></span>


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="b4e50-108">參數</span><span class="sxs-lookup"><span data-stu-id="b4e50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4e50-109">*Param* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4e50-109">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e50-110">[**DEXTER \_**](dexter-param.md)指定屬性的 PARAM 結構。</span><span class="sxs-lookup"><span data-stu-id="b4e50-110">[**DEXTER\_PARAM**](dexter-param.md) structure that specifies the property.</span></span> <span data-ttu-id="b4e50-111">結構 **的值成員必須** 等於 *paValue* 參數中指定的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="b4e50-111">The **nValues** member of the structure must equal the size of the array given in the *paValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b4e50-112">*paValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4e50-112">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4e50-113">[**DEXTER \_ 值**](dexter-value.md)結構的陣列的指標，其中包含時間值的配對。</span><span class="sxs-lookup"><span data-stu-id="b4e50-113">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures that contain time-value pairs.</span></span> <span data-ttu-id="b4e50-114">陣列必須是遞增的時間順序。</span><span class="sxs-lookup"><span data-stu-id="b4e50-114">The array must be in ascending time order.</span></span> <span data-ttu-id="b4e50-115">時間相對於效果或轉換的開始時間。</span><span class="sxs-lookup"><span data-stu-id="b4e50-115">The times are relative to the starting time of the effect or transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4e50-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4e50-116">Return value</span></span>

<span data-ttu-id="b4e50-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b4e50-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4e50-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b4e50-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4e50-119">備註</span><span class="sxs-lookup"><span data-stu-id="b4e50-119">Remarks</span></span>

<span data-ttu-id="b4e50-120">第一個 [**DEXTER \_ 值**](dexter-value.md) 結構必須指定零的參考時間和插補旗標 (**dwInterp**) 的 **DEXTERF \_ 跳躍**，否則方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b4e50-120">The first [**DEXTER\_VALUE**](dexter-value.md) structure must specify a reference time of zero and an interpolation flag (**dwInterp**) of **DEXTERF\_JUMP**, or the method returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="b4e50-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b4e50-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b4e50-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b4e50-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b4e50-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b4e50-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b4e50-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4e50-124">Requirements</span></span>



| <span data-ttu-id="b4e50-125">需求</span><span class="sxs-lookup"><span data-stu-id="b4e50-125">Requirement</span></span> | <span data-ttu-id="b4e50-126">值</span><span class="sxs-lookup"><span data-stu-id="b4e50-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e50-127">標頭</span><span class="sxs-lookup"><span data-stu-id="b4e50-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b4e50-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4e50-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b4e50-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="b4e50-129">Library</span></span><br/> | <dl> <span data-ttu-id="b4e50-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4e50-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4e50-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4e50-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e50-132">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="b4e50-132">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="b4e50-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="b4e50-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




