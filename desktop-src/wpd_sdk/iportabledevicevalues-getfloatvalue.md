---
description: GetFloatValue 方法會抓取 (type VT \_ R4) 由索引鍵指定的浮點值。
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'IPortableDeviceValues：： GetFloatValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984051"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a><span data-ttu-id="8101e-103">IPortableDeviceValues：： GetFloatValue 方法</span><span class="sxs-lookup"><span data-stu-id="8101e-103">IPortableDeviceValues::GetFloatValue method</span></span>

<span data-ttu-id="8101e-104">**GetFloatValue** 方法會抓取 ( type VT \_ R4) 由索引鍵指定的浮點值。</span><span class="sxs-lookup"><span data-stu-id="8101e-104">The **GetFloatValue** method retrieves a **FLOAT** value (type VT\_R4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8101e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8101e-105">Syntax</span></span>


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="8101e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8101e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8101e-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8101e-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8101e-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="8101e-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="8101e-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8101e-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8101e-110">已抓取 **浮點** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="8101e-110">Pointer to the retrieved **FLOAT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8101e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8101e-111">Return value</span></span>

<span data-ttu-id="8101e-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="8101e-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8101e-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="8101e-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8101e-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8101e-114">Return code</span></span>                                                                                             | <span data-ttu-id="8101e-115">Description</span><span class="sxs-lookup"><span data-stu-id="8101e-115">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="8101e-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8101e-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="8101e-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="8101e-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8101e-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="8101e-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>    | <span data-ttu-id="8101e-119">索引 *鍵* 所指定的屬性不是 **FLOAT** 類型。</span><span class="sxs-lookup"><span data-stu-id="8101e-119">The property specified by *key* is not a **FLOAT** type.</span></span><br/>  |
| <dl> <span data-ttu-id="8101e-120"><dt>**E \_ \_ \_ 不支援的識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="8101e-120"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="8101e-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="8101e-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8101e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8101e-122">Requirements</span></span>



| <span data-ttu-id="8101e-123">需求</span><span class="sxs-lookup"><span data-stu-id="8101e-123">Requirement</span></span> | <span data-ttu-id="8101e-124">值</span><span class="sxs-lookup"><span data-stu-id="8101e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8101e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8101e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8101e-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="8101e-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8101e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="8101e-127">Library</span></span><br/> | <dl> <span data-ttu-id="8101e-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8101e-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8101e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8101e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8101e-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="8101e-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="8101e-131">**IPortableDeviceValues::SetFloatValue**</span><span class="sxs-lookup"><span data-stu-id="8101e-131">**IPortableDeviceValues::SetFloatValue**</span></span>](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




