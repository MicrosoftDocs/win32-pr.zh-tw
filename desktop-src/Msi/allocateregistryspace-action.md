---
description: AllocateRegistrySpace 動作可確保登錄中的 AVAILABLEFREEREG 屬性所指定的可用登錄空間量是否存在。
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: AllocateRegistrySpace 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986890"
---
# <a name="allocateregistryspace-action"></a>AllocateRegistrySpace 動作

AllocateRegistrySpace 動作可確保登錄中的 [**AVAILABLEFREEREG**](availablefreereg.md) 屬性所指定的可用登錄空間量是否存在。

## <a name="sequence-restrictions"></a>順序限制

您必須在 [InstallInitialize](installinitialize-action.md)之後呼叫 AllocateRegistrySpace 動作。 建議您在所有其他動作之前排程 AllocateRegistrySpace，以確保有足夠的登錄空間可繼續。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述     |
|-------|--------------------------------|
| \[1\] | 需要登錄空間，以 KB 為單位。 |



 

 

 



