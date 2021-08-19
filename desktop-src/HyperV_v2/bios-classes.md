---
description: 虛擬 BIOS 是載入 RAM 的軟體映射，可設定部分的基本層面，並將電腦系統開機。 每台電腦系統都有一個 BIOS 元素，而且無法取代或移除該元素。
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: BIOS 類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9605f28a23fc84b653ba5efe6c6e4be057eba48da81ddb777c7516d1317da6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813635"
---
# <a name="bios-classes"></a>BIOS 類別

虛擬 BIOS 是載入 RAM 的軟體映射，可設定部分的基本層面，並將電腦系統開機。 每台電腦系統都有一個 BIOS 元素，而且無法取代或移除該元素。 因此，沒有任何資源集區可將新的 BIOS 元素新增至虛擬機器。 BIOS 元素也沒有自己的 SettingData 類別來描述 BIOS 的設定。 您可以在 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別中找到 BIOS 的設定，例如序號、開機順序和 num lock 狀態。

以下是與 BIOS 相關的虛擬化 WMI 類別。 這些類別位於中 \\ \\ 。 \\根 \\ 虛擬化命名空間。

## <a name="in-this-section"></a>本節內容



| 主題                                                    | 描述                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**Msvm \_ BIOSElement**](msvm-bioselement.md)<br/> | 代表載入 RAM 以設定及啟動系統的低層級軟體。<br/> |
| [**Msvm \_ SystemBIOS**](msvm-systembios.md)<br/>   | 用來將虛擬機器與其 BIOS 產生關聯。<br/>                                           |



 

 

 




