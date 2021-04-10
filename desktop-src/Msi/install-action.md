---
description: 安裝動作是呼叫以安裝或移除元件的最上層動作。
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: 安裝動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026584"
---
# <a name="install-action"></a>安裝動作

安裝動作是呼叫以安裝或移除元件的最上層動作。 此動作會查詢 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md) ，以瞭解要執行的動作、動作執行的條件，以及順序中的動作位置：

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

系統不會從動作資料表序列內呼叫安裝動作，它會在呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 時傳遞給 Windows Installer，或使用 '**/i**' 命令列參數來呼叫命令列可執行檔 Msiexec.exe，或呼叫任何可能執行安裝工作的安裝程式函數，例如 [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)、 [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)或 [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)。

 

 



