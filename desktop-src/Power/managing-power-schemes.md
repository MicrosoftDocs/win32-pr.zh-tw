---
description: 電源配置管理
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: 電源配置管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4717fd8efc91a520e178baac6ad9138028f306386ed2ee1141b76a423b16e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143401"
---
# <a name="power-scheme-management"></a>電源配置管理

每個電源配置都是由 **GUID** 來唯一識別。 若要列舉所有可用的電源配置，請使用 [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) 函數。 **PowerEnumerate** 也可用來取得指定配置的所有電源設定。

目前正在系統上使用的電源配置稱為「使用中」電源配置或方案。 若要取得使用中計畫的 **GUID** ，請呼叫 [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) 函數。 若要變更作用中的電源計劃，請呼叫 [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) 函式。

若要建立電源配置，您必須先使用 [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) 函式來複製現有的配置，並指定您想要作為新配置基礎之配置的 **GUID** 。 您應該複製其中一個內建的配置，並依據您的需求修改電源設定。 請注意，建立電源計劃不會自動更新主動式電源計劃。 您必須一律呼叫 [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) 來更新使用中的電源計劃。 您可以修改現有的電源計劃，然後以同樣的方式套用。

若要移除電源計劃，請呼叫 [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) 函數。

> [!Note]  
> 若要取出系統電源狀態的其他資訊，請呼叫 [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) 函數。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[電源配置](power-schemes.md)
</dt> </dl>

 

 



