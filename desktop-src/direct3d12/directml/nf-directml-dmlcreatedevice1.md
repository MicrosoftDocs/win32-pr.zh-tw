---
UID: NF:directml.DMLCreateDevice1
title: DMLCreateDevice1 函式
description: 為指定的 Direct3D 12 裝置建立 DirectML 裝置。
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803768"
---
# <a name="dmlcreatedevice1-function-directmlh"></a><span data-ttu-id="5dc07-103">DMLCreateDevice1 函式 (directml) </span><span class="sxs-lookup"><span data-stu-id="5dc07-103">DMLCreateDevice1 function (directml.h)</span></span>

<span data-ttu-id="5dc07-104">為指定的 Direct3D 12 裝置建立 DirectML 裝置。</span><span class="sxs-lookup"><span data-stu-id="5dc07-104">Creates a DirectML device for a given Direct3D 12 device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5dc07-105">此 API 可作為 DirectML 獨立可轉散發套件的一部分， (請參閱 [DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) 1.4 版和更新版本。</span><span class="sxs-lookup"><span data-stu-id="5dc07-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5dc07-106">另請參閱 [DirectML 版本歷程記錄](../dml-version-history.md)。</span><span class="sxs-lookup"><span data-stu-id="5dc07-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc07-107">語法</span><span class="sxs-lookup"><span data-stu-id="5dc07-107">Syntax</span></span>

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="5dc07-108">參數</span><span class="sxs-lookup"><span data-stu-id="5dc07-108">Parameters</span></span>

`d3d12Device`

<span data-ttu-id="5dc07-109">類型： <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span><span class="sxs-lookup"><span data-stu-id="5dc07-109">Type: <b><a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>\*</b></span></span>

<span data-ttu-id="5dc07-110">[ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device)的指標，代表要建立 DirectML 裝置的 Direct3D 12 裝置。</span><span class="sxs-lookup"><span data-stu-id="5dc07-110">A pointer to an [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) representing the Direct3D 12 device to create the DirectML device over.</span></span> <span data-ttu-id="5dc07-111">DirectML 支援任何 D3D 功能等級，以及在任何介面卡上建立的 Direct3D 12 裝置，包括變形。</span><span class="sxs-lookup"><span data-stu-id="5dc07-111">DirectML supports any D3D feature level, and Direct3D 12 devices created on any adapter, including WARP.</span></span> <span data-ttu-id="5dc07-112">不過，並非 DirectML 中的所有功能都可以根據 Direct3D 12 裝置的功能來使用。</span><span class="sxs-lookup"><span data-stu-id="5dc07-112">However, not all features in DirectML may be available depending on the capabilities of the Direct3D 12 device.</span></span> <span data-ttu-id="5dc07-113">如需詳細資訊，請參閱 [IDMLDevice：： CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) 。</span><span class="sxs-lookup"><span data-stu-id="5dc07-113">See [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) for more info.</span></span>

<span data-ttu-id="5dc07-114">如果 **DMLCreateDevice1** 的呼叫成功，則 DirectML 裝置會維護提供的 Direct3D 12 裝置的強式參考。</span><span class="sxs-lookup"><span data-stu-id="5dc07-114">If the call to **DMLCreateDevice1** is successful, then the DirectML device maintains a strong reference to the supplied Direct3D 12 device.</span></span>

`flags`

<span data-ttu-id="5dc07-115">類型： <b>DML_CREATE_DEVICE_FLAGS</b></span><span class="sxs-lookup"><span data-stu-id="5dc07-115">Type: <b>DML_CREATE_DEVICE_FLAGS</b></span></span>

<span data-ttu-id="5dc07-116">指定其他裝置建立選項的 [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) 值。</span><span class="sxs-lookup"><span data-stu-id="5dc07-116">A [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) value specifying additional device creation options.</span></span>

`minimumFeatureLevel`

<span data-ttu-id="5dc07-117">類型： <b>DML_FEATURE_LEVEL</b></span><span class="sxs-lookup"><span data-stu-id="5dc07-117">Type: <b>DML_FEATURE_LEVEL</b></span></span>

<span data-ttu-id="5dc07-118">[DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)值，指定所需的最小功能層級支援。</span><span class="sxs-lookup"><span data-stu-id="5dc07-118">A [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) value specifying the minimum feature level support required.</span></span>

