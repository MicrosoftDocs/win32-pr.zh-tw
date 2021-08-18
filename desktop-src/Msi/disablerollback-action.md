---
description: DisableRollback 動作會停用其餘安裝的復原。
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: DisableRollback 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe500e3b810e5b06802e3a0face1da9b76441099a407882da08d5911a37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745368"
---
# <a name="disablerollback-action"></a>DisableRollback 動作

DisableRollback 動作會停用其餘安裝的 [復原](rollback-installation.md) 。 只有在順序資料表中的 DisableRollback 動作之後排序的動作才會停用復原。 如果 DisableRollback 動作是在 [InstallInitialize 動作](installinitialize-action.md)之前排序，則會停用整個安裝的復原。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-message"></a>ActionData 訊息

沒有任何 ActionData 訊息。

 

 



