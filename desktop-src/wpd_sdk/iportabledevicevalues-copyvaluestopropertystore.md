---
description: CopyValuesToPropertyStore 方法會將集合中的所有值複製到 IPropertyStore 介面中。
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'IPortableDeviceValues：： CopyValuesToPropertyStore 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978428"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a><span data-ttu-id="308a1-103">IPortableDeviceValues：： CopyValuesToPropertyStore 方法</span><span class="sxs-lookup"><span data-stu-id="308a1-103">IPortableDeviceValues::CopyValuesToPropertyStore method</span></span>

<span data-ttu-id="308a1-104">**CopyValuesToPropertyStore** 方法會將集合中的所有值複製到 **IPropertyStore** 介面中。</span><span class="sxs-lookup"><span data-stu-id="308a1-104">The **CopyValuesToPropertyStore** method copies all the values from a collection into an **IPropertyStore** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="308a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="308a1-105">Syntax</span></span>


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="308a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="308a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="308a1-107">*pStore* \[在\]</span><span class="sxs-lookup"><span data-stu-id="308a1-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="308a1-108">存放區物件的指標。</span><span class="sxs-lookup"><span data-stu-id="308a1-108">Pointer to a store object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="308a1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="308a1-109">Return value</span></span>

<span data-ttu-id="308a1-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="308a1-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="308a1-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="308a1-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="308a1-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="308a1-112">Return code</span></span>                                                                          | <span data-ttu-id="308a1-113">Description</span><span class="sxs-lookup"><span data-stu-id="308a1-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="308a1-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="308a1-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="308a1-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="308a1-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="308a1-116">備註</span><span class="sxs-lookup"><span data-stu-id="308a1-116">Remarks</span></span>

<span data-ttu-id="308a1-117">這個方法不會將 VT LPWSTR 的值轉換 \_ 成 vt \_ BSTR。</span><span class="sxs-lookup"><span data-stu-id="308a1-117">This method does not convert values of VT\_LPWSTR into VT\_BSTR.</span></span> <span data-ttu-id="308a1-118">許多與您的應用程式通訊的外部應用程式或元件（例如某些 shell 應用程式）都會使用 **IPropertyStore** 介面。</span><span class="sxs-lookup"><span data-stu-id="308a1-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="308a1-119">這種方法可讓您快速輕鬆地與這些程式交換資料。</span><span class="sxs-lookup"><span data-stu-id="308a1-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="308a1-120">Windows Vista 和更新版本的 Windows 中支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="308a1-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="308a1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="308a1-121">Requirements</span></span>



| <span data-ttu-id="308a1-122">需求</span><span class="sxs-lookup"><span data-stu-id="308a1-122">Requirement</span></span> | <span data-ttu-id="308a1-123">值</span><span class="sxs-lookup"><span data-stu-id="308a1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="308a1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="308a1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="308a1-125"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="308a1-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="308a1-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="308a1-126">Library</span></span><br/> | <dl> <span data-ttu-id="308a1-127"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="308a1-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="308a1-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="308a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="308a1-129">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="308a1-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="308a1-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="308a1-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span></span>](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




