---
description: 略過列舉序列中指定的裝置數目。
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'IEnumPortableDeviceConnectors：： Skip 方法 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027106"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a><span data-ttu-id="bba20-103">IEnumPortableDeviceConnectors：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="bba20-103">IEnumPortableDeviceConnectors::Skip method</span></span>

<span data-ttu-id="bba20-104">**Skip** 方法會在列舉順序中略過指定數目的裝置。</span><span class="sxs-lookup"><span data-stu-id="bba20-104">The **Skip** method skips the specified number of devices in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba20-105">語法</span><span class="sxs-lookup"><span data-stu-id="bba20-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a><span data-ttu-id="bba20-106">參數</span><span class="sxs-lookup"><span data-stu-id="bba20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba20-107">*cConnectors* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bba20-107">*cConnectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba20-108">要略過的裝置數目。</span><span class="sxs-lookup"><span data-stu-id="bba20-108">The number of devices to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba20-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bba20-109">Return value</span></span>

<span data-ttu-id="bba20-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bba20-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bba20-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="bba20-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bba20-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bba20-112">Return code</span></span>                                                                             | <span data-ttu-id="bba20-113">Description</span><span class="sxs-lookup"><span data-stu-id="bba20-113">Description</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bba20-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bba20-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="bba20-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="bba20-115">The method succeeded.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="bba20-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="bba20-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="bba20-117">無法略過指定的裝置數目。</span><span class="sxs-lookup"><span data-stu-id="bba20-117">The specified number of devices could not be skipped.</span></span> <span data-ttu-id="bba20-118">其中一個可能的原因： *cConnectors* 參數指定的裝置數目超過實際保留在列舉順序中的數目。</span><span class="sxs-lookup"><span data-stu-id="bba20-118">One possible cause: The *cConnectors* parameter specifies more devices than actually remain in the enumeration sequence.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bba20-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bba20-119">Requirements</span></span>



| <span data-ttu-id="bba20-120">需求</span><span class="sxs-lookup"><span data-stu-id="bba20-120">Requirement</span></span> | <span data-ttu-id="bba20-121">值</span><span class="sxs-lookup"><span data-stu-id="bba20-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba20-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bba20-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bba20-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bba20-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="bba20-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bba20-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bba20-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bba20-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                   |
| <span data-ttu-id="bba20-126">標頭</span><span class="sxs-lookup"><span data-stu-id="bba20-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bba20-127"><dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt></span><span class="sxs-lookup"><span data-stu-id="bba20-127"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="bba20-128">Idl</span><span class="sxs-lookup"><span data-stu-id="bba20-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bba20-129"><dt>Portabledeviceconnectapi .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bba20-129"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="bba20-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="bba20-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="bba20-131"><dt>PortableDeviceGuids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bba20-131"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="bba20-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bba20-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba20-133">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="bba20-133">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




