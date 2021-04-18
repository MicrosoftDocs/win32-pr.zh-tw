---
title: IDeviceAccessPolicyCheck DeviceInterfaceClassAccessCheckWithCallingThread 方法
description: 此 API 會判斷目前內容的權杖是否可存取指定的裝置介面類別別。 IID 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B。
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- DeviceInterfaceClassAccessCheckWithCallingThread 方法 Device Access Broker API
- DeviceInterfaceClassAccessCheckWithCallingThread 方法 Device Access Broker API，IDeviceAccessPolicyCheck 介面
- IDeviceAccessPolicyCheck 介面裝置存取代理程式 API，DeviceInterfaceClassAccessCheckWithCallingThread 方法
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "106965216"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a><span data-ttu-id="8783c-107">IDeviceAccessPolicyCheck：:D eviceInterfaceClassAccessCheckWithCallingThread 方法</span><span class="sxs-lookup"><span data-stu-id="8783c-107">IDeviceAccessPolicyCheck::DeviceInterfaceClassAccessCheckWithCallingThread method</span></span>

> [!Important]  
> <span data-ttu-id="8783c-108">這些介面不受支援，且不應該使用。</span><span class="sxs-lookup"><span data-stu-id="8783c-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="8783c-109">請改用 [裝置存取 API c + + 程式設計參考](device-access-api-c---programming-reference.md) 中的 api。</span><span class="sxs-lookup"><span data-stu-id="8783c-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="8783c-110">此 API 會判斷目前內容的權杖是否可存取指定的裝置介面類別別。</span><span class="sxs-lookup"><span data-stu-id="8783c-110">This API will determine if the token for the current context has access to the device interface class specified.</span></span> <span data-ttu-id="8783c-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B。</span><span class="sxs-lookup"><span data-stu-id="8783c-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span></span>

## <a name="syntax"></a><span data-ttu-id="8783c-112">語法</span><span class="sxs-lookup"><span data-stu-id="8783c-112">Syntax</span></span>

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a><span data-ttu-id="8783c-113">參數</span><span class="sxs-lookup"><span data-stu-id="8783c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8783c-114">*pszDeviceInterfaceClassGuid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8783c-114">*pszDeviceInterfaceClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8783c-115">應檢查其存取權的裝置介面類別別 GUID。</span><span class="sxs-lookup"><span data-stu-id="8783c-115">Device interface class GUID for which access should be checked.</span></span>

</dd> <dt>

<span data-ttu-id="8783c-116">*dwClientThreadId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8783c-116">*dwClientThreadId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8783c-117">用戶端執行緒識別碼，視需要顯示任何相關聯的 UI。</span><span class="sxs-lookup"><span data-stu-id="8783c-117">Client thread ID where any associated UI should be shown if necessary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8783c-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="8783c-118">Return value</span></span>

<span data-ttu-id="8783c-119">如果此函式成功，它會傳回 S_OK。</span><span class="sxs-lookup"><span data-stu-id="8783c-119">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="8783c-120">否則，它會傳回 HRESULT 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8783c-120">Otherwise, it returns an HRESULT error code.</span></span>
