---
description: 釋放 IPortableDeviceManager：： GetDevices 或 IPortableDeviceServiceManager：： GetDeviceServices 方法所取出的隨插即用 (PnP) 識別碼。
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: 'FreePortableDevicePnPIDs 函式 (PortableDevice) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193943"
---
# <a name="freeportabledevicepnpids-function"></a><span data-ttu-id="eec87-103">FreePortableDevicePnPIDs 函式</span><span class="sxs-lookup"><span data-stu-id="eec87-103">FreePortableDevicePnPIDs function</span></span>

<span data-ttu-id="eec87-104">**FreePortableDevicePnPIDs** helper 函式會釋放 [**IPortableDeviceManager：： GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)或 [**IPortableDeviceServiceManager：： GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices)方法所抓取的隨插即用 (PnP) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="eec87-104">The **FreePortableDevicePnPIDs** helper function frees the Plug and Play (PnP) identifiers that are retrieved by the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) or [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec87-105">語法</span><span class="sxs-lookup"><span data-stu-id="eec87-105">Syntax</span></span>


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a><span data-ttu-id="eec87-106">參數</span><span class="sxs-lookup"><span data-stu-id="eec87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eec87-107">*pPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="eec87-107">*pPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="eec87-108">要釋放的隨插即用 (PnP) 識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="eec87-108">The array of Plug and Play (PnP) identifiers to be freed.</span></span>

</dd> <dt>

<span data-ttu-id="eec87-109">*cPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="eec87-109">*cPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="eec87-110">*PPnPIDs* 參數所指定之陣列中的識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="eec87-110">The number of identifiers in the array specified by the *pPnPIDs* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eec87-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="eec87-111">Return value</span></span>

<span data-ttu-id="eec87-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="eec87-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec87-113">備註</span><span class="sxs-lookup"><span data-stu-id="eec87-113">Remarks</span></span>

<span data-ttu-id="eec87-114">應用程式會負責釋放它所配置的指標陣列。</span><span class="sxs-lookup"><span data-stu-id="eec87-114">The application is responsible for freeing the array of pointers that it allocates.</span></span>

## <a name="examples"></a><span data-ttu-id="eec87-115">範例</span><span class="sxs-lookup"><span data-stu-id="eec87-115">Examples</span></span>


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a><span data-ttu-id="eec87-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="eec87-116">Requirements</span></span>



| <span data-ttu-id="eec87-117">需求</span><span class="sxs-lookup"><span data-stu-id="eec87-117">Requirement</span></span> | <span data-ttu-id="eec87-118">值</span><span class="sxs-lookup"><span data-stu-id="eec87-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec87-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eec87-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eec87-120">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eec87-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="eec87-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eec87-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eec87-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="eec87-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="eec87-123">標頭</span><span class="sxs-lookup"><span data-stu-id="eec87-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec87-124"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="eec87-124"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




