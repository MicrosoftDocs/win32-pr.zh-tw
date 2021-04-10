---
description: COOKER 變異數 \_ 計數器類型公式提供的變化性，是用來表示在 Win32 PerfRawData 實例中某一個屬性的一組原始觀察值的散佈 \_ 。
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026548"
---
# <a name="cooker_variance"></a>COOKER \_ 變異數

COOKER 變異數 \_ 計數器類型公式提供的變化性，是用來表示在 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 實例中某一個屬性的一組原始觀察值的散佈。 變異數的計算方式是將偏差的平方總和與每個計數器的平均值除以計數器數目。 換句話說，變異數是每個計數器平均平方差的平均值。 此計數器類型只會在 WMI 內定義，而不能用於效能監視技術，例如 [效能計數器6.0 版](/windows/desktop/PerfCtrs/performance-counters-portal)。

如需有關計數器類型公式的詳細資訊，請參閱 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))。

如需有關高效能提供者和腳本的詳細資訊，請參閱 [WMI 效能計數器類型](wmi-performance-counter-types.md)。

## <a name="example-code"></a>範例程式碼

如需程式碼範例，請參閱 [取得統計效能資料](obtaining-statistical-performance-data.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[統計計數器類型](statistical-counter-types.md)
</dt> <dt>

[監視效能資料](monitoring-performance-data.md)
</dt> </dl>

 

 
