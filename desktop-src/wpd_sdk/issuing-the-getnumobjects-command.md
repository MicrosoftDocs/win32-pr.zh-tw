---
description: 發出 GetNumObjects 命令
ms.assetid: d06690e4-f592-4b17-a5f1-baec2accc8dd
title: 發出 GetNumObjects 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3ece98e409ab4ee2774c4efdba0c84c06c60e373b5ed15aee77f5dee65d9101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194008"
---
# <a name="issuing-the-getnumobjects-command"></a>發出 GetNumObjects 命令

此區段中的範例會叫用 **GetNumObjects** MTP 命令。  (如需此命令及其參數的完整描述，請參閱 [MTP 規格](https://www.usb.org/sites/default/files/MTPv1_1.zip)。 ) 

在您叫用此命令之前，您必須先設定命令參數。


```
#include <portabledevice.h>
#include <portabledeviceapi.h>
#include <wpdmtpextensions.h>

HRESULT SendGetNumObjects(IPortableDevice* pDevice)
{
    HRESULT hr = S_OK;
    const WORD PTP_OPCODE_GETNUMOBJECT = 0x1006; // GetNumObject opcode is 0x1006
    const WORD PTP_RESPONSECODE_OK = 0x2001;     // 0x2001 indicates command success

    // Build basic WPD parameters for the command
    CComPtr<IPortableDeviceValues> spParameters;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**)&spParameters);
    }

    // Use the WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE command
    // Similar commands exist for reading and writing data phases
    if (hr == S_OK)
    {
        hr = spParameters->SetGuidValue(WPD_PROPERTY_COMMON_COMMAND_CATEGORY, 
                                           WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE.fmtid);
    }

    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_COMMON_COMMAND_ID, 
                                                      WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE.pid);
    }

    // Specify the actual MTP opcode that we want to execute here
    if (hr == S_OK)
    {
        hr = spParameters->SetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_OPERATION_CODE, 
                                                      (ULONG) PTP_OPCODE_GETNUMOBJECT);
    }

    // GetNumObject requires three params - storage ID, object format, and parent object handle   
    // Parameters need to be first put into a PropVariantCollection
    CComPtr<IPortableDevicePropVariantCollection> spMtpParams;
    if (hr == S_OK)
    {
        hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                                  NULL,
                                  CLSCTX_INPROC_SERVER,
                                  IID_IPortableDevicePropVariantCollection,
                                  (VOID**)&spMtpParams);
    }

    PROPVARIANT pvParam = {0};
    pvParam.vt = VT_UI4;

    // Specify storage ID parameter. Most devices that have 0x10001 have the storage ID. This
    // should be changed to use the device's real storage ID (which can be obtained by
    // removing the prefix for the WPD object ID for the storage)
    if (hr == S_OK)
    {
        pvParam.ulVal = 0x10001;
        hr = spMtpParams->Add(&pvParam);
    }

    // Specify object format code parameter. 0x0 can be specified to indicate this is unused 
    if (hr == S_OK)
    {
        pvParam.ulVal = 0x0;
        hr = spMtpParams->Add(&pvParam);
    }

    // Specify parent object handle parameter. 0x0 can be specified to indicate this is unused
    if (hr == S_OK)
    {
        pvParam.ulVal = 0x0;
        hr = spMtpParams->Add(&pvParam);
    }

    // Add MTP parameters collection to our main parameter list
    if (hr == S_OK)
    {
        hr = spParameters->SetIPortableDevicePropVariantCollectionValue(
                                          WPD_PROPERTY_MTP_EXT_OPERATION_PARAMS, spMtpParams);
    }  
```



設定好參數之後，應用程式會叫用命令。


```C++
// Send the command to the MTP device
    CComPtr<IPortableDeviceValues> spResults;
    if (hr == S_OK)
    {
        hr = pDevice->SendCommand(0, spParameters, &spResults);
    } 
```



當應用程式叫用命令之後，它會處理 MTP 驅動程式的回應。


```C++
// Check if the driver was able to send the command by interrogating WPD_PROPERTY_COMMON_HRESULT
    HRESULT hrCmd = S_OK;
    if (hr == S_OK)
    {
         hr = spResults->GetErrorValue(WPD_PROPERTY_COMMON_HRESULT, &hrCmd);
    }

    if (hr == S_OK)
    {
        printf("Driver return code: 0x%08X\n", hrCmd);
        hr = hrCmd;
    }

    // If the command was executed successfully, check the MTP response code to see if the
    // device can handle the command. Be aware that there is a distinction between the command
    // being successfully sent to the device and the command being handled successfully by the device.
    DWORD dwResponseCode;
    if (hr == S_OK)
    {
        hr = spResults->GetUnsignedIntegerValue(WPD_PROPERTY_MTP_EXT_RESPONSE_CODE, &dwResponseCode);
    }

    if (hr == S_OK)
    {
        printf("MTP Response code: 0x%X\n", dwResponseCode);
        hr = (dwResponseCode == (DWORD) PTP_RESPONSECODE_OK) ? S_OK : E_FAIL;
    }
  
    // If the command was executed successfully, the MTP response parameters are returned in 
    // the WPD_PROPERTY_MTP_EXT_RESPONSE_PARAMS property, which is a PropVariantCollection
    CComPtr<IPortableDevicePropVariantCollection> spRespParams;
    if (hr == S_OK)
    {
        hr = spResults->GetIPortableDevicePropVariantCollectionValue(WPD_PROPERTY_MTP_EXT_RESPONSE_PARAMS, 
                                                                        &spRespParams);
    }

    // The first response parameter contains the number of objects result
    PROPVARIANT pvResult = {0};
    if (hr == S_OK)
    {
        hr = spRespParams->GetAt(0, &pvResult);
    }
   
    if (hr == S_OK)
    {
        printf("Reported number of objects: %d", pvResult.ulVal);
        PropVariantClear(&pvResult);    // Not really required, but use it for completeness
    }

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[支援 MTP 擴充功能](supporting-mtp-extensions.md)
</dt> </dl>

 

 



