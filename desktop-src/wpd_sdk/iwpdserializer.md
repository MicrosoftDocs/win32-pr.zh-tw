---
description: 設備磁碟機會使用 IWpdSerializer 介面，將 IPortableDeviceValues 介面序列化為與應用程式通訊所用的原始資料緩衝區。應用程式不需要使用此介面，因為資料會在呼叫 IPortableDevice：： SendCommand 時自動序列化和還原序列化。若要取得此介面，請呼叫 CoCreateInstance 並傳入 IID \_ IWpdSerializer。
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: 'IWpdSerializer 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 51bb44a7ffec600ff6a059815f096b6920095ece1abd6606e9449045137dbc61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704458"
---
# <a name="iwpdserializer-interface"></a>IWpdSerializer 介面

設備磁碟機會使用 **IWpdSerializer** 介面，將 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面序列化為與應用程式通訊所用的原始資料緩衝區。

應用程式不需要使用此介面，因為資料會在呼叫 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)時自動序列化和還原序列化。

若要取得此介面，請呼叫 **CoCreateInstance** 並傳入 **IID \_ IWpdSerializer**。

## <a name="members"></a>成員

**IWpdSerializer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWpdSerializer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWpdSerializer** 介面具有這些方法。



| 方法                                                                                          | 描述                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | 將提交的 **IPortableDeviceValues** 介面序列化為配置的位元組陣列。<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | 將位元組陣列還原序列化為 **IPortableDeviceValues** 介面。<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | 計算保存序列化 **IPortableDeviceValues** 介面所需的緩衝區大小。<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | 將 **IPortableDeviceValues** 介面序列化為呼叫端配置的位元組陣列。<br/>                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**驅動程式介面**](driver-interfaces.md)
</dt> </dl>

 

