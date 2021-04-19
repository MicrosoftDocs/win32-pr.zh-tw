---
description: SetErrorValue 方法會新增 HRESULT 值 (type VT \_ ERROR) 或覆寫現有的值。
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'IPortableDeviceValues：： SetErrorValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996212"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a><span data-ttu-id="13e9e-103">IPortableDeviceValues：： SetErrorValue 方法</span><span class="sxs-lookup"><span data-stu-id="13e9e-103">IPortableDeviceValues::SetErrorValue method</span></span>

<span data-ttu-id="13e9e-104">**SetErrorValue** 方法會新增 **HRESULT** 值 (type VT \_ ERROR) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="13e9e-104">The **SetErrorValue** method adds a new **HRESULT** value (type VT\_ERROR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="13e9e-105">Syntax</span></span>


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
);
```



## <a name="parameters"></a><span data-ttu-id="13e9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="13e9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e9e-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13e9e-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e9e-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="13e9e-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="13e9e-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13e9e-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e9e-110">包含新值的 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="13e9e-110">An **HRESULT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e9e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="13e9e-111">Return value</span></span>

<span data-ttu-id="13e9e-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="13e9e-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="13e9e-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="13e9e-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="13e9e-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="13e9e-114">Return code</span></span>                                                                          | <span data-ttu-id="13e9e-115">Description</span><span class="sxs-lookup"><span data-stu-id="13e9e-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="13e9e-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="13e9e-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="13e9e-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="13e9e-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13e9e-118">備註</span><span class="sxs-lookup"><span data-stu-id="13e9e-118">Remarks</span></span>

<span data-ttu-id="13e9e-119">如果現有的值具有 *金鑰* 參數指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="13e9e-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e9e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="13e9e-120">Requirements</span></span>



| <span data-ttu-id="13e9e-121">需求</span><span class="sxs-lookup"><span data-stu-id="13e9e-121">Requirement</span></span> | <span data-ttu-id="13e9e-122">值</span><span class="sxs-lookup"><span data-stu-id="13e9e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e9e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="13e9e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="13e9e-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="13e9e-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="13e9e-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="13e9e-125">Library</span></span><br/> | <dl> <span data-ttu-id="13e9e-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13e9e-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e9e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13e9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e9e-128">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="13e9e-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="13e9e-129">**IPortableDeviceValues::GetErrorValue**</span><span class="sxs-lookup"><span data-stu-id="13e9e-129">**IPortableDeviceValues::GetErrorValue**</span></span>](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




