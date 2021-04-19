---
description: 虛擬機器中的序列裝置包含序列控制器和序列埠。 每部虛擬機器只有一個串列控制器，且每個序列控制器都有兩個序列埠。
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: 序列裝置類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987597"
---
# <a name="serial-devices-classes"></a>序列裝置類別

虛擬機器中的序列裝置包含序列控制器和序列埠。 每部虛擬機器只有一個串列控制器，且每個序列控制器都有兩個序列埠。

無法設定序列控制器的設定;因此，沒有相關聯的設定資料實例。 此外，您無法在虛擬機器中新增或移除串列控制器或序列埠。 因此，沒有適用于序列裝置的資源集區實例。

以下是與序列裝置相關的虛擬化 WMI 類別。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                      | 描述                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Msvm \_ SerialController**](msvm-serialcontroller.md)<br/>                         | 代表序列控制器的功能和管理。<br/> |
| [**Msvm \_ SerialPort**](msvm-serialport.md)<br/>                                     | 代表與序列控制器相關聯的序列埠。<br/>      |
| [**Msvm \_ SerialPortOnSerialController**](msvm-serialportonserialcontroller.md)<br/> | 將序列埠與序列控制器產生關聯。<br/>                   |



 

 

 




