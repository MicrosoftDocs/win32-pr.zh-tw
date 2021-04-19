---
description: Windows 可攜式裝置 (WPD) 支援下列命令參數的屬性。
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: '命令參數 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978794"
---
# <a name="command-parameters"></a><span data-ttu-id="7b0c9-103">命令參數</span><span class="sxs-lookup"><span data-stu-id="7b0c9-103">Command Parameters</span></span>

<span data-ttu-id="7b0c9-104">Windows 可攜式裝置 (WPD) 支援下列命令參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-104">Windows Portable Devices (WPD) supports the following properties of command parameters.</span></span>




| <span data-ttu-id="7b0c9-105">**屬性**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-105">**Property**</span></span>                                            | <span data-ttu-id="7b0c9-106">**VarType**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-106">**VarType**</span></span>     | <span data-ttu-id="7b0c9-107">**說明**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-107">**Description**</span></span>                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0c9-108">**WPD \_ 屬性 \_ 通用 \_ 用戶端 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-108">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION**</span></span>          | <span data-ttu-id="7b0c9-109">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="7b0c9-110">驅動程式用來識別用戶端的 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-110">An [**IPortableDeviceValues**](iportabledevicevalues.md) interface that the driver uses to identify the client.</span></span>                                                             |
| <span data-ttu-id="7b0c9-111">**WPD \_ 屬性 \_ 通用 \_ 用戶端 \_ 資訊 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-111">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION\_CONTEXT**</span></span> | <span data-ttu-id="7b0c9-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="7b0c9-113">驅動程式指定的內容，用來識別所有後續作業的用戶端。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-113">A driver-specified context which identifies a client for all subsequent operations.</span></span>                                                                                          |
| <span data-ttu-id="7b0c9-114">**WPD \_ 屬性 \_ 通用 \_ 命令 \_ 類別目錄**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-114">**WPD\_PROPERTY\_COMMON\_COMMAND\_CATEGORY**</span></span>            | <span data-ttu-id="7b0c9-115">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-115">**VT\_CLSID**</span></span>   | <span data-ttu-id="7b0c9-116">命令之 **PROPERTYKEY** 值的 **GUID** 部分。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-116">The **GUID** portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                                            |
| <span data-ttu-id="7b0c9-117">**WPD \_ 屬性 \_ 通用 \_ 命令 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-117">**WPD\_PROPERTY\_COMMON\_COMMAND\_ID**</span></span>                  | <span data-ttu-id="7b0c9-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-118">**VT\_UI4**</span></span>     | <span data-ttu-id="7b0c9-119"> (PID 的持續性唯一識別碼) 部分的命令 **PROPERTYKEY** 值。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-119">The Persistent Unique ID (PID) portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                          |
| <span data-ttu-id="7b0c9-120">**WPD \_ 屬性 \_ 通用 \_ 命令 \_ 目標**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-120">**WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET**</span></span>              | <span data-ttu-id="7b0c9-121">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-121">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="7b0c9-122">目標物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-122">The target-object identifier.</span></span>                                                                                                                                                |
| <span data-ttu-id="7b0c9-123">**WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-123">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>          | <span data-ttu-id="7b0c9-124">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-124">**VT\_UI4**</span></span>     | <span data-ttu-id="7b0c9-125">WPD 驅動程式所傳回的驅動程式特定錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-125">A driver-specific error code returned by a WPD driver.</span></span>                                                                                                                       |
| <span data-ttu-id="7b0c9-126">**WPD \_ 屬性 \_ 通用 \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-126">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                      | <span data-ttu-id="7b0c9-127">**VT \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-127">**VT\_ERROR**</span></span>   | <span data-ttu-id="7b0c9-128">特定作業的 WPD 驅動程式所傳回的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-128">The **HRESULT** value returned by a WPD driver for a particular operation.</span></span>                                                                                                   |
| <span data-ttu-id="7b0c9-129">**WPD \_ 屬性 \_ 通用 \_ 物件 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-129">**WPD\_PROPERTY\_COMMON\_OBJECT\_IDS**</span></span>                  | <span data-ttu-id="7b0c9-130">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-130">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="7b0c9-131">Variant 型別 **VT \_ LPWSTR** 的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)介面，其中包含物件識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-131">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of object identifiers.</span></span> |
| <span data-ttu-id="7b0c9-132">**WPD \_ 屬性 \_ 常見的 \_ 持續性 \_ 唯一 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-132">**WPD\_PROPERTY\_COMMON\_PERSISTENT\_UNIQUE\_IDS**</span></span>      | <span data-ttu-id="7b0c9-133">**VT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-133">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="7b0c9-134">Variant 型別 **VT \_ LPWSTR** 的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)介面，其中包含 pid 的清單。</span><span class="sxs-lookup"><span data-stu-id="7b0c9-134">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of PIDs.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="7b0c9-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b0c9-135">Requirements</span></span>



| <span data-ttu-id="7b0c9-136">需求</span><span class="sxs-lookup"><span data-stu-id="7b0c9-136">Requirement</span></span> | <span data-ttu-id="7b0c9-137">值</span><span class="sxs-lookup"><span data-stu-id="7b0c9-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0c9-138">標頭</span><span class="sxs-lookup"><span data-stu-id="7b0c9-138">Header</span></span><br/> | <dl> <span data-ttu-id="7b0c9-139"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b0c9-139"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0c9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b0c9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0c9-141">**屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="7b0c9-141">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




