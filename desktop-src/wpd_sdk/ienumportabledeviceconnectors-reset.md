---
description: IEnumPortableDeviceConnectors：： Reset 方法-將列舉順序重設為開頭。
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'IEnumPortableDeviceConnectors：： Reset 方法 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083204"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="bd6bf-103">IEnumPortableDeviceConnectors：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="bd6bf-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="bd6bf-104">**Reset** 方法會將列舉順序重設為開頭。</span><span class="sxs-lookup"><span data-stu-id="bd6bf-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd6bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="bd6bf-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="bd6bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd6bf-106">Parameters</span></span>

<span data-ttu-id="bd6bf-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bd6bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd6bf-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd6bf-108">Return value</span></span>

<span data-ttu-id="bd6bf-109">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bd6bf-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bd6bf-110">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="bd6bf-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bd6bf-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bd6bf-111">Return code</span></span>                                                                          | <span data-ttu-id="bd6bf-112">Description</span><span class="sxs-lookup"><span data-stu-id="bd6bf-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bd6bf-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bd6bf-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bd6bf-114">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="bd6bf-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd6bf-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd6bf-115">Requirements</span></span>



| <span data-ttu-id="bd6bf-116">需求</span><span class="sxs-lookup"><span data-stu-id="bd6bf-116">Requirement</span></span> | <span data-ttu-id="bd6bf-117">值</span><span class="sxs-lookup"><span data-stu-id="bd6bf-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6bf-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd6bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6bf-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd6bf-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="bd6bf-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd6bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6bf-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="bd6bf-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="bd6bf-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bd6bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6bf-123"><dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6bf-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="bd6bf-124">Idl</span><span class="sxs-lookup"><span data-stu-id="bd6bf-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd6bf-125"><dt>Portabledeviceconnectapi .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd6bf-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="bd6bf-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="bd6bf-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd6bf-127"><dt>PortableDeviceGuids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd6bf-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="bd6bf-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd6bf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6bf-129">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="bd6bf-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




