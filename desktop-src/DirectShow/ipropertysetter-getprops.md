---
description: GetProps 方法會抓取這個物件上設定的屬性，以及其對應的值。
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'IPropertySetter：： GetProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990114"
---
# <a name="ipropertysettergetprops-method"></a><span data-ttu-id="8df32-103">IPropertySetter：： GetProps 方法</span><span class="sxs-lookup"><span data-stu-id="8df32-103">IPropertySetter::GetProps method</span></span>

> [!Note]  
> <span data-ttu-id="8df32-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="8df32-104">\[Deprecated.</span></span> <span data-ttu-id="8df32-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="8df32-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8df32-106">方法會抓取 `GetProps` 這個物件上設定的屬性，以及其對應的值。</span><span class="sxs-lookup"><span data-stu-id="8df32-106">The `GetProps` method retrieves the properties set on this object, with their corresponding values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df32-107">語法</span><span class="sxs-lookup"><span data-stu-id="8df32-107">Syntax</span></span>


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a><span data-ttu-id="8df32-108">參數</span><span class="sxs-lookup"><span data-stu-id="8df32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df32-109">*pcParams* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8df32-109">*pcParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df32-110">接收 *paParam* 中傳回的結構數目。</span><span class="sxs-lookup"><span data-stu-id="8df32-110">Receives the number of structures returned in *paParam*.</span></span>

</dd> <dt>

<span data-ttu-id="8df32-111">*paParam* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8df32-111">*paParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df32-112">[**DEXTER \_ PARAM**](dexter-param.md)結構陣列的指標位址。</span><span class="sxs-lookup"><span data-stu-id="8df32-112">Address of a pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="8df32-113">*paValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8df32-113">*paValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df32-114">[**DEXTER \_ 值**](dexter-value.md)結構陣列的指標位址。</span><span class="sxs-lookup"><span data-stu-id="8df32-114">Address of a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df32-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8df32-115">Return value</span></span>

<span data-ttu-id="8df32-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8df32-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8df32-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8df32-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df32-118">備註</span><span class="sxs-lookup"><span data-stu-id="8df32-118">Remarks</span></span>

<span data-ttu-id="8df32-119">針對 *paParam* 中傳回的每個屬性， **值成員表示** 與屬性相關聯的 [**DEXTER \_ 值**](dexter-value.md) 結構數目。</span><span class="sxs-lookup"><span data-stu-id="8df32-119">For each property returned in *paParam*, the **nValues** member indicates the number of [**DEXTER\_VALUE**](dexter-value.md) structures associated with the property.</span></span> <span data-ttu-id="8df32-120">針對每個屬性，會以遞增的時間順序傳回配對。</span><span class="sxs-lookup"><span data-stu-id="8df32-120">The pairs are returned in ascending time order for each property.</span></span>

<span data-ttu-id="8df32-121">當您完成使用傳回的結構時，請呼叫 [**IPropertySetter：： FreeProps**](ipropertysetter-freeprops.md) 來釋出這個方法所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="8df32-121">When you are finished using the returned structures, call [**IPropertySetter::FreeProps**](ipropertysetter-freeprops.md) to free the resources allocated by this method.</span></span>

> [!Note]  
> <span data-ttu-id="8df32-122">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="8df32-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8df32-123">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="8df32-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8df32-124">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="8df32-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8df32-125">範例</span><span class="sxs-lookup"><span data-stu-id="8df32-125">Examples</span></span>

<span data-ttu-id="8df32-126">下列程式碼範例示範如何逐一查看屬性 setter 實例上的所有值：</span><span class="sxs-lookup"><span data-stu-id="8df32-126">The following code example shows how to iterate through all the values on an instance of the property setter:</span></span>


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a><span data-ttu-id="8df32-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8df32-127">Requirements</span></span>



| <span data-ttu-id="8df32-128">需求</span><span class="sxs-lookup"><span data-stu-id="8df32-128">Requirement</span></span> | <span data-ttu-id="8df32-129">值</span><span class="sxs-lookup"><span data-stu-id="8df32-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8df32-130">標頭</span><span class="sxs-lookup"><span data-stu-id="8df32-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8df32-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="8df32-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8df32-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="8df32-132">Library</span></span><br/> | <dl> <span data-ttu-id="8df32-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8df32-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8df32-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8df32-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df32-135">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="8df32-135">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="8df32-136">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="8df32-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




