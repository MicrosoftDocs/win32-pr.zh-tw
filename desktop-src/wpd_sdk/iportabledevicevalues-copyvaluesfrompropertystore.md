---
description: CopyValuesFromPropertyStore 方法會將 IPropertyStore 的內容複寫到集合中。
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'IPortableDeviceValues：： CopyValuesFromPropertyStore 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995389"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a><span data-ttu-id="157c2-103">IPortableDeviceValues：： CopyValuesFromPropertyStore 方法</span><span class="sxs-lookup"><span data-stu-id="157c2-103">IPortableDeviceValues::CopyValuesFromPropertyStore method</span></span>

<span data-ttu-id="157c2-104">**CopyValuesFromPropertyStore** 方法會將 **IPropertyStore** 的內容複寫到集合中。</span><span class="sxs-lookup"><span data-stu-id="157c2-104">The **CopyValuesFromPropertyStore** method copies the contents of an **IPropertyStore** into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="157c2-105">語法</span><span class="sxs-lookup"><span data-stu-id="157c2-105">Syntax</span></span>


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="157c2-106">參數</span><span class="sxs-lookup"><span data-stu-id="157c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="157c2-107">*pStore* \[在\]</span><span class="sxs-lookup"><span data-stu-id="157c2-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="157c2-108">要複製到集合中之 **IPropertyStore** 的指標。</span><span class="sxs-lookup"><span data-stu-id="157c2-108">Pointer to an **IPropertyStore** to copy into the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="157c2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="157c2-109">Return value</span></span>

<span data-ttu-id="157c2-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="157c2-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="157c2-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="157c2-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="157c2-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="157c2-112">Return code</span></span>                                                                          | <span data-ttu-id="157c2-113">Description</span><span class="sxs-lookup"><span data-stu-id="157c2-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="157c2-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="157c2-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="157c2-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="157c2-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="157c2-116">備註</span><span class="sxs-lookup"><span data-stu-id="157c2-116">Remarks</span></span>

<span data-ttu-id="157c2-117">這個方法會自動將所有 **VT \_ BSTR** 值轉換成 **VT \_ LPWSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="157c2-117">This method automatically converts all **VT\_BSTR** values to **VT\_LPWSTR** values.</span></span>

<span data-ttu-id="157c2-118">許多與您的應用程式通訊的外部應用程式或元件（例如某些 shell 應用程式）都會使用 **IPropertyStore** 介面。</span><span class="sxs-lookup"><span data-stu-id="157c2-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="157c2-119">這種方法可讓您快速輕鬆地與這些程式交換資料。</span><span class="sxs-lookup"><span data-stu-id="157c2-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="157c2-120">Windows Vista 和更新版本的 Windows 中支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="157c2-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="157c2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="157c2-121">Requirements</span></span>



| <span data-ttu-id="157c2-122">需求</span><span class="sxs-lookup"><span data-stu-id="157c2-122">Requirement</span></span> | <span data-ttu-id="157c2-123">值</span><span class="sxs-lookup"><span data-stu-id="157c2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="157c2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="157c2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="157c2-125"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="157c2-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="157c2-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="157c2-126">Library</span></span><br/> | <dl> <span data-ttu-id="157c2-127"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="157c2-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="157c2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="157c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="157c2-129">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="157c2-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="157c2-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="157c2-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span></span>](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




