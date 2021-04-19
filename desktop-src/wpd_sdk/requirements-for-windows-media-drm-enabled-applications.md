---
description: Windows Media DRM-Enabled 應用程式的需求
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Windows Media DRM-Enabled 應用程式的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982807"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Windows Media DRM-Enabled 應用程式的需求

To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document. 此外，在開啟裝置時，應用程式必須在用戶端資訊中提供其他屬性。

下表說明啟用 Windows Media 受 DRM 保護的內容傳輸所需的兩個額外屬性。



| 屬性                                      | 描述                              |
|-----------------------------------------------|------------------------------------------|
| WPD \_ 用戶端 \_ WMDRM \_ 應用程式 \_ 私用 \_ 金鑰 | 指定應用程式的私密金鑰。 |
| WPD \_ 用戶端 \_ WMDRM \_ 應用程式 \_ 憑證  | 指定應用程式的憑證。 |



 

當使用 [**IPortableDevice：： Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) 方法開啟裝置時，必須在應用程式的用戶端資訊中提供這些屬性。 當提供這些屬性時，WPD API 會允許受保護的內容傳輸。 如果應用程式已提供憑證和私密金鑰，則 API 會建立安全通道，以將受保護的 WMDRM 內容傳輸至裝置。

如需有關建立和散發支援 Windows Media DRM 之 Windows 應用程式的詳細資訊，請參閱下列以 [windows 為基礎的授權應用程式](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) 主題。

## <a name="transferring-content"></a>傳送內容

若要傳送受 WMDRM 保護的內容，請使用 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)。 此方法可用於受保護和純文字的內容，而不需要額外的選項。 WPD API 會根據內容是否受到保護或清除，自動選取受保護或清除的通道。 它會與 WMDRM 安全內容提供者互動以處理 WMDRM 授權。

## <a name="transferring-known-clear-content"></a>傳送已知的清楚內容

如果您已啟用應用程式來處理受保護的內容，但您知道特定檔案未受到保護，您可以在呼叫 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)以取得清除 **內容時，** 將 **WPD \_ API 選項 [ \_ \_ 使用 \_ 清除 \_ 資料流程 \_** ] 選項設定為 [TRUE]，以告知 WPD 略過 DRM 處理。

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>使用 IWMDRMDeviceApp 存取計量作業

WPD 提供一種機制，可存取授權更新和計量資料抓取的 **IWMDRMDeviceApp** api。 若要透過 WPD 存取此 API，請從 [**IPortableDeviceContent：： CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)傳回的 **IStream** 呼叫 **IID \_ IWMDRMDeviceApp** 上的 **QueryInterface** 。 這個 **IWMDRMDeviceApp** 實例系結至與您的 WMDRM 相容裝置 **IPortableDevice** 的連線，而不是已取得 **IStream** 之特定內容的連結。 WPD 會在內部包裝計量 Api，並使其可供您的應用程式存取。 您的應用程式應該 \_ \_ 針對 IWMDMDevice 參數使用 WMDRMDEVICEAPP use WPD \_ 裝置 \_ PTR 常數 \* 。

下列程式碼片段會示範這一點。


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



應用程式私密金鑰和憑證的必要條件也同樣適用于此處。 如果金鑰/憑證無效，或 WMDRM 系統無法初始化， **QueryInferface** 呼叫將會失敗。

如果您的應用程式已經執行先前受保護的內容傳輸，上述從 **IStream** 指標取得 **IWMDRMDeviceApp** 介面的方法就是很方便的方法，然後再繼續進行計量和授權同步處理作業。

對於需要存取 **IWMDRMDeviceApp** 的大部分應用程式，我們的建議是直接初始化 **IWMDRMDeviceApp** ，因為這不需要您的應用程式傳送受保護的內容或保存到傳輸介面，以便進行裝置計量和授權同步處理。此方法需要使用 Windows Media 裝置管理員 (WMDM) Api。 如需詳細資訊和範例程式碼，請參閱 WHDC 網站上的 [從 WPD 應用程式存取 WMDRM api](../windows-portable-devices.md) 白皮書。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows 可攜式裝置**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