<span data-ttu-id="5dc07-119">此參數對於需要特定 DirectML 版本的呼叫端很有用，但可能會發現本身呼叫舊版 DirectML 的人員。</span><span class="sxs-lookup"><span data-stu-id="5dc07-119">This parameter can be useful for callers that require a specific version of DirectML, but who may find themselves calling into an older version of DirectML.</span></span> <span data-ttu-id="5dc07-120">例如，當使用者在舊版 Windows 10 上執行您的應用程式時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="5dc07-120">This can happen, for example, when the user runs your application on an older version of Windows 10.</span></span>

<span data-ttu-id="5dc07-121">明確相依于特定功能等級所引進之功能的應用程式，可以將它指定為 *minimumFeatureLevel*。</span><span class="sxs-lookup"><span data-stu-id="5dc07-121">Applications that explicitly depend on functionality introduced in a particular feature level can specify it as a *minimumFeatureLevel*.</span></span> <span data-ttu-id="5dc07-122">這可保證 **DMLCreateDevice1** 將不會成功，除非基礎執行 *至少* 與這項要求的最小功能等級相同。</span><span class="sxs-lookup"><span data-stu-id="5dc07-122">This will guarantee that **DMLCreateDevice1** won't succeed unless the underlying implementation is *at least* as capable as this requested minimum feature level.</span></span>

<span data-ttu-id="5dc07-123">請注意，因為此參數指定 *最小* 的功能等級，所以基礎 DirectML 裝置實際上支援的功能層級高於所要求的最小值。</span><span class="sxs-lookup"><span data-stu-id="5dc07-123">Note that as this parameter specifies a *minimum* feature level, the underlying DirectML device may in fact support a higher feature level than the requested minimum.</span></span> <span data-ttu-id="5dc07-124">裝置建立成功之後，您就可以使用 [IDMLDevice：： CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)來查詢此裝置支援的所有功能層級。</span><span class="sxs-lookup"><span data-stu-id="5dc07-124">Once device creation succeeds, you can query all of the feature levels supported by this device using [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).</span></span>

`riid`

<span data-ttu-id="5dc07-125">類型： <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="5dc07-125">Type: <b>REFIID</b></span></span>

