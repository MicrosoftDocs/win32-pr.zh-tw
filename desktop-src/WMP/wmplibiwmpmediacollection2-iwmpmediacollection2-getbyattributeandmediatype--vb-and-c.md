---
title: IWMPMediaCollection2 getByAttributeAndMediaType 方法
description: GetByAttributeAndMediaType 方法會傳回 IWMPPlaylist 介面，以提供具有指定屬性和媒體類型的媒體專案存取權。
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- getByAttributeAndMediaType 方法 Windows Media Player
- getByAttributeAndMediaType 方法 Windows Media Player，IWMPMediaCollection2 介面
- IWMPMediaCollection2 介面 Windows Media Player，getByAttributeAndMediaType 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978513"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a><span data-ttu-id="5045f-106">IWMPMediaCollection2：： getByAttributeAndMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="5045f-106">IWMPMediaCollection2::getByAttributeAndMediaType method</span></span>

<span data-ttu-id="5045f-107">`getByAttributeAndMediaType`方法會傳回 **IWMPPlaylist** 介面，以提供具有指定屬性和媒體類型之媒體專案的存取權。</span><span class="sxs-lookup"><span data-stu-id="5045f-107">The `getByAttributeAndMediaType` method returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5045f-108">語法</span><span class="sxs-lookup"><span data-stu-id="5045f-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a><span data-ttu-id="5045f-109">參數</span><span class="sxs-lookup"><span data-stu-id="5045f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5045f-110">*bstrAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5045f-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5045f-111">指定之屬性的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="5045f-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="5045f-112">*bstrValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5045f-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5045f-113">*BstrAttribute* 中所指定之屬性的指定值的 **system.string。**</span><span class="sxs-lookup"><span data-stu-id="5045f-113">The **System.String** that is the specified value for the attribute that is specified in *bstrAttribute*.</span></span>

</dd> <dt>

<span data-ttu-id="5045f-114">*bstrMediaType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5045f-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5045f-115">指定媒體類型的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="5045f-115">The **System.String** that is the specified media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5045f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5045f-116">Return value</span></span>

<span data-ttu-id="5045f-117">已抓取播放清單的 **WMPLib IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="5045f-117">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="5045f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5045f-118">Requirements</span></span>



| <span data-ttu-id="5045f-119">需求</span><span class="sxs-lookup"><span data-stu-id="5045f-119">Requirement</span></span> | <span data-ttu-id="5045f-120">值</span><span class="sxs-lookup"><span data-stu-id="5045f-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5045f-121">版本</span><span class="sxs-lookup"><span data-stu-id="5045f-121">Version</span></span><br/>   | <span data-ttu-id="5045f-122">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="5045f-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="5045f-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="5045f-123">Namespace</span></span><br/> | <span data-ttu-id="5045f-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5045f-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5045f-125">組件</span><span class="sxs-lookup"><span data-stu-id="5045f-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5045f-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="5045f-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5045f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5045f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5045f-128">**IWMPMediaCollection2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5045f-128">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5045f-129">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="5045f-129">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





