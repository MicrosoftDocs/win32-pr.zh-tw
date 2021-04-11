---
description: 建立目前 IEnumPortableDeviceConnectors 介面的複本。
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'IEnumPortableDeviceConnectors：： Clone 方法 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320403"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a><span data-ttu-id="047c5-103">IEnumPortableDeviceConnectors：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="047c5-103">IEnumPortableDeviceConnectors::Clone method</span></span>

<span data-ttu-id="047c5-104">**Clone** 方法會建立目前 [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)介面的複本。</span><span class="sxs-lookup"><span data-stu-id="047c5-104">The **Clone** method creates a copy of the current [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="047c5-105">語法</span><span class="sxs-lookup"><span data-stu-id="047c5-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="047c5-106">參數</span><span class="sxs-lookup"><span data-stu-id="047c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="047c5-107">*ppEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="047c5-107">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="047c5-108">[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="047c5-108">The address of a pointer to an [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span> <span data-ttu-id="047c5-109">呼叫的應用程式必須在其完成時釋放這個介面。</span><span class="sxs-lookup"><span data-stu-id="047c5-109">The calling application must release this interface when it is done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="047c5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="047c5-110">Return value</span></span>

<span data-ttu-id="047c5-111">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="047c5-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="047c5-112">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="047c5-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="047c5-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="047c5-113">Return code</span></span>                                                                          | <span data-ttu-id="047c5-114">Description</span><span class="sxs-lookup"><span data-stu-id="047c5-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="047c5-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="047c5-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="047c5-116">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="047c5-116">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="047c5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="047c5-117">Requirements</span></span>



| <span data-ttu-id="047c5-118">需求</span><span class="sxs-lookup"><span data-stu-id="047c5-118">Requirement</span></span> | <span data-ttu-id="047c5-119">值</span><span class="sxs-lookup"><span data-stu-id="047c5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047c5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="047c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="047c5-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="047c5-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="047c5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="047c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="047c5-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="047c5-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="047c5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="047c5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="047c5-125"><dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt></span><span class="sxs-lookup"><span data-stu-id="047c5-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="047c5-126">Idl</span><span class="sxs-lookup"><span data-stu-id="047c5-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="047c5-127"><dt>Portabledeviceconnectapi .idl</dt></span><span class="sxs-lookup"><span data-stu-id="047c5-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="047c5-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="047c5-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="047c5-129"><dt>PortableDeviceGuids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="047c5-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="047c5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="047c5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047c5-131">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="047c5-131">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




