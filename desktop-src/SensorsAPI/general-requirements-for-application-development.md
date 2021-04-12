---
description: 本主題說明開始建立使用感應器 API 的程式時，必須執行的動作。
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: 應用程式開發 (感應器 API) 的一般需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320035"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>應用程式開發 (感應器 API) 的一般需求

本主題說明開始建立使用感應器 API 的程式時，必須執行的動作。

若要建立感應器 API 應用程式，您必須在電腦上安裝 Windows 7 和 Windows 7 軟體發展工具組 (SDK) 。 下表說明您將需要的特定檔案。



| 檔案名稱               | 描述                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi。h            | 感應器 API 的主要標頭檔。 此標頭檔包含介面定義。               |
| 感應器。h               | 包含平臺定義常數定義的標頭檔。                                    |
| Initguid。h              | 包含用於控制 **GUID** 初始化之定義的標頭檔。                          |
| FunctionDiscoveryKeys。h | 標頭檔，定義當您連接到邏輯感應器時，所需的裝置識別碼屬性索引鍵。 |
| Sensorsapi .lib          | 靜態程式庫，其中包含感應器 API 的 **GUID** 定義。                                     |
| PortableDeviceGuids .lib | 靜態程式庫，其中包含 Windows 可攜式裝置物件的 **GUID** 定義。                   |



 

您的程式可能需要額外的檔案。

## <a name="supported-operating-systems"></a>支援的作業系統

感應器 API 應用程式將會在 windows 7 Starter edition 以外的所有 Windows 7 版本上執行。

## <a name="windows-portable-devices-interfaces"></a>Windows 可攜式裝置介面

感應器 API 會使用某些 Windows 可攜式裝置 (WPD) 物件來封裝屬性索引鍵和值。 下表描述這些物件的介面。



| 介面                                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | 這個介面可讓您輕鬆地建立名稱/值配對的屬性包。 名稱會以 **PROPERTYKEY** 來表示，而值則是以 **PROPVARIANT** s 表示。 <br/> API 會使用此介面來設定和同時抓取單一值和值的集合。 您可以從方法中取出這個介面，或者，如果需要新的物件，請呼叫具有 CLSID PortableDeviceValues 的 **CoCreateInstance** \_ 。<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | 這個介面包含 **PROPERTYKEY** 的集合。 這些索引鍵代表可由 **IPortableDeviceValues** 儲存的屬性名稱。 API 會使用此集合物件來設定和抓取單一屬性名稱和屬性名稱的集合。<br/> 您可以從方法中取出這個介面，或者，如果需要新的物件，請呼叫具有 CLSID PortableDeviceKeyCollection 的 **CoCreateInstance** \_ 。 <br/>    |



 

 

