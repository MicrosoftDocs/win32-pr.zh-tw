---
title: DVC 執行詳細資料
description: 本節包含有關如何 (DVC) 用戶端模組寫入動態虛擬通道的資訊。
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969648"
---
# <a name="dvc-implementation-details"></a>DVC 執行詳細資料

本節包含有關如何 (DVC) 用戶端模組寫入動態虛擬通道的資訊。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[撰寫用戶端 DVC 模組](writing-a-client-dvc-component.md)
</dt> <dd>

若要 (DVC) 用戶端模組寫入動態虛擬通道，您必須先執行並註冊遠端桌面連線 (RDC) 用戶端外掛程式。

</dd> <dt>

[DVC 外掛程式註冊](dvc-plug-in-registration.md)
</dt> <dd>

描述遠端桌面連線 (RDC) 用戶端的動態虛擬通道 (DVC) 外掛程式專案的語法。

</dd> <dt>

[啟動 DVC 接聽程式](starting-a-dvc-listener.md)
</dt> <dd>

若要建立兩個動態虛擬通道之間的成功連接 (DVC) 遠端桌面連線 (RDC) 用戶端和伺服器上執行的模組，則 DVC 接聽程式必須正在執行且處於接聽狀態。

</dd> <dt>

[接受連接](accepting-a-connection.md)
</dt> <dd>

在某個時間點，動態虛擬通道 (DVC) 用戶端會要求 DVC 接聽程式的連接。

</dd> <dt>

[使用 DVC 通道寫入資料](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

使用動態虛擬通道來寫入通道資料 (DVC) 是遠端桌面工作階段主機 (RD 工作階段主機) 伺服器和用戶端的對稱。

</dd> <dt>

[測試和調試](testing-and-debugging.md)
</dt> <dd>

有一個由遠端桌面連線 (RDC) 用戶端所執行的「echo」接聽程式，其一律存在並接聽連入連線。

</dd> <dt>

[DVC 用戶端外掛程式範例](dvc-client-plug-in-example.md)
</dt> <dd>

C + + 程式碼範例，說明如何) 用戶端動態虛擬通道 (DVC) 外掛程式建立遠端桌面連線 (RDC。

</dd> <dt>

[DVC 伺服器模組範例](dvc-server-component-example.md)
</dt> <dd>

C + + 程式碼範例，說明如何建立伺服器端動態虛擬通道 (DVC) 模組。

</dd> </dl>

 

 




