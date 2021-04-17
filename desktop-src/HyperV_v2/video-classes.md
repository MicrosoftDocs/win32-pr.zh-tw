---
description: 所有虛擬機器都反映出模擬的 S3 影片控制器以及加速的綜合視訊控制器。
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: 影片類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469433"
---
# <a name="video-classes"></a>影片類別

所有虛擬機器都反映出模擬的 S3 影片控制器以及加速的綜合視訊控制器。

每個顯示控制器都有與其相關聯的影片標頭物件。 虛擬機器中隨時只能有一個顯示控制器處於作用中狀態。

連接至虛擬機器的每個作用中遠端會話都有一個終端機連線。

以下是與影片相關的虛擬化 WMI 類別。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                  | 描述                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ S3DisplayController**](msvm-s3displaycontroller.md)<br/>               | 代表存在於每個虛擬機器設定中的模擬 S3 控制器的狀態。<br/>       |
| [**Msvm \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)<br/> | 代表存在於每個虛擬機器設定中的綜合顯示控制器的狀態。<br/> |
| [**Msvm \_ SystemTerminalConnection**](msvm-systemterminalconnection.md)<br/>     | 將虛擬機器與終端機連線建立關聯。<br/>                                                        |
| [**Msvm \_ TerminalConnection**](msvm-terminalconnection.md)<br/>                 | 表示與虛擬機器互動之作用中遠端會話的狀態。<br/>                             |
| [**Msvm \_ VideoHead**](msvm-videohead.md)<br/>                                   | 描述顯示控制器上的主要繪圖介面。<br/>                                                  |
| [**Msvm \_ VideoHeadOnController**](msvm-videoheadoncontroller.md)<br/>           | 將影片標頭與包含它的影片控制器產生關聯。<br/>                                             |



 

 

 




