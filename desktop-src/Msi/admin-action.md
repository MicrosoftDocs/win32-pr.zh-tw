---
description: 系統管理員動作是用來執行系統管理安裝的最上層動作。
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: 管理動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848986"
---
# <a name="admin-action"></a>管理動作

系統管理員動作是用來執行系統 [管理安裝](administrative-installation.md)的最上層動作。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

系統管理員動作不會從動作資料表序列內呼叫，Windows Installer 會在使用設定為 "ACTION = ADMIN" 的 *szCommandLine* 參數呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)時執行此動作，或使用 '/a ' 命令列參數來呼叫命令列可執行檔 Msiexec.exe。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AdminUISequence 資料表](adminuisequence-table.md)
</dt> <dt>

[AdminExecuteSequence 資料表](adminexecutesequence-table.md)
</dt> </dl>

 

 



