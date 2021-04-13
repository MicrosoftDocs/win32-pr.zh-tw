---
title: IDeviceBroker OpenDeviceFromInterfacePath 方法
description: 嘗試代表用戶端開啟裝置介面實例。 IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98。
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- OpenDeviceFromInterfacePath 方法 Device Access Broker API
- OpenDeviceFromInterfacePath 方法 Device Access Broker API，IDeviceBroker 介面
- IDeviceBroker 介面裝置存取代理程式 API，OpenDeviceFromInterfacePath 方法
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374338"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a><span data-ttu-id="77028-107">IDeviceBroker：： OpenDeviceFromInterfacePath 方法</span><span class="sxs-lookup"><span data-stu-id="77028-107">IDeviceBroker::OpenDeviceFromInterfacePath method</span></span>

> [!Important]  
> <span data-ttu-id="77028-108">這些介面不受支援，且不應該使用。</span><span class="sxs-lookup"><span data-stu-id="77028-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="77028-109">請改用 [裝置存取 API c + + 程式設計參考](device-access-api-c---programming-reference.md) 中的 api。</span><span class="sxs-lookup"><span data-stu-id="77028-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="77028-110">嘗試代表用戶端開啟裝置介面實例。</span><span class="sxs-lookup"><span data-stu-id="77028-110">Attempts to open a device interface instance on behalf of a client.</span></span> <span data-ttu-id="77028-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98。</span><span class="sxs-lookup"><span data-stu-id="77028-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span></span>

## <a name="syntax"></a><span data-ttu-id="77028-112">語法</span><span class="sxs-lookup"><span data-stu-id="77028-112">Syntax</span></span>

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a><span data-ttu-id="77028-113">參數</span><span class="sxs-lookup"><span data-stu-id="77028-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77028-114">*pszDeviceInterfacePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77028-114">*pszDeviceInterfacePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77028-115">要開啟的裝置介面實例。</span><span class="sxs-lookup"><span data-stu-id="77028-115">Device interface instance to open.</span></span>

</dd> <dt>

<span data-ttu-id="77028-116">*desiredAccess* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77028-116">*desiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77028-117">要傳遞至 open 的預期存取權。</span><span class="sxs-lookup"><span data-stu-id="77028-117">Desired access to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="77028-118">*shareMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77028-118">*shareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77028-119">要傳遞至 open 的共用模式。</span><span class="sxs-lookup"><span data-stu-id="77028-119">Share mode to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="77028-120">*flagsAndAttributes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77028-120">*flagsAndAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77028-121">要傳遞至 open 的旗標和屬性。</span><span class="sxs-lookup"><span data-stu-id="77028-121">Flags and attributes to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="77028-122">*\* phDevice* \[\]</span><span class="sxs-lookup"><span data-stu-id="77028-122">*\*phDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77028-123">開啟成功時產生的控制碼。</span><span class="sxs-lookup"><span data-stu-id="77028-123">Resulting handle if open was successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77028-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="77028-124">Return value</span></span>

<span data-ttu-id="77028-125">如果此函式成功，它會傳回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="77028-125">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="77028-126">否則，它會傳回 HRESULT 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="77028-126">Otherwise, it returns an HRESULT error code.</span></span>
