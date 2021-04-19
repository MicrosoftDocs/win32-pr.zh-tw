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
# <a name="ienumportabledeviceconnectorsnext-method"></a>IEnumPortableDeviceConnectors：： Next 方法

**下** 一個方法會抓取列舉順序中的下一個或多個 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)物件。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cRequested* \[在\]
</dt> <dd>

要求的裝置數目。 此值也會指出由 *pConnectors* 參數指定之呼叫端配置陣列中的元素數目。

</dd> <dt>

*pConnectors* \[擴展\]
</dt> <dd>

[**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)指標的陣列，每個指標都會指定配對的 MTP 藍牙裝置。 呼叫端必須配置 **IPortableDeviceConnector** 指標的陣列，以及由 *cRequested* 參數指定的陣列長度。 在成功傳回時，呼叫端必須釋放陣列和傳回的指標。 **IPortableDeviceConnector** 介面會藉由呼叫 **IUnknown：： Release** 方法釋放。

</dd> <dt>

*pcFetched* \[in、out\]
</dt> <dd>

實際取出的 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) 介面數目。 如果未抓取任何 **IPortableDeviceConnector** 介面，且傳回值為 **\_ FALSE**，則表示沒有其他 **IPortableDeviceConnector** 介面可供列舉。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                             | Description                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 此方法已成功。<br/>                                 |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 沒有其他 MTP 藍牙裝置可供列舉。<br/> |



 

## <a name="examples"></a>範例

下列範例示範如何使用這個方法來列舉成對的 MTP/Bluetooth 裝置，以及將非同步連線要求傳送給每個裝置。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                                                                             |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi .idl</dt> </dl>                                                                |
| 程式庫<br/>                  | <dl> <dt>PortableDeviceGuids .lib</dt> </dl>                                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




