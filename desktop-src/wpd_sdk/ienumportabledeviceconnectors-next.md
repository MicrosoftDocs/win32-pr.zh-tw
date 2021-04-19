---
description: 抓取列舉順序中的下一個或多個 IPortableDeviceConnector 物件。
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: 'IEnumPortableDeviceConnectors：： Next 方法 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 709e938c28f9bf09e34d918eea7be3029c7a11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987363"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a><span data-ttu-id="9a55f-103">IEnumPortableDeviceConnectors：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="9a55f-103">IEnumPortableDeviceConnectors::Next method</span></span>

<span data-ttu-id="9a55f-104">**下** 一個方法會抓取列舉順序中的下一個或多個 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)物件。</span><span class="sxs-lookup"><span data-stu-id="9a55f-104">The **Next** method retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a55f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a55f-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="9a55f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a55f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a55f-107">*cRequested* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a55f-107">*cRequested* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a55f-108">要求的裝置數目。</span><span class="sxs-lookup"><span data-stu-id="9a55f-108">The number of requested devices.</span></span> <span data-ttu-id="9a55f-109">此值也會指出由 *pConnectors* 參數指定之呼叫端配置陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="9a55f-109">This value also indicates the number of elements in the caller-allocated array specified by the *pConnectors* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9a55f-110">*pConnectors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9a55f-110">*pConnectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a55f-111">[**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)指標的陣列，每個指標都會指定配對的 MTP 藍牙裝置。</span><span class="sxs-lookup"><span data-stu-id="9a55f-111">An array of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) pointers, each specifying a paired MTP Bluetooth device.</span></span> <span data-ttu-id="9a55f-112">呼叫端必須配置 **IPortableDeviceConnector** 指標的陣列，以及由 *cRequested* 參數指定的陣列長度。</span><span class="sxs-lookup"><span data-stu-id="9a55f-112">The caller must allocate an array of **IPortableDeviceConnector** pointers, with the array length specified by the *cRequested* parameter.</span></span> <span data-ttu-id="9a55f-113">在成功傳回時，呼叫端必須釋放陣列和傳回的指標。</span><span class="sxs-lookup"><span data-stu-id="9a55f-113">On successful return, the caller must free both the array and the returned pointers.</span></span> <span data-ttu-id="9a55f-114">**IPortableDeviceConnector** 介面會藉由呼叫 **IUnknown：： Release** 方法釋放。</span><span class="sxs-lookup"><span data-stu-id="9a55f-114">The **IPortableDeviceConnector** interfaces are freed by calling the **IUnknown::Release** method.</span></span>

</dd> <dt>

<span data-ttu-id="9a55f-115">*pcFetched* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9a55f-115">*pcFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a55f-116">實際取出的 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) 介面數目。</span><span class="sxs-lookup"><span data-stu-id="9a55f-116">The number of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces that are actually retrieved.</span></span> <span data-ttu-id="9a55f-117">如果未抓取任何 **IPortableDeviceConnector** 介面，且傳回值為 **\_ FALSE**，則表示沒有其他 **IPortableDeviceConnector** 介面可供列舉。</span><span class="sxs-lookup"><span data-stu-id="9a55f-117">If no **IPortableDeviceConnector** interfaces are retrieved and the return value is **S\_FALSE**, there are no more **IPortableDeviceConnector** interfaces to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a55f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a55f-118">Return value</span></span>

<span data-ttu-id="9a55f-119">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9a55f-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9a55f-120">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="9a55f-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9a55f-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9a55f-121">Return code</span></span>                                                                             | <span data-ttu-id="9a55f-122">Description</span><span class="sxs-lookup"><span data-stu-id="9a55f-122">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a55f-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9a55f-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9a55f-124">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="9a55f-124">The method succeeded.</span></span><br/>                                 |
| <dl> <span data-ttu-id="9a55f-125"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="9a55f-125"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9a55f-126">沒有其他 MTP 藍牙裝置可供列舉。</span><span class="sxs-lookup"><span data-stu-id="9a55f-126">There are no more MTP Bluetooth devices to enumerate.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="9a55f-127">範例</span><span class="sxs-lookup"><span data-stu-id="9a55f-127">Examples</span></span>

<span data-ttu-id="9a55f-128">下列範例示範如何使用這個方法來列舉成對的 MTP/Bluetooth 裝置，以及將非同步連線要求傳送給每個裝置。</span><span class="sxs-lookup"><span data-stu-id="9a55f-128">The following example demonstrates the use of this method to enumerate paired MTP/Bluetooth devices, and to send an asynchronous connection request to each.</span></span>


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a><span data-ttu-id="9a55f-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a55f-129">Requirements</span></span>



| <span data-ttu-id="9a55f-130">需求</span><span class="sxs-lookup"><span data-stu-id="9a55f-130">Requirement</span></span> | <span data-ttu-id="9a55f-131">值</span><span class="sxs-lookup"><span data-stu-id="9a55f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a55f-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a55f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9a55f-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a55f-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="9a55f-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a55f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9a55f-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="9a55f-135">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="9a55f-136">標頭</span><span class="sxs-lookup"><span data-stu-id="9a55f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a55f-137"><dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt></span><span class="sxs-lookup"><span data-stu-id="9a55f-137"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="9a55f-138">Idl</span><span class="sxs-lookup"><span data-stu-id="9a55f-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a55f-139"><dt>Portabledeviceconnectapi .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a55f-139"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="9a55f-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a55f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a55f-141"><dt>PortableDeviceGuids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a55f-141"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="9a55f-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a55f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a55f-143">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="9a55f-143">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




