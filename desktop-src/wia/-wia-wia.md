---
description: Wia 物件是所有 Windows 映像取得 (WIA) 腳本功能的進入點。
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: Wia 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113264"
---
# <a name="wia-object"></a>Wia 物件

**Wia** 物件是所有 Windows 映像取得 (Wia) 腳本功能的進入點。 使用 WIA 腳本模型的任何應用程式都必須建立 [**SafeWia**](-wia-safewia.md) 或 **WIA** 物件。 您可以使用該物件來列舉和建立裝置，並接收硬體事件的通知。

> [!Note]  
> 此物件對腳本而言並不安全。 如需此物件可安全地進行腳本處理的版本，請參閱 [**SafeWia**](-wia-safewia.md)。

 

## <a name="members"></a>成員

**Wia** 物件具有下列類型的成員：

-   [事件](#events)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**Wia** 物件具有這些事件。



| 事件                                                                 | 描述                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | 連接新的 WIA 硬體裝置時所發生的事件。<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | 當新的 WIA 硬體裝置中斷連線時所發生的事件。<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | 成功完成資料傳輸時所發生的事件。<br/> |



 

### <a name="methods"></a>方法

**Wia** 物件具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**創建**](-wia-iwia-create.md) | **Wia** 物件的 [**Create**](-wia-iwia-create.md)方法會連接到指定的 Wia 裝置，並傳回代表該裝置的 [**專案**](-wia-item.md)物件。<br/> |



 

### <a name="properties"></a>屬性

**Wia** 物件具有這些屬性。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">屬性</th>
<th style="text-align: left;">存取類型</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>設備</strong></a><br/></td>
<td style="text-align: left;">唯讀<br/></td>
<td style="text-align: left;"><a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a>物件的集合，代表安裝在電腦上的所有裝置。 唯讀。 <br/>
<blockquote>
[!Note]<br />
這個集合是以0為基礎。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (4.90 版或更新版本) </dt> </dl> |
| IID<br/>                      | CLSID \_ Wia<br/>                                                                                         |



 

 