<span data-ttu-id="5dc07-126">您要在 <i>裝置</i>中傳回之介面 (GUID) 的全域唯一識別碼的參考。</span><span class="sxs-lookup"><span data-stu-id="5dc07-126">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>device</i>.</span></span> <span data-ttu-id="5dc07-127">這應該是 [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)的 GUID。</span><span class="sxs-lookup"><span data-stu-id="5dc07-127">This is expected to be the GUID of [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

`ppv`

<span data-ttu-id="5dc07-128">類型： \_ COM \_ Outptr \_ opt \_ <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="5dc07-128">Type: \_COM\_Outptr\_opt\_ <b>void\*\*</b></span></span>

<span data-ttu-id="5dc07-129">記憶體區塊的指標，該區塊會接收裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="5dc07-129">A pointer to a memory block that receives a pointer to the device.</span></span> <span data-ttu-id="5dc07-130">這是 [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)指標的位址，代表所建立的 DirectML 裝置。</span><span class="sxs-lookup"><span data-stu-id="5dc07-130">This is the address of a pointer to an [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice), representing  the DirectML device created.</span></span>


## <a name="return-value"></a><span data-ttu-id="5dc07-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="5dc07-131">Return value</span></span>

<span data-ttu-id="5dc07-132">類型： [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5dc07-132">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5dc07-133">如果函式成功，它會傳回 <b>S_OK</b>。</span><span class="sxs-lookup"><span data-stu-id="5dc07-133">If the function succeeds, it returns <b>S_OK</b>.</span></span> <span data-ttu-id="5dc07-134">否則，它會傳回 [HRESULT](/windows/desktop/winprog/windows-data-types) 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5dc07-134">Otherwise, it returns an [HRESULT](/windows/desktop/winprog/windows-data-types) error code.</span></span>

<span data-ttu-id="5dc07-135">如果此版本的 DirectML 不支援所要求的 *minimumFeatureLevel* ，則此函式會傳回 **DXGI_ERROR_UNSUPPORTED**。</span><span class="sxs-lookup"><span data-stu-id="5dc07-135">If this version of DirectML doesn't support the *minimumFeatureLevel* requested, then this function will return **DXGI_ERROR_UNSUPPORTED**.</span></span>

<span data-ttu-id="5dc07-136">您必須安裝「圖形工具」隨選功能 (FOD) 才能使用 DirectML 的調試層。</span><span class="sxs-lookup"><span data-stu-id="5dc07-136">The Graphics Tools Feature on Demand (FOD) must be installed in order to use the DirectML debug layers.</span></span> <span data-ttu-id="5dc07-137">如果在 *旗標* 中指定 [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags)旗標，且未安裝調試層，則 **DMLCreateDevice1** 會傳回 **DXGI_ERROR_SDK_COMPONENT_MISSING**。</span><span class="sxs-lookup"><span data-stu-id="5dc07-137">If the [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) flag is specified in *flags* and the debug layers are not installed, then **DMLCreateDevice1** returns **DXGI_ERROR_SDK_COMPONENT_MISSING**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dc07-138">備註</span><span class="sxs-lookup"><span data-stu-id="5dc07-138">Remarks</span></span>

<span data-ttu-id="5dc07-139">這個函式 [DMLCreateDevice1]()的較新版本是在 DirectML 版本1.1.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="5dc07-139">A newer version of this function, [DMLCreateDevice1](), was introduced in DirectML version 1.1.0.</span></span> <span data-ttu-id="5dc07-140">**DMLCreateDevice1** 相當於呼叫 **DMLCreateDevice1** 並提供 [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level)的 *minimumFeatureLevel* 。</span><span class="sxs-lookup"><span data-stu-id="5dc07-140">**DMLCreateDevice1** is equivalent to calling **DMLCreateDevice1** and supplying a *minimumFeatureLevel* of [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).</span></span>

## <a name="availability"></a><span data-ttu-id="5dc07-141">可用性</span><span class="sxs-lookup"><span data-stu-id="5dc07-141">Availability</span></span>

<span data-ttu-id="5dc07-142">此 API 是在 DirectML 版本中引進 `1.1.0` 。</span><span class="sxs-lookup"><span data-stu-id="5dc07-142">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc07-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dc07-143">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5dc07-144">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="5dc07-144">**Target Platform**</span></span> | <span data-ttu-id="5dc07-145">Windows</span><span class="sxs-lookup"><span data-stu-id="5dc07-145">Windows</span></span> |
| <span data-ttu-id="5dc07-146">**標頭**</span><span class="sxs-lookup"><span data-stu-id="5dc07-146">**Header**</span></span> | <span data-ttu-id="5dc07-147">directml。h</span><span class="sxs-lookup"><span data-stu-id="5dc07-147">directml.h</span></span> |
| <span data-ttu-id="5dc07-148">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="5dc07-148">**Library**</span></span> | <span data-ttu-id="5dc07-149">DirectML .lib</span><span class="sxs-lookup"><span data-stu-id="5dc07-149">DirectML.lib</span></span> |
| <span data-ttu-id="5dc07-150">**DLL**</span><span class="sxs-lookup"><span data-stu-id="5dc07-150">**DLL**</span></span> | <span data-ttu-id="5dc07-151">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="5dc07-151">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="5dc07-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dc07-152">See also</span></span>

* [<span data-ttu-id="5dc07-153">DML_FEATURE_LEVEL 列舉</span><span class="sxs-lookup"><span data-stu-id="5dc07-153">DML_FEATURE_LEVEL enumeration</span></span>](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [<span data-ttu-id="5dc07-154">DirectML 版本歷程記錄</span><span class="sxs-lookup"><span data-stu-id="5dc07-154">DirectML version history</span></span>](../dml-version-history.md)
* [<span data-ttu-id="5dc07-155">DirectML 功能等級歷程記錄</span><span class="sxs-lookup"><span data-stu-id="5dc07-155">DirectML feature level history</span></span>](/windows/win32/direct3d12/dml-feature_level-history)    
* [<span data-ttu-id="5dc07-156">使用 DirectML debug layer</span><span class="sxs-lookup"><span data-stu-id="5dc07-156">Using the DirectML debug layer</span></span>](../dml-debug-layer.md)